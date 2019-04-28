---
title: Windows betik motorları | Microsoft Docs
ms.custom: ''
ms.date: 01/18/2017
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: article
helpviewer_keywords:
- Windows script engines
ms.assetid: e576853d-7252-4eb9-81eb-9d5bb7626ab4
caps.latest.revision: 12
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: 1acbc364e9ee2a5a4911564eb6d2c7d4c34de458
ms.sourcegitcommit: 47eeeeadd84c879636e9d48747b615de69384356
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "63416003"
---
# <a name="windows-script-engines"></a>Windows Komut Dosyası Motorları
Microsoft Windows betik altyapısı uygulamak için aşağıdaki arabirimlerinden destekleyen bir OLE COM nesnesi oluşturun.  
  
|||  
|-|-|  
|Arabirim|Açıklama|  
|[IActiveScript](../winscript/reference/iactivescript.md)|Temel betik oluşturma olanağı sağlar. Bu arabirimin gereklidir.|  
|[IActiveScriptParse](../winscript/reference/iactivescriptparse.md)|Betik metin eklemek, nevyhodnocovat ve benzeri olanağı sağlar. Bu arabirimin isteğe bağlıdır; uygulanmazsa, ancak komut dosyası altyapısı IPersist * arabirimlerinden biri, bir komut dosyası yüklemek için uygulamanız gerekir.|  
|IPersist *|Kalıcılık desteği sağlar. Uygulama aşağıdaki arabirimlerinden en az birinin ise gerekli [Iactivescriptparse](../winscript/reference/iactivescriptparse.md) uygulanmadı.<br /><br /> IPersistStorage: VERİLER için destek sağlayan = {url} özniteliğini nesne etiketi.<br /><br /> IPersistStreamInit: Aynı için destek sağlar `IPersistStorage` verilerin yanı sıra = "dizesi olarak kodlanmış bayt akışı" özniteliğini nesne etiketi.<br /><br /> IPersistPropertyBag: PARAM için destek sağlar = özniteliğini nesne etiketi.|  
  
> [!NOTE]
> Komut dosyası altyapısı asla üzerine kaydetmek veya bir betik durumu ile geri yüklemek için çağrılmaz, mümkündür `IPersist*`. Bunun yerine, [Iactivescriptparse](../winscript/reference/iactivescriptparse.md) çağırarak kullanılan [IActiveScriptParse::InitNew](../winscript/reference/iactivescriptparse-initnew.md) boş bir komut dosyası oluşturmak için ardından kod parçacıklarını eklenmiş ve olaylar ile bağlı [Iactivescriptparse:: AddScriptlet](../winscript/reference/iactivescriptparse-addscriptlet.md) ve genel kod ile eklenen [IActiveScriptParse::ParseScriptText](../winscript/reference/iactivescriptparse-parsescripttext.md). Öte yandan, bir komut dosyası altyapısı tam olarak en az bir uygulamalıdır `IPersist*` arabirimi (tercihen `IPersistStreamInit`), diğer uygulamaları barındırmak yapmaya çünkü bunları kullanın.  
  
 Aşağıdaki bölümlerde, bir Windows komut dosyası altyapısı uygulama daha ayrıntılı olarak açıklanmaktadır.  
  
 Bkz: [Windows betik arabirimleri başvurusu](../winscript/reference/windows-script-interfaces-reference.md) daha fazla bilgi için.  
  
## <a name="registry-standard"></a>Kayıt defteri standart  
 Bir Windows komut dosyası altyapısı kendi kategori tanımlayıcıları kullanarak tanımlayabilirsiniz. Windows komut dosyası şu anda iki kategori tanımlayıcı tanımlar.  
  
|||  
|-|-|  
|Kategori|Açıklama|  
|CATID_ActiveScript|Sınıf tanımlayıcıları (CLSID) desteği, en azından Windows betik motorları olduğunu gösterir [IActiveScript](../winscript/reference/iactivescript.md) arabirimi ve Kalıcılık mekanizması ( `IPersistStorage`, `IPersistStreamInit`, veya IPersistPropertyBag arabirimi).|  
|CATID_ActiveScriptParse|Desteği, en azından Windows betik motorları CLSID gösterir [IActiveScript](../winscript/reference/iactivescript.md) ve [Iactivescriptparse](../winscript/reference/iactivescriptparse.md) arabirimleri.|  
  
 Ancak [Iactivescriptparse](../winscript/reference/iactivescriptparse.md) bir true Kalıcılık mekanizması değil destekliyor mu [IActiveScriptParse::InitNew](../winscript/reference/iactivescriptparse-initnew.md) işlevsel olarak eşdeğerdir yöntemi `IPersist*::InitNew`.  
  
## <a name="script-engine-states"></a>Komut dosyası motoru durumu  
 Herhangi bir zamanda bir Windows komut dosyası altyapısı birkaç durumdan birinde olabilir.  
  
|||  
|-|-|  
|Durum|Açıklama|  
|başlatılmamış|Komut dosyası değiştirilmediğinden olmayan başlatıldı veya IPersist * arabirim kullanılarak yüklenen bir [Iactivescriptsite](../winscript/reference/iactivescriptsite.md) arabirim kümesi. Betik yüklendiğinde kadar komut dosyası altyapısı genellikle bu durumdan kullanılabilir durumda değil.|  
|başlatıldı|Betik ile başlatılmış bir `IPersist*` arabirim ve sahip bir [Iactivescriptsite](../winscript/reference/iactivescriptsite.md) arabirim kümesi, ancak konak nesneleri ve indirme olaylarına bağlı değil. Bu durum yalnızca, anlamına gelir `IPersist*::Load`, `IPersist*::InitNew`, veya [IActiveScriptParse::InitNew](../winscript/reference/iactivescriptparse-initnew.md) yöntemi tamamlandıktan ve [IActiveScript::SetScriptSite](../winscript/reference/iactivescript-setscriptsite.md) has yöntemi çağrılmış. Altyapı kodunu bu modda çalıştırılamaz. Alt yapısı ana bilgisayar üzerinden geçirir kod kuyruklar [IActiveScriptParse::ParseScriptText](../winscript/reference/iactivescriptparse-parsescripttext.md) yöntemi ve sonra başlangıç durumuna geçiş kodu yürütür.<br /><br /> Dilleri semantiği yaygın olarak değişebileceğinden altyapılarının bu durum geçişi desteklemek için gerekli değildir. Altyapıları destekleyen [IActiveScript::Clone](../winscript/reference/iactivescript-clone.md) yöntemi bu durum geçişi ancak desteklemesi gerekir. Konaklar için bu geçiş hazırlama ve uygun eylemi gerçekleştirin: sürüm geçerli komut dosyası altyapısı, yeni bir komut dosyası altyapısı ve çağrı `IPersist*::Load`, `IPersist*::InitNew`, veya [IActiveScriptParse::InitNew](../winscript/reference/iactivescriptparse-initnew.md) (ve büyük olasılıkla çağırıp [IActiveScriptParse::ParseScriptText](../winscript/reference/iactivescriptparse-parsescripttext.md)). Bu geçiş kullanımını iyileştirme yukarıdaki adımları dikkate alınmalıdır. Komut dosyası altyapısı adlı öğelerin adlarını hakkında herhangi bir bilgi edinmiş olması ve adlandırılmış öğeleri açıklayan tür bilgisi geçerli kaldığı unutmayın.<br /><br /> Dilleri büyük ölçüde farklılık gösterdiğinden, bu geçiş tam semantiği tanımlamak zordur. En azından, komut dosyası altyapısı gerekir tüm olayları bağlantısını kesmek ve yayınlama işlemlerinin tümünün çağırılarak SCRIPTINFO_IUNKNOWN işaretçiler [IActiveScriptSite::GetItemInfo](../winscript/reference/iactivescriptsite-getiteminfo.md) yöntemi. Betiği yeniden çalıştırdıktan sonra altyapısı bu işaretçileri yeniden almanız gerekir. Komut dosyası altyapısı, betik dili için uygun bir ilk durumuna geri için de sıfırlamalısınız. Örneğin, VBScript tüm değişkenlerini sıfırlar ve dinamik olarak çağırarak eklenen herhangi bir kod korur [IActiveScriptParse::ParseScriptText](../winscript/reference/iactivescriptparse-parsescripttext.md) ile SCRIPTTEXT_ISPERSISTENT bayrağı ayarlanmış. Diğer diller geçerli değerleri (gibi hiçbir kod/verilerin ayrılmasını olduğundan Lisp) tutmak mı (statik olarak başlatılmış değişkenleri dillerle içerir) iyi bilinen bir duruma sıfırlayın gerekebilir.<br /><br /> Başlangıç durumuna geçişi ile aynı semantiğe sahip gerektiğini unutmayın (diğer bir deyişle, bu komut dosyası altyapısı aynı durumda bırakmanız gerekir) çağrıldığında `IPersist*::Save` kaydetmek için komut dosyası altyapısı ve ardından arama `IPersist*::Load` yeni bir yükleme için komut dosyası motoru; bunlar Eylemler aynı semantiklere sahip olmalıdır [IActiveScript::Clone](../winscript/reference/iactivescript-clone.md). Komut dosyası henüz desteklemediği altyapılarındaki `IActiveScript::Clone` veya `IPersist*` böyle bir geçiş Yukarıdaki koşullar, ihlal değil, dikkatli bir şekilde başlangıç durumuna geçişi nasıl davranacağı, dikkate almanız gereken `IActiveScript::Clone` veya `IPersist*` Daha sonra destek eklendi.<br /><br /> Bu geçişi başlatıldı durumuna sırasında komut dosyası altyapısı olay havuzlarını öğesinden sonra uygun Yıkıcılar bağlantısını keser ve benzeri, betikte yürütülür. Yürütülen bu yok ediciler girmekten kaçınmak için konak ilk komut bağlantısı kesilmiş durumuna başlatılan duruma geçmeden önce taşıyabilirsiniz.<br /><br /> Kullanım [IActiveScript::InterruptScriptThread](../winscript/reference/iactivescript-interruptscriptthread.md) sonlanması, çalışan bir betik iş parçacığı için geçerli olay beklemeden iptal etmek ve benzeri şekilde.|  
|Başlatıldı|Başlatılmış bir durumda durumundan başlangıç durumuna başlatılan durumda sıraya alındı herhangi bir kod yürütmek altyapı sağlar. Motoru başlangıç durumuna kod yürütebilir, ancak eklenen herhangi bir olay için bağlanmadı [IActiveScript::AddNamedItem](../winscript/reference/iactivescript-addnameditem.md) yöntemi. Altyapısı elde IDispatch çağırarak kod yürütebilir [IActiveScript::GetScriptDispatch](../winscript/reference/iactivescript-getscriptdispatch.md) yöntemi çağırarak veya [IActiveScriptParse::ParseScriptText](../winscript/reference/iactivescriptparse-parsescripttext.md). Daha fazla arka plan başlatmanın (aşamalı yükleme) hala devam eden mümkündür ve bu çağırma [IActiveScript::SetScriptState](../winscript/reference/iactivescript-setscriptstate.md) yöntemi SCRIPTSTATE_CONNECTED bayrağı ayarlanmış engellemek betik neden olabilir başlatma işlemi tamamlanana kadar.|  
|Bağlı|Betik yüklendi ve olayları konak nesnelerden indirme için bağlı. Bu bir geçiş başlatılmış bir durumda ise, komut dosyası altyapısı aracılığıyla bağlı durumuna giriliyor ve olayları bağlama önce gerekli eylemleri gerçekleştirme başlangıç durumuna geçiş.|  
|Bağlantısı kesildi|Betik yüklenir ve bir çalışma zamanı durumu vardır ancak konak nesnelerden indirme olaylardan geçici olarak kesilir. Bu ya da mantıksal olarak yapılabilir (alınan olayları yoksayılıyor) veya fiziksel (uygun bir bağlantı noktalarında IConnectionPoint::Unadvise çağırma). Bu bir geçiş başlatılmış bir durumda ise, komut dosyası altyapısı aracılığıyla bağlantısı kesilmiş girmeden önce gerekli eylemleri gerçekleştirme başlangıç durumuna geçiş. İşlenmekte olan olay havuzlarını durum değişikliklerini önce tamamlandı (kullanın [IActiveScript::InterruptScriptThread](../winscript/reference/iactivescript-interruptscriptthread.md) çalışan bir betik iş parçacığının iptal etmek için). Bu durum, bu durum geçişi sıfırlamak komut dosyası neden olmaz, betik çalıştırma durumu sıfırlanır ve bir betiği başlatma yordamı çalıştırılmadı başlatılmış durumundan ayırt edilir.|  
|Kapalı|Komut dosyası kapatıldı. Komut dosyası altyapısı artık çalışır ve çoğu yöntemleri için hataları döndürür.|  
  
 Aşağıdaki çizimde, çeşitli komut dosyası motoru durumu ilişkiler gösterilmektedir ve geçişleri bir durumdan diğerine neden yöntemleri gösterir.  
  
 Aşağıdaki çizim, komut dosyası altyapısı çeşitli durumuna geçişler sırasında gerçekleştirdiği eylemleri gösterir.  
  
## <a name="scripting-engine-threading"></a>Komut dosyası altyapısı iş parçacığı  
 Bir Windows komut dosyası altyapısı birçok ortamlarda kullanılabildiğinden, yürütme modeli kadar esnek tutmak önemlidir. Örneğin, sunucu tabanlı bir konak, verimli bir şekilde Windows komut dosyası kullanarak birden çok iş parçacıklı bir tasarım korumak gerekebilir. Aynı anda, normal bir uygulama gibi iş parçacığı kullanmayan bir konak yönetim iş parçacığı ile burdened değil. Windows komut dosyası, bu dengeyi konağa konaklarından Bu yük boşaltma, serbest iş parçacıklı bir komut dosyası altyapısı geri arama yöntemleri kısıtlayarak elde eder.  
  
 Altyapılarının sunucularında kullanılan genellikle ücretsiz iş parçacıklı COM nesneleri uygulanır. Diğer bir deyişle yöntemlerde [IActiveScript](../winscript/reference/iactivescript.md) ve onun ilişkili arabirim çağrılabilir işleminde, bir iş parçacığından hazırlama olmadan. (OLE nesneleri serbest iş parçacıklı işlemler arası hazırlama şu anda desteklemediği için ne yazık ki bu da bir işlem sunucusu uygulanması gereken komut dosyası altyapısı anlamına gelir.) Eşitleme komut dosyası altyapısı sorumluluğundadır. Dahili olarak desteklemeyeceğini olmayan altyapıları betik oluşturma ya da birden çok iş parçacıklı olmayan dil modelleri için eşitleme erişimi bir mutex ile komut dosyası altyapısı serileştirmek olarak basit olabilir. Kuşkusuz belirli yöntemler gibi [IActiveScript::InterruptScriptThread](../winscript/reference/iactivescript-interruptscriptthread.md), böylece takılmış bir komut dosyası başka bir iş parçacığından sonlandırılabilir bu şekilde seri hale getirilmemelidir.  
  
 Olgu, [IActiveScript](../winscript/reference/iactivescript.md) genellikle serbest iş parçacıklı, genellikle gelir [Iactivescriptsite](../winscript/reference/iactivescriptsite.md) arabirimi ve ana bilgisayarın nesne modeli olmalıdır ücretsiz iş parçacıklı de. Bu uygulama konağının özellikle tek iş parçacıklı Windows tabanlı bir uygulama, nesne modelinde tek iş parçacıklı ya da apartman modeli ActiveX denetimi ile ana bilgisayar olduğu ortak durumda oldukça zor hale getirir. Bu nedenle, aşağıdaki kısıtlamalar üzerinde komut dosyası altyapısının kullanımını yerleştirilir [Iactivescriptsite](../winscript/reference/iactivescriptsite.md):  
  
 Betik site her zaman bir ana iş parçacığının bağlamında çağrılır. Diğer bir deyişle, komut dosyası altyapısı hiçbir zaman komut dosyası altyapısı oluşturulan iş parçacığı, ancak yalnızca içinden bağlamında betik site bir komut dosyası altyapısı konaktan çağrılan yöntemi çağrıları [IActiveScript](../winscript/reference/iactivescript.md) ve sunulan komut dosyası altyapısının dağıtım nesnesi aracılığıyla bir Windows iletisi veya ana bilgisayarın nesne modelinde bir olay kaynağı aracılığıyla türevleri.  
  
 Betik site hiçbir zaman basit bir iş parçacığı durumu denetimi yöntemi bağlamında çağrılır (örneğin, [IActiveScript::InterruptScriptThread](../winscript/reference/iactivescript-interruptscriptthread.md) yöntemi) veya [IActiveScript::Clone](../winscript/reference/iactivescript-clone.md) yöntem.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Windows Komut Dosyası Arabirimleri](../winscript/windows-script-interfaces.md)

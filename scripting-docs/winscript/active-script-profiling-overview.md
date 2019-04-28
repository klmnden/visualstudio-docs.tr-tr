---
title: Etkin betik profil oluşturmaya genel bakış | Microsoft Docs
ms.custom: ''
ms.date: 01/18/2017
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: article
helpviewer_keywords:
- Active Script Profiling
ms.assetid: eec2f413-6605-4df4-a86f-4919755e9358
caps.latest.revision: 10
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: 777d20ecb51b09b282f88dc08464727b9ff2a945
ms.sourcegitcommit: 47eeeeadd84c879636e9d48747b615de69384356
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "63432969"
---
# <a name="active-script-profiling-overview"></a>Etkin Komut Dosyası Profil Oluşturmaya Genel Bakış
[Etkin komut dosyası Profiler arabirimleri](../winscript/reference/active-script-profiler-interfaces.md) bir komut dosyası altyapısı profil oluşturmayı etkinleştirin. Etkin betik profil oluşturma, aşağıdaki bölümden oluşur:  
  
- Dil altyapısı  
  
- Ana bilgisayar  
  
- Profil Oluşturucu  
  
## <a name="language-engine"></a>Dil altyapısı  
 Dil altyapısı betiğini yürütür. Bunu, betik kodunu yürütülür gibi profil oluşturma olanak tanıyan yöntemler sağlar. Profil oluşturma etkin olduğunda, dil altyapısı bağımsız değişken olarak COM nesnesi profil oluşturucu sınıfı tanımlayıcısı (CLSID) alır. Profil Oluşturucu COM nesnesinin bir örneğini oluşturur ve sonra çeşitli olaylar meydana geldiğinde profil oluşturucuyu çağırır.  
  
 Dil altyapısı uygulayan [Iactivescriptprofilercontrol arabirimi](../winscript/reference/iactivescriptprofilercontrol-interface.md).  
  
> [!NOTE]
> [!INCLUDE[javascript](../javascript/includes/javascript-md.md)] Dil çalışma zamanı JS_PROFILER ortam değişkeni oluşturulurken, profil oluşturma etkinleştirilmesi gerekip gerekmediğini belirlemek için denetler. Bu değişken için profil oluşturucu CLSID değeri ayarlarsanız, dil çalışma zamanı oluşturmak için hangi profil oluşturucu belirlemek için değişkenin değerini kullanarak profil oluşturucu COM nesnesinin örneği oluşturur.  
  
## <a name="host"></a>Ana bilgisayar  
 Konağın dil altyapısı oluşturur ve yürütülecek komut dosyaları ile dil altyapısı sağlar. Bir akıllı ana bilgisayar ayrıca, hata ayıklama veya profil oluşturma daha iyi bilgi sağlamak için hata ayıklayıcı veya profil oluşturucu tarafından kullanılabilir belge bağlamı sağlar.  
  
## <a name="profiler"></a>Profil Oluşturucu  
 Çeşitli olaylar meydana geldiğinde profil oluşturucu çağrılarını dil altyapısı alır. Profil Oluşturucu bir COM nesnesi olarak kayıtlı olması gerekir ve uygulamalıdır [Iactivescriptprofilercallback arabirimi](../winscript/reference/iactivescriptprofilercallback-interface.md) arabirimi.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Etkin Betik Profil Oluşturucu Arabirimleri](../winscript/reference/active-script-profiler-interfaces.md)
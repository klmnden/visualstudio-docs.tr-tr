---
title: Projeleri yükseltme | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
helpviewer_keywords:
- upgrading VSPackages
- upgrading applications, strategies
- VSPackages, upgrade support
ms.assetid: e01cb44a-8105-4cf4-8223-dfae65f8597a
author: madskristensen
ms.author: madsk
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: a6a9e5b73315d8332c71e0fb7ddc3c6c1df041c3
ms.sourcegitcommit: 40d612240dc5bea418cd27fdacdf85ea177e2df3
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/29/2019
ms.locfileid: "66344680"
---
# <a name="upgrading-projects"></a>Projeleri Yükseltme

Visual Studio sürümünden sonraki proje modeli değişiklikler, daha yeni sürümüne çalıştırabilmeniz için projeler ve çözümler yükseltilmesi özellikle gerektirebilir. [!INCLUDE[vsipsdk](../../extensibility/includes/vsipsdk_md.md)] Yükseltme desteği kendi projelerinde uygulamak için kullanılan arabirimleri sağlar.

## <a name="upgrade-strategies"></a>Yükseltme stratejileri

Yükseltme desteklemek için proje sistemi uygulamanızı tanımlamak ve yükseltme bir strateji yürütmelidir. Stratejinizi belirlemede yan yana (SxS) yedekleme, kopya yedekleme veya her ikisini de desteklemek seçebilirsiniz.

- SxS yedekleme, bir proje bir yerde, uygun dosya adı sonek, örneğin, ekleme "eski" Yükseltme gereken dosyaları kopyalar anlamına gelir.

- Kopya yedekleme, bir projenin tüm proje öğeleri kullanıcı tarafından sağlanan bir yedek konumuna kopyalar anlamına gelir. Ardından, özgün proje konumda sürücülerinizdeki ilgili dosyaların yükseltilir.

## <a name="how-upgrade-works"></a>Yükseltme nasıl çalışır?

Visual Studio'nun önceki bir sürümde oluşturulmuş bir çözümü daha yeni bir sürümde açıldığında, IDE yükseltilmesi gerekip gerekmediğini belirlemek için çözüm dosyasını denetler. Yükseltme gerekli ise **Yükseltme Sihirbazı** kullanıcı yükseltme sürecinde size yol için otomatik olarak başlatılır.

Bir çözüm yükseltme gerektiğinde, her proje fabrikası yükseltme stratejisinin için sorgular. Strateji, proje fabrikası kopya yedekleme veya SxS yedekleme destekleyip desteklemediğini belirler. Bilgiler gönderilir **Yükseltme Sihirbazı**, yedekleme için gerekli bilgileri toplar ve kullanıcıya uygun bir seçenek sunar.

### <a name="multi-project-solutions"></a>Birden çok proje çözümü

Varsa bir çözüm birden fazla proje içeren ve yükseltme stratejiler farklı gibi yalnızca SxS yedekleme destekleyen bir C++ projesi ve yalnızca kopya yedeği destekleyen bir Web projesi, proje fabrikalarını yükseltme stratejisini anlaşmaları gerekir.

Her proje fabrikası için çözüm sorgular <xref:Microsoft.VisualStudio.Shell.Interop.IVsProjectUpgradeViaFactory>. Ardından <xref:Microsoft.VisualStudio.Shell.Interop.IVsProjectUpgradeViaFactory.UpgradeProject_CheckOnly%2A> genel proje dosyalarını yükseltme gerekip gerekmediğini ve desteklenen yükseltme stratejiler belirlemek için. **Yükseltme Sihirbazı** sonra çağrılır.

Kullanıcı, sihirbaz tamamlandıktan sonra <xref:Microsoft.VisualStudio.Shell.Interop.IVsProjectUpgradeViaFactory.UpgradeProject%2A> gerçek yükseltmeyi gerçekleştirmek için her proje fabrikası çağrılır. Yedekleme kolaylaştırmak için IVsProjectUpgradeViaFactory yöntemleri sağlayan <xref:Microsoft.VisualStudio.Shell.Interop.SVsUpgradeLogger> yükseltme işleminin ayrıntılarını oturum hizmeti. Bu hizmet önbelleğe alınamaz.

Tüm ilgili genel dosyaları güncelleştirdikten sonra her proje fabrikası, bir proje oluşturmak seçebilirsiniz. Proje uygulama desteklemelidir <xref:Microsoft.VisualStudio.Shell.Interop.IVsProjectUpgrade>. <xref:Microsoft.VisualStudio.Shell.Interop.IVsProjectUpgrade.UpgradeProject%2A> Yöntemi tüm ilgili proje öğeleri yükseltmek sonra çağrılır.

> [!NOTE]
> <xref:Microsoft.VisualStudio.Shell.Interop.IVsProjectUpgradeViaFactory.UpgradeProject%2A> Yöntemi SVsUpgradeLogger hizmet sağlamaz. Bu hizmet, çağrılarak alınabilir <xref:Microsoft.VisualStudio.OLE.Interop.IServiceProvider.QueryService%2A>.

## <a name="best-practices"></a>En İyi Yöntemler

Kullanım <xref:Microsoft.VisualStudio.Shell.Interop.SVsQueryEditQuerySave> hizmetinin, bir dosya düzenlemeden önce düzenleyebilir ve kaydetmeden önce kaydedebilirsiniz olmadığını denetleyin. Bu yedekleme yardımcı olur ve yükseltme uygulamaları işlemek için kaynak denetimi altında proje dosyaları, dosyaları yetersiz izinler ve benzeri.

Kullanım <xref:Microsoft.VisualStudio.Shell.Interop.SVsUpgradeLogger> hizmet yedekleme tüm aşamalarında ve başarı veya başarısızlık yükseltme işleminin bilgi sağlamak için yükseltin.

Yedekleme ve projelerini yükseltme hakkında daha fazla bilgi için içinde vsshell2.idl IVsProjectUpgrade için yorumlara bakın.

## <a name="upgrading-custom-projects"></a> Özel projelerini yükseltme

Değiştirirseniz, ürünün farklı Visual Studio sürümleri arasında proje dosyasındaki bilgileri kalıcı sonra proje dosyası eski sürümden yeni sürüme yükseltme desteklemeniz gerekiyor. Katılmak izin veren yükseltmeyi desteklediği için **Visual Studio Dönüştürme Sihirbazı**, uygulama <xref:Microsoft.VisualStudio.Shell.Interop.IVsProjectUpgradeViaFactory> arabirimi. Bu arabirim, kopyalama yükseltmek için yalnızca mekanizması kullanılabilir içerir. Proje yükseltme açılır çözümün bir parçası olarak gerçekleşir. <xref:Microsoft.VisualStudio.Shell.Interop.IVsProjectUpgradeViaFactory> Arabirimi proje fabrikası tarafından uygulanan ya da proje fabrikadan elde edilebilir en az olmalıdır.

Kullanan eski mekanizması <xref:Microsoft.VisualStudio.Shell.Interop.IVsProjectUpgrade> arabirimi hala desteklenmektedir, ancak kavramsal olarak proje sistemi proje açıkken bir parçası olarak yükseltir. <xref:Microsoft.VisualStudio.Shell.Interop.IVsProjectUpgrade> Arabirimi tarafından durumunda bile Visual Studio ortamı bu nedenle adlı <xref:Microsoft.VisualStudio.Shell.Interop.IVsProjectUpgradeViaFactory> arabirimi adlı veya uygulandığında. Bu yaklaşım kullanmanıza olanak tanır <xref:Microsoft.VisualStudio.Shell.Interop.IVsProjectUpgradeViaFactory> yerinde (muhtemelen en yeni konum) yapılacak işleri geri kalanı tarafından temsilci kopyalama uygulamak ve yalnızca yükseltme bölümlerini proje <xref:Microsoft.VisualStudio.Shell.Interop.IVsProjectUpgrade> arabirimi.

Bir örnek uygulaması için <xref:Microsoft.VisualStudio.Shell.Interop.IVsProjectUpgrade>, bkz: [VSSDK örnekleri](https://aka.ms/vs2015sdksamples).

Aşağıdaki senaryolarda, proje yükseltmeleriyle ortaya çıkar:

- Dosyayı proje destekleyebileceğinden daha yeni bir biçimde varsa, bunu bildiren bir hata döndürmelidir. Bu, eski sürümünü sürümü denetlemek için kod içerdiğini varsayar.

- Varsa <xref:Microsoft.VisualStudio.Shell.Interop.__VSPPROJECTUPGRADEVIAFACTORYFLAGS.PUVFF_SXSBACKUP> bayrağı belirtilen <xref:Microsoft.VisualStudio.Shell.Interop.IVsProjectUpgradeViaFactory.UpgradeProject%2A> yöntemi, yükseltme gittiğini projenin açılış öncesinde yerinde yükseltme olarak uygulanabilir.

- Varsa <xref:Microsoft.VisualStudio.Shell.Interop.__VSPPROJECTUPGRADEVIAFACTORYFLAGS.PUVFF_COPYBACKUP> bayrağı belirtilen <xref:Microsoft.VisualStudio.Shell.Interop.IVsProjectUpgradeViaFactory.UpgradeProject%2A> yükseltme yöntemi, bir kopyasını yükseltme olarak uygulanır.

- Varsa <xref:Microsoft.VisualStudio.Shell.Interop.__VSUPGRADEPROJFLAGS.UPF_SILENTMIGRATE> bayrağı belirtilen <xref:Microsoft.VisualStudio.Shell.Interop.IVsProjectUpgrade.UpgradeProject%2A> çağrısında verilmişse, kullanıcı ortamı tarafından proje açıldıktan sonra proje dosyası, yerinde yükseltme yükseltmek için çalışandan. Örneğin, ortam çözümü daha eski bir sürümünü kullanıcı oturum açtığında yükseltmek için kullanıcıya sorar.

- Varsa <xref:Microsoft.VisualStudio.Shell.Interop.__VSUPGRADEPROJFLAGS.UPF_SILENTMIGRATE> bayrağı belirtilmiş değil <xref:Microsoft.VisualStudio.Shell.Interop.IVsProjectUpgrade.UpgradeProject%2A> çağrısında verilmişse, proje dosyası yükseltme kullanıcıdan gerekir.

     Bir örnek yükseltme istemi iletisi aşağıda verilmiştir:

     "'%1' projesi Visual Studio'nun daha eski bir sürümüyle oluşturuldu. Visual Studio'nun bu sürümü ile açın, Visual Studio'nun eski sürümleriyle açmanız mümkün olmayabilir. Devam etmek ve bu projeyi açmak istiyor musunuz?"

### <a name="to-implement-ivsprojectupgradeviafactory"></a>IVsProjectUpgradeViaFactory uygulamak için

1. Yöntemi uygulamak <xref:Microsoft.VisualStudio.Shell.Interop.IVsProjectUpgradeViaFactory> arabirimi, özellikle <xref:Microsoft.VisualStudio.Shell.Interop.IVsProjectUpgradeViaFactory.UpgradeProject%2A> proje fabrikası uygulamanızda yöntemi veya uygulamaları proje fabrikası uygulamadan çağrılabilir.

2. Açma çözümün bir parçası olarak bir yerinde yükseltme gerçekleştirmek istiyorsanız, bayrak sağlayın <xref:Microsoft.VisualStudio.Shell.Interop.__VSPPROJECTUPGRADEVIAFACTORYFLAGS.PUVFF_SXSBACKUP> olarak `VSPUVF_FLAGS` parametresinde, <xref:Microsoft.VisualStudio.Shell.Interop.IVsProjectUpgradeViaFactory.UpgradeProject%2A> uygulaması.

3. Açma çözümün bir parçası olarak bir yerinde yükseltme gerçekleştirmek istiyorsanız, bayrak sağlayın <xref:Microsoft.VisualStudio.Shell.Interop.__VSPPROJECTUPGRADEVIAFACTORYFLAGS.PUVFF_COPYBACKUP> olarak `VSPUVF_FLAGS` parametresinde, <xref:Microsoft.VisualStudio.Shell.Interop.IVsProjectUpgradeViaFactory.UpgradeProject%2A> uygulaması.

4. Her iki adımları için 2 ve 3 gerçek dosyayı yükseltme adımları kullanarak, <xref:Microsoft.VisualStudio.Shell.Interop.IVsQueryEditQuerySave2>, açıklandığı gibi uygulanabilir "uygulama `IVsProjectUpgade`" aşağıda bölümünde veya gerçek dosya yükseltme devredebilirsiniz <xref:Microsoft.VisualStudio.Shell.Interop.IVsProjectUpgrade>.

5. Yöntemlerini kullanan <xref:Microsoft.VisualStudio.Shell.Interop.IVsUpgradeLogger> iletileri Visual Studio Geçiş Sihirbazı'nı kullanarak kullanıcı için ilgili yükseltme sonrası.

6. <xref:Microsoft.VisualStudio.Shell.Interop.IVsFileUpgrade> arabirimi, her türden proje yükseltmesinin bir parçası gerçekleşmesi dosya yükseltmeyi uygulamak için kullanılır. Bu arabirim, gelen çağrılmaz <xref:Microsoft.VisualStudio.Shell.Interop.IVsProjectUpgradeViaFactory>, ancak proje sistemi, ancak ana proje sisteminin bir parçası olan dosyaları yükseltmek için bir mekanizma doğrudan haberdar olmayabilir olarak sağlanır. Örneğin, dosyaları ve özelliklerini, proje sistemi açıklarsınız aynı geliştirme ekibi tarafından işlenmez derleyici ilgili değilse bu durum meydana gelebilecek.

### <a name="ivsprojectupgrade-implementation"></a>IVsProjectUpgrade uygulama

Proje sisteminizi uyguluyorsa <xref:Microsoft.VisualStudio.Shell.Interop.IVsProjectUpgrade> yalnızca katılabilmesi değil **Visual Studio Dönüştürme Sihirbazı**. Ancak, uygulamanız bile <xref:Microsoft.VisualStudio.Shell.Interop.IVsProjectUpgradeViaFactory> arabirimi, dosya yükseltme hala temsil edebilir <xref:Microsoft.VisualStudio.Shell.Interop.IVsProjectUpgrade> uygulaması.

#### <a name="to-implement-ivsprojectupgrade"></a>IVsProjectUpgrade uygulamak için

1. Bir kullanıcı bir projeyi açmayı denediğinde <xref:Microsoft.VisualStudio.Shell.Interop.IVsProjectUpgrade.UpgradeProject%2A> proje açıldıktan sonra başka bir kullanıcı önce projeye eylemin alınmasından yöntemi ortamı tarafından çağrılır. Kullanıcı zaten çözümünü Yükselt istenirse sonra <xref:Microsoft.VisualStudio.Shell.Interop.__VSUPGRADEPROJFLAGS.UPF_SILENTMIGRATE> bayrağı geçirilir `grfUpgradeFlags` parametresi. Kullanıcı bir proje doğrudan böyle açarsa olarak kullanarak **Varolan Proje Ekle** komutu, ardından <xref:Microsoft.VisualStudio.Shell.Interop.__VSUPGRADEPROJFLAGS.UPF_SILENTMIGRATE> bayrağı geçirilmedi ve projeyi yükseltmek için kullanıcıdan gerekiyor.

2. Yanıt olarak <xref:Microsoft.VisualStudio.Shell.Interop.IVsProjectUpgrade.UpgradeProject%2A> çağrı, proje gerekir değerlendirmek için proje dosyasını yükseltilmiş olup olmadığını. Proje, proje türü yeni bir sürüme yükseltmeniz gerekmez. sonra yalnızca döndürebilir <xref:Microsoft.VisualStudio.VSConstants.S_OK> bayrağı.

3. Projenin proje türü yeni bir sürüme yükseltme gerekiyor sonra proje dosyasını çağırarak değiştirilip değiştirilemeyeceğini belirlemelidir <xref:Microsoft.VisualStudio.Shell.Interop.IVsQueryEditQuerySave2.QueryEditFiles%2A> yöntemi ve değeri geçirme <xref:Microsoft.VisualStudio.Shell.Interop.tagVSQueryEditFlags> için `rgfQueryEdit` parametresi. Proje, ardından aşağıdakileri yapması gerekir:

    - Varsa `VSQueryEditResult` döndürülen değer `pfEditCanceled` parametresi <xref:Microsoft.VisualStudio.Shell.Interop.tagVSQueryEditResult.QER_EditOK>, sonra da proje dosyası yazılabilir olduğundan yükseltme devam.

    - Varsa `VSQueryEditResult` döndürülen değer `pfEditCanceled` parametresi <xref:Microsoft.VisualStudio.Shell.Interop.tagVSQueryEditResult.QER_EditNotOK> ve `VSQueryEditResult` değerine sahip <xref:Microsoft.VisualStudio.Shell.Interop.tagVSQueryEditResultFlags.QER_ReadOnlyNotUnderScc> bit kümesi <xref:Microsoft.VisualStudio.Shell.Interop.IVsProjectUpgrade.UpgradeProject%2A> kullanıcıların izinleri kendilerini sorun gidermeniz gerekir çünkü hatası döndürmesi gerekir. Proje sonra aşağıdakileri yapmanız gerekir:

         Çağırarak hatayı kullanıcıya bildirin <xref:Microsoft.VisualStudio.Shell.Interop.IVsUIShell.ReportErrorInfo%2A> ve dönüş <xref:Microsoft.VisualStudio.Shell.Interop.VSErrorCodes.VS_E_PROJECTMIGRATIONFAILED> hata koduna <xref:Microsoft.VisualStudio.Shell.Interop.IVsProjectUpgrade>.

    - Varsa `VSQueryEditResult` değer <xref:Microsoft.VisualStudio.Shell.Interop.tagVSQueryEditResult.QER_EditNotOK> ve `VSQueryEditResultFlags` değerine sahip <xref:Microsoft.VisualStudio.Shell.Interop.tagVSQueryEditResultFlags.QER_ReadOnlyUnderScc> biti ayarlanmamış, proje dosyasını çağırarak denetlenmesi gerektiğini sonra <xref:Microsoft.VisualStudio.Shell.Interop.IVsQueryEditQuerySave2.QueryEditFiles%2A> (<xref:Microsoft.VisualStudio.Shell.Interop.tagVSQueryEditFlags.QEF_ForceEdit_NoPrompting>, <xref:Microsoft.VisualStudio.Shell.Interop.tagVSQueryEditFlags.QEF_DisallowInMemoryEdits>,...).

4. Varsa <xref:Microsoft.VisualStudio.Shell.Interop.IVsQueryEditQuerySave2.QueryEditFiles%2A> dosya kullanıma alınması ve alınması için en son sürümü proje dosyası çağrıda neden olur ve ardından Proje kaldırılıp yeniden yüklenene. <xref:Microsoft.VisualStudio.Shell.Interop.IVsProjectUpgrade.UpgradeProject%2A> Yöntemi proje başka bir örneği oluşturulduktan sonra tekrar çağrılır. Bu ikinci çağrıda, proje dosyası yazılabilir diske; projeyi önceki biçiminde proje dosyasının bir kopyasını kaydedin önerilir bir. ESKİ uzantısı, yükseltme gerekli değişiklikleri yapın ve yeni biçiminde proje dosyasını kaydedin. Yükseltme işleminin herhangi bir bölümü başarısız olursa yeniden yöntemi hata döndürerek belirtmelidir <xref:Microsoft.VisualStudio.Shell.Interop.VSErrorCodes.VS_E_PROJECTMIGRATIONFAILED>. Bu proje, Çözüm Gezgini'nde kaldırılmasına neden olur.

     Durumda ortamda oluşan tam süreci anlamak önemlidir çağrısı <xref:Microsoft.VisualStudio.Shell.Interop.IVsQueryEditQuerySave2.QueryEditFiles%2A> (sadece rapor değerini belirterek) döner <xref:Microsoft.VisualStudio.Shell.Interop.tagVSQueryEditResult.QER_EditNotOK> ve <xref:Microsoft.VisualStudio.Shell.Interop.tagVSQueryEditResultFlags.QER_ReadOnlyUnderScc> bayrakları.

5. Kullanıcı, proje dosyası açmaya çalışır.

6. Ortam çağrıları, <xref:Microsoft.VisualStudio.Shell.Interop.IVsProjectFactory.CanCreateProject%2A> uygulaması.

7. Varsa <xref:Microsoft.VisualStudio.Shell.Interop.IVsProjectFactory.CanCreateProject%2A> döndürür `true`, sonra ortamı çağrıları, <xref:Microsoft.VisualStudio.Shell.Interop.IVsProjectFactory.CanCreateProject%2A> uygulaması.

8. Ortam çağrıları, <xref:Microsoft.VisualStudio.Shell.Interop.IPersistFileFormat.Load%2A> dosyasını açın ve örneğin, project nesnesini başlatmak için Project1 uygulaması.

9. Ortam çağrıları, `IVsProjectUpgrade::UpgradeProject` proje dosyasının yükseltilmesi gerekip gerekmediğini belirlemek için uygulama.

10. Çağırmanızı <xref:Microsoft.VisualStudio.Shell.Interop.IVsQueryEditQuerySave2.QueryEditFiles%2A> ve bir değer geçirmek <xref:Microsoft.VisualStudio.Shell.Interop.tagVSQueryEditFlags.QEF_ReportOnly> için `rgfQueryEdit` parametresi.

11. Ortam döndürür <xref:Microsoft.VisualStudio.Shell.Interop.tagVSQueryEditResult.QER_EditNotOK> için `VSQueryEditResult` ve <xref:Microsoft.VisualStudio.Shell.Interop.tagVSQueryEditResultFlags.QER_ReadOnlyUnderScc> bitinin ayarlanmasıdır `VSQueryEditResultFlags`.

12. <xref:Microsoft.VisualStudio.Shell.Interop.IVsProjectUpgrade> Uygulama çağrıları `IVsQueryEditQuerySave::QueryEditFiles` (<xref:Microsoft.VisualStudio.Shell.Interop.tagVSQueryEditFlags.QEF_ForceEdit_NoPrompting>, <xref:Microsoft.VisualStudio.Shell.Interop.tagVSQueryEditFlags.QEF_DisallowInMemoryEdits>).

Bu çağrı bir kopyasını kullanıma alınması için proje dosyanızı neden olabilir ve proje dosyanızı yeniden yüklemek için bir gereksinim yanı sıra en son sürümü alınır. Bu noktada, ikisinden biri gerçekleşir:

- Ardından, kendi proje yeniden işlemek, ortam çağırır, <xref:Microsoft.VisualStudio.Shell.Interop.IVsPersistHierarchyItem2.ReloadItem%2A> (VSITEMID_ROOT) uygulama. Bu çağrı aldığında, projenize (Project1) ilk örneğinin yeniden yüklemeniz ve proje dosyanız yükseltmeye devam edin. Ortam döndürürse, kendi proje yeniden işlemek bilir `true` için <xref:Microsoft.VisualStudio.Shell.Interop.IVsHierarchy.GetProperty%2A> (<xref:Microsoft.VisualStudio.Shell.Interop.__VSHPROPID.VSHPROPID_HandlesOwnReload>).

- Kendi proje yeniden işlememesi sonra iade ettiğiniz `false` için <xref:Microsoft.VisualStudio.Shell.Interop.IVsHierarchy.GetProperty%2A> (<xref:Microsoft.VisualStudio.Shell.Interop.__VSHPROPID.VSHPROPID_HandlesOwnReload>). Bu durumda, önce <xref:Microsoft.VisualStudio.Shell.Interop.IVsQueryEditQuerySave2.QueryEditFiles%2A>(QEF_ForceEdit_NoPrompting, QEF_DisallowInMemoryEdits) ortamı oluşturur Örneğin, Project2 projeniz başka bir yeni örneğini gibi döndürür:

    1. Ortam çağrıları <xref:Microsoft.VisualStudio.Shell.Interop.IVsHierarchy.Close%2A> ilk proje nesneniz üzerinde Project1, bu nedenle etkin olmayan bir durumda bu nesne yerleştirme.

    2. Ortam çağrıları, `IVsProjectFactory::CreateProject` Project2 projenizi ikinci bir örneğini oluşturmak için uygulama.

    3. Ortam çağrıları, `IPersistFileFormat::Load` uygulama dosyasını açın ve Project2 ikinci project nesnesini başlatır.

    4. Ortam çağrıları `IVsProjectUpgrade::UpgradeProject` project nesnesini yükseltilmesi olup olmadığını belirlemek ikinci bir kez. Ancak, bu çağrı yeni, ikinci projesi Project2 örneğini yapılır. Bu çözümde açık projedir.

        > [!NOTE]
        > İlk projenizi, Project1, etkin olmayan duruma yerleştirilir ve ardından döndürmesi gereken örneğinde <xref:Microsoft.VisualStudio.VSConstants.S_OK> ilk çağrısından, <xref:Microsoft.VisualStudio.Shell.Interop.IVsProjectUpgrade.UpgradeProject%2A> uygulaması.

    5. Çağırmanızı <xref:Microsoft.VisualStudio.Shell.Interop.IVsQueryEditQuerySave2.QueryEditFiles%2A> ve bir değer geçirmek <xref:Microsoft.VisualStudio.Shell.Interop.tagVSQueryEditFlags.QEF_ReportOnly> için `rgfQueryEdit` parametresi.

    6. Ortam döndürür <xref:Microsoft.VisualStudio.Shell.Interop.tagVSQueryEditResult.QER_EditOK> ve proje dosyasının yazılabilir olduğundan yükseltme devam.

Yükseltme başarısız olursa, dönüş <xref:Microsoft.VisualStudio.Shell.Interop.VSErrorCodes.VS_E_PROJECTMIGRATIONFAILED> gelen `IVsProjectUpgrade::UpgradeProject`. Yükseltme gerekli olan veya yükseltme, kabul için seçtiğiniz `IVsProjectUpgrade::UpgradeProject` bir İşlemsiz çağırın. Size dönüş yaparsa <xref:Microsoft.VisualStudio.Shell.Interop.VSErrorCodes.VS_E_PROJECTMIGRATIONFAILED>, çözüm projeniz için bir yer tutucu düğümünün eklenir.

## <a name="upgrading-project-items"></a>Proje öğeleri yükseltme

Ekler veya öğeleri uygulamaz proje sistemleri içinde yönetmek, proje yükseltme işlemine katılmasını gerekebilir. Crystal Reports, proje sistemi için eklenebilir bir öğenin bir örnektir.

Genellikle, proje öğesi uygulayıcılar hangi proje başvuruları ve diğer proje özellikleri var. bir yükseltme kararı vermeniz nelerdir bilmesi gerektiğinden proje zaten tam olarak oluşturulmuş ve yükseltilen yararlanmak isteyen.

### <a name="to-get-the-project-upgrade-notification"></a>Proje yükseltme bildirim almak için

1. Ayarlama <xref:Microsoft.VisualStudio.Shell.Interop.UIContextGuids80.SolutionOrProjectUpgrading> proje öğesi uygulamanızda bayrağı (vsshell80.idl içinde tanımlanmıştır). Visual Studio Kabuğu, proje sistemi yükseltme sürecinde olduğunu belirlediğinde, bu proje öğenizin VSPackage otomatik yük neden olur.

2. Öneri <xref:Microsoft.VisualStudio.Shell.Interop.IVsSolutionEventsProjectUpgrade> aracılığıyla arabirim <xref:Microsoft.VisualStudio.Shell.Interop.IVsSolution2.AdviseSolutionEvents%2A> yöntemi.

3. <xref:Microsoft.VisualStudio.Shell.Interop.IVsSolutionEventsProjectUpgrade> Arabirimi, proje sistemi uygulama yükseltme işlemlerini tamamladı ve yeni yükseltilen proje oluşturulduktan sonra tetiklenir. Senaryoya bağlı olarak <xref:Microsoft.VisualStudio.Shell.Interop.IVsSolutionEventsProjectUpgrade> arabirimi sonra tetiklenir <xref:Microsoft.VisualStudio.Shell.Interop.IVsSolutionEvents3.OnAfterOpenSolution%2A>, <xref:Microsoft.VisualStudio.Shell.Interop.IVsSolutionEvents3.OnAfterOpenProject%2A>, veya <xref:Microsoft.VisualStudio.Shell.Interop.IVsSolutionEvents3.OnAfterLoadProject%2A> yöntemleri.

### <a name="to-upgrade-the-project-item-files"></a>Proje öğesi dosyaları yükseltmek için

1. Proje öğesi uygulamanızda dosya yedekleme işlemi dikkatle yönetmeniz gerekir. Yan yana yedeklemesi için bu özellikle geçerlidir burada `fUpgradeFlag` parametresinin <xref:Microsoft.VisualStudio.Shell.Interop.IVsProjectUpgradeViaFactory.UpgradeProject%2A> yöntemi ayarlandığında <xref:Microsoft.VisualStudio.Shell.Interop.__VSPPROJECTUPGRADEVIAFACTORYFLAGS.PUVFF_SXSBACKUP>, "eski" belirlenmiş dosyalarını boyunca yedeklenmiş dosyaları yerleştirildiği. Proje zaman yükseltildi sistem saatinden daha önce Yedeklenen dosyaların eski belirlenebilir. Ayrıca, bunu önlemek için belirli adımlar sürece, yazılabilir.

2. Zaman, proje öğesi proje yükseltme bir bildirim alır. **Visual Studio Dönüştürme Sihirbazı** gösterilmeye devam eder. Bu nedenle, yöntemlerini kullanmanız gerekir <xref:Microsoft.VisualStudio.Shell.Interop.IVsUpgradeLogger> arabirimi yükseltme iletileri Sihirbazı kullanıcı Arabirimi sağlar.

## <a name="see-also"></a>Ayrıca bkz.

- [Projeler](../../extensibility/internals/projects.md)
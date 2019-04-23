---
title: Projeleri yükseltme | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-sdk
ms.topic: conceptual
helpviewer_keywords:
- upgrading VSPackages
- upgrading applications, strategies
- VSPackages, upgrade support
ms.assetid: e01cb44a-8105-4cf4-8223-dfae65f8597a
caps.latest.revision: 13
ms.author: gregvanl
manager: jillfra
ms.openlocfilehash: 7e97e21b2d08d7398a4372ac31cda63b5cfb9fe9
ms.sourcegitcommit: 1fc6ee928733e61a1f42782f832ead9f7946d00c
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/22/2019
ms.locfileid: "60100605"
---
# <a name="upgrading-projects"></a>Projeleri Yükseltme
[!INCLUDE[vs2017banner](../../includes/vs2017banner.md)]

Proje modeli için bir sürümünden değişiklikleri [!INCLUDE[vsprvs](../../includes/vsprvs-md.md)] sonraki sürüme üzerinde çalıştırabilmeniz için projeler ve çözümler yükseltilmesi özellikle gerektirebilir. [!INCLUDE[vsipsdk](../../includes/vsipsdk-md.md)] Yükseltme desteği kendi projelerinde uygulamak için kullanılan arabirimleri sağlar.  
  
## <a name="upgrade-strategies"></a>Yükseltme stratejileri  
 Yükseltme desteklemek için proje sistemi uygulamanızı tanımlamak ve yükseltme bir strateji yürütmelidir. Stratejinizi belirlemede yan yana (SxS) yedekleme, kopya yedekleme veya her ikisini de desteklemek seçebilirsiniz.  
  
- SxS yedekleme, bir proje bir yerde, uygun dosya adı sonek, örneğin, ekleme "eski" Yükseltme gereken dosyaları kopyalar anlamına gelir.  
  
- Kopya yedekleme, bir projenin tüm proje öğeleri kullanıcı tarafından sağlanan bir yedek konumuna kopyalar anlamına gelir. Ardından, özgün proje konumda sürücülerinizdeki ilgili dosyaların yükseltilir.  
  
## <a name="how-upgrade-works"></a>Yükseltme nasıl çalışır?  
 Bir önceki sürümünde oluşturulmuş bir çözümü, [!INCLUDE[vsprvs](../../includes/vsprvs-md.md)] , çözüm dosya yükseltilmesi gerekip gerekmediğini belirlemek için IDE denetimleri gibi daha yeni bir sürümü açılır. Yükseltme gerekli ise **Yükseltme Sihirbazı** kullanıcı yükseltme sürecinde size yol için otomatik olarak başlatılır.  
  
 Bir çözüm yükseltme gerektiğinde, her proje fabrikası yükseltme stratejisinin için sorgular. Strateji, proje fabrikası kopya yedekleme veya SxS yedekleme destekleyip desteklemediğini belirler. Bilgiler gönderilir **Yükseltme Sihirbazı**, yedekleme için gerekli bilgileri toplar ve kullanıcıya uygun bir seçenek sunar.  
  
### <a name="multi-project-solutions"></a>Birden çok proje çözümü  
 Varsa bir çözüm birden fazla proje içeren ve yükseltme stratejiler farklı gibi yalnızca SxS yedekleme destekleyen bir C++ projesi ve yalnızca kopya yedeği destekleyen bir Web projesi, proje fabrikalarını yükseltme stratejisini anlaşmaları gerekir.  
  
 Her proje fabrikası için çözüm sorgular <xref:Microsoft.VisualStudio.Shell.Interop.IVsProjectUpgradeViaFactory>. Ardından <xref:Microsoft.VisualStudio.Shell.Interop.IVsProjectUpgradeViaFactory.UpgradeProject_CheckOnly%2A> genel proje dosyalarını yükseltme gerekip gerekmediğini ve desteklenen yükseltme stratejiler belirlemek için. **Yükseltme Sihirbazı** sonra çağrılır.  
  
 Kullanıcı, sihirbaz tamamlandıktan sonra <xref:Microsoft.VisualStudio.Shell.Interop.IVsProjectUpgradeViaFactory.UpgradeProject%2A> gerçek yükseltmeyi gerçekleştirmek için her proje fabrikası çağrılır. Yedekleme kolaylaştırmak için IVsProjectUpgradeViaFactory yöntemleri sağlayan <xref:Microsoft.VisualStudio.Shell.Interop.SVsUpgradeLogger> yükseltme işleminin ayrıntılarını oturum hizmeti. Bu hizmet önbelleğe alınamaz.  
  
 Tüm ilgili genel dosyaları güncelleştirdikten sonra her proje fabrikası, bir proje oluşturmak seçebilirsiniz. Proje uygulama desteklemelidir <xref:Microsoft.VisualStudio.Shell.Interop.IVsProjectUpgrade>. <xref:Microsoft.VisualStudio.Shell.Interop.IVsProjectUpgrade.UpgradeProject%2A> Yöntemi tüm ilgili proje öğeleri yükseltmek sonra çağrılır.  
  
> [!NOTE]
>  <xref:Microsoft.VisualStudio.Shell.Interop.IVsProjectUpgradeViaFactory.UpgradeProject%2A> Yöntemi SVsUpgradeLogger hizmet sağlamaz. Bu hizmet, çağrılarak alınabilir <xref:Microsoft.VisualStudio.OLE.Interop.IServiceProvider.QueryService%2A>.  
  
## <a name="best-practices"></a>En İyi Yöntemler  
 Kullanım <xref:Microsoft.VisualStudio.Shell.Interop.SVsQueryEditQuerySave> hizmetinin, bir dosya düzenlemeden önce düzenleyebilir ve kaydetmeden önce kaydedebilirsiniz olmadığını denetleyin. Bu yedekleme yardımcı olur ve yükseltme uygulamaları işlemek için kaynak denetimi altında proje dosyaları, dosyaları yetersiz izinler ve benzeri.  
  
 Kullanım <xref:Microsoft.VisualStudio.Shell.Interop.SVsUpgradeLogger> hizmet yedekleme tüm aşamalarında ve başarı veya başarısızlık yükseltme işleminin bilgi sağlamak için yükseltin.  
  
 Yedekleme ve projelerini yükseltme hakkında daha fazla bilgi için içinde vsshell2.idl IVsProjectUpgrade için yorumlara bakın.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Projeleri](../../extensibility/internals/projects.md)   
 [Özel projelerini yükseltme](../../misc/upgrading-custom-projects.md)   
 [Proje öğeleri yükseltme](../../misc/upgrading-project-items.md)

---
title: Proje yapı yapılandırmasını | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-sdk
ms.topic: conceptual
helpviewer_keywords:
- projects [Visual Studio SDK], configuration for building
- project configurations, building
ms.assetid: 2c83615d-fa4d-4b9f-b315-7a69b3000da0
caps.latest.revision: 12
ms.author: gregvanl
manager: jillfra
ms.openlocfilehash: 99d9e20799f3747def12be6a40ae3b1f8269e666
ms.sourcegitcommit: 8b538eea125241e9d6d8b7297b72a66faa9a4a47
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54760985"
---
# <a name="project-configuration-for-building"></a>Derleme için Proje Yapılandırması
[!INCLUDE[vs2017banner](../../includes/vs2017banner.md)]

Belirli bir çözüm için çözüm yapılandırmaları listesi çözüm yapılandırmaları iletişim kutusu tarafından yönetilir.  
  
 Ek çözüm yapılandırmalarının her biri kendi benzersiz bir ada sahip bir kullanıcı oluşturabilirsiniz. Kullanıcı yeni bir çözüm yapılandırması oluşturduğunda, karşılık gelen ad varsa IDE projeleri veya hata ayıklama karşılık gelen yapılandırma adı olur. Kullanıcı Seçimi gerekirse belirli gereksinimleri karşılayacak şekilde değiştirebilirsiniz. Bu davranışı tek istisnası, projeye yeni çözüm yapılandırması adıyla eşleşen bir yapılandırma destekler andır. Örneğin, bir çözüm Project1 ve Project2 içerdiğini varsayalım. Proje yapılandırması hata ayıklama, perakende ve MyConfig1 Project1 sahiptir. Proje yapılandırması hata ayıklama, perakende ve MyConfig2 Project2 sahiptir.  
  
 Kullanıcı MyConfig2 adlı yeni bir çözüm yapılandırması oluşturursa, Project1 için çözüm yapılandırması hata ayıklama yapılandırmasını varsayılan olarak bağlar. Project2 ayrıca MyConfig2 yapılandırmasıyla çözüm yapılandırması için varsayılan olarak bağlar.  
  
> [!NOTE]
>  Bağlama büyük/küçük harfe duyarsızdır.  
  
 Kullanıcı seçtiğinde **çoklu seçim** öğesi yapılandırma aşağı açılan listeden ortamı kullanılabilir yapılandırmaların listesi sunan bir iletişim kutusu görüntüler.  
  
 ![Birden çok yapılandırma](../../extensibility/internals/media/vsmultiplecfgs.gif "vsMultipleCfgs")  
Birden çok yapılandırma  
  
 Bu iletişim kutusu içinde bir veya birden fazla Yapılandırması kullanıcı seçebilirsiniz. Sonra seçili yapılandırmalar için değerlerinin kesişimini özellik sayfaları iletişim kutusu üzerinde görüntülenen özellik değerleri yansıtır.  
  
 Bkz: [çözüm yapılandırması](../../extensibility/internals/solution-configuration.md) ekleme ve çözümler ve projeler için yapılandırmaları yeniden adlandırma ile ilgili bilgi için.  
  
 Proje bağımlılıkları ve derleme sırası olan bağımsız bir çözüm yapılandırması: diğer bir deyişle, yalnızca tüm Çözümdeki projeler için bir bağımlılık ağacı ayarlayabilirsiniz. Çözüm veya projeyi sağ tıklayıp ya da **proje bağımlılıkları** veya **Proje yapı siparişi** açılır seçenek **proje bağımlılıkları** iletişim kutusu. Gelen de açılabilir **proje** menüsü.  
  
 ![Proje bağımlılıkları](../../extensibility/internals/media/vsprojdependencies.gif "vsProjDependencies")  
Proje bağımlılıkları  
  
 Proje bağımlılıkları, Proje yapı sırasını belirler. Derleme sırası sekmesini iletişim kutusunda, bir çözüm içindeki projelerin derleme ve yapılandırma sırasını değiştirmek için bağımlılıklar sekmesini kullanın tam sırayı görüntülemek için kullanın.  
  
> [!NOTE]
>  Tarafından belirtilen özel bağımlılıklar nedeniyle ortama göre kendi onay kutularını seçili ancak gri görünüyorsa projeleri listesinde eklenmiştir <xref:Microsoft.VisualStudio.Shell.Interop.IVsBuildDependency> veya <xref:Microsoft.VisualStudio.Shell.Interop.IVsDeployDependency> arabirimleri ve değiştirilemez. Örneğin, bir proje başvuru ekleyerek bir [!INCLUDE[vbprvb](../../includes/vbprvb-md.md)] proje başka bir projeye başvuru silerek yalnızca kaldırılabilir bir derleme bağımlılığı otomatik olarak ekler. Bunun yapılması bir bağımlılık döngüsü oluşturabileceğinden projeleri olan onay kutularını temizleyin ve gri görünüyorsa seçilemez (örneğin, Project1 Project2 bağımlı olacaktır ve Project2 Project1 bağımlı olur), hangi derleme kabin.  
  
 [!INCLUDE[vsprvs](../../includes/vsprvs-md.md)] Yapı işlemleri tipik derleme ve tek bir derleme komutla çağrılan bağlantı işlemlerini içerir. Diğer iki yapı işlemlerini de desteklenebilir: önceki bir yapıdan ve bir çıkış öğesi yapılandırmasında değişip değişmediğini belirlemek için bir güncellik denetimi tüm çıkış öğelerini silmek için temizleme işlemi.  
  
 <xref:Microsoft.VisualStudio.Shell.Interop.IVsProjectCfg2> nesneler döndürmeye karşılık gelen <xref:Microsoft.VisualStudio.Shell.Interop.IVsBuildableProjectCfg> (döndürüldüğü <xref:Microsoft.VisualStudio.Shell.Interop.IVsProjectCfg2.get_CfgType%2A>) yapı işlemlerini yönetmek için. Yapılandırmalar, gerçekleştirildiği sırada bir yapı işleminin durumunu bildirmek için çağrı yapmak <xref:Microsoft.VisualStudio.Shell.Interop.IVsBuildStatusCallback>, arabirimin uygulanan ortamı tarafından ve herhangi bir nesne derleme durumu olayları ilgileniyor.  
  
 Bir kez oluşturulduktan sonra yapılandırma ayarları hata ayıklayıcının denetiminin altında çalıştırılabilir olup olmadığını belirlemek için kullanılabilir. Yapılandırmalar uygulamanız <xref:Microsoft.VisualStudio.Shell.Interop.IVsDebuggableProjectCfg> hata ayıklamayı desteklemek için.  
  
 Proje bağımlılıkları uyguladıktan sonra otomasyon modeli aracılığıyla bağımlılıkları programlı olarak yönetebilirsiniz. Çağırmanızı <xref:EnvDTE.SolutionBuild.BuildDependencies%2A> otomasyon modeli. Çözüm derleme Yöneticisi yapılandırmaları ve özellikleri doğrudan işlemeye izin kullanılabilir VSIP API düzeyi arabirimlerine yok.  
  
 Ayrıca, proje bağımlılıkları penceresinde bir kılavuz sağlar. Daha fazla bilgi için [özellikler görüntü Kılavuzu](../../extensibility/internals/properties-display-grid.md).  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Yapılandırma seçeneklerini yönetme](../../extensibility/internals/managing-configuration-options.md)   
 [Dağıtımı yönetmek için proje yapılandırması](../../extensibility/internals/project-configuration-for-managing-deployment.md)   
 [Çıkış için Proje Yapılandırması](../../extensibility/internals/project-configuration-for-output.md)

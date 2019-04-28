---
title: Çözümlere genel bakış | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-sdk
ms.topic: conceptual
helpviewer_keywords:
- solutions, about solutions
ms.assetid: 3b21e3a1-170a-4485-941e-6b04b7b27886
caps.latest.revision: 11
ms.author: gregvanl
manager: jillfra
ms.openlocfilehash: fb3bb85ab172404262c147cce285cebaf756afc9
ms.sourcegitcommit: 47eeeeadd84c879636e9d48747b615de69384356
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "63432077"
---
# <a name="solutions-overview"></a>Çözümlere Genel Bakış
[!INCLUDE[vs2017banner](../../includes/vs2017banner.md)]

Bir çözümü, bir uygulama oluşturmak için birlikte çalışan bir veya daha fazla proje gruplandırmasıdır. Çözüme ilişkin proje ve durum bilgilerini iki farklı çözümü dosyalarında depolanır. Çözüm (.sln) dosyasını metin tabanlı kaynak kodu denetimi altında yerleştirilmiş ve kullanıcılar arasında paylaşılan. Çözüm kullanıcı seçeneği (.suo) ikili dosyadır. Sonuç olarak, .suo dosya kaynak kodu denetimi altında yerleştirilmiş ve kullanıcıya özgü bilgileri içerir.  
  
 Her iki çözüm dosya türünün herhangi bir VSPackage yazabilirsiniz. Dosya yapısı nedeniyle, kendisine yazmak için uygulanan iki farklı arabirimi vardır. <xref:Microsoft.VisualStudio.Shell.Interop.IVsPersistSolutionProps> Arabirimi .sln dosyasına metin bilgi yazar ve <xref:Microsoft.VisualStudio.Shell.Interop.IVsPersistSolutionOpts> arabirimi ikili akışlar .suo dosyasına yazar.  
  
> [!NOTE]
> Bir proje açıkça bir giriş kendisi için çözüm dosyasına yazmak zorunda değildir; ortam, proje için işler. Bu nedenle, ek içeriği özellikle çözüm dosyasına eklemek istediğiniz sürece, bu şekilde, VSPackage kaydetme gerekmez.  
  
 Çözüm Kalıcılık destekleyen her bir VSPackage üç arabirimi kullanan <xref:Microsoft.VisualStudio.Shell.Interop.IVsSolutionPersistence> ortamı tarafından uygulanan ve VSPackage'ı tarafından çağrılır, arabirimi ve `IVsPersistSolutionProps` ve `IVsPersistSolutionOpts`, uygulanan hem de bir işlem olan VSPackage'ı. `IVsPersistSolutionOpts` Arabirimi yalnızca gereken gizli bilgileri tarafından VSPackage .suo dosyasına yazılması ise uygulanacak.  
  
 Bir çözümü açtığınızda, aşağıdaki süreç gerçekleşir.  
  
1. Ortam çözümü okur.  
  
2. Ortam bulursa bir `CLSID`, karşılık gelen VSPackage'ı yükler.  
  
3. VSPackage yüklendiği varsa, ortam çağrıları `QueryInterface` için <xref:Microsoft.VisualStudio.Shell.Interop.IVsPackage> VSPackage gerektiren arabirimi için bir arabirim.  
  
   1. Bir .sln dosyasından okurken, ortam çağırır `QueryInterface` için `IVsPersistSolutionProps`.  
  
   2. Bir .suo dosyasından okurken, ortam çağırır `QueryInterface` için `IVsPersistSolutionOpts`.  
  
   Bu dosyaların kullanımıyla ilgili belirli bilgileri bulunabilir [çözüm (. Sln) dosya](../../extensibility/internals/solution-dot-sln-file.md) ve [çözüm kullanıcı seçenekleri (. Suo) dosyası](../../extensibility/internals/solution-user-options-dot-suo-file.md).  
  
> [!NOTE]
> İki proje yapılandırmalarını oluşan ve üçüncü bir derlemeden hariç olmak üzere yeni bir çözüm yapılandırması oluşturmak istiyorsanız, otomasyon ve özellik sayfaları kullanıcı arabirimini kullanmanız gerekir. Çözüm yapı yöneticisi yapılandırmaları ve özellikleri doğrudan değiştiremezsiniz, ancak çözüm derleme Yöneticisi kullanarak işleyebileceğiniz `SolutionBuild` DTE sınıfında otomasyon modeli. Çözümleri yapılandırma hakkında daha fazla bilgi için bkz. [çözüm yapılandırması](../../extensibility/internals/solution-configuration.md).  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 <xref:Microsoft.VisualStudio.Shell.Interop.IVsPackage>   
 <xref:Microsoft.VisualStudio.Shell.Interop.IVsPersistSolutionOpts>   
 <xref:Microsoft.VisualStudio.Shell.Interop.IVsPersistSolutionProps>   
 <xref:Microsoft.VisualStudio.Shell.Interop.IVsSolutionPersistence>

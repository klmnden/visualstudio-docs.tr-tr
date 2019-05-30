---
title: Çözümlere genel bakış
ms.date: 11/04/2016
ms.topic: conceptual
helpviewer_keywords:
- solutions, about solutions
ms.assetid: 3b21e3a1-170a-4485-941e-6b04b7b27886
author: madskristensen
ms.author: madsk
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: 9405177e193349eeb6e7767b70af0ef82208cc4c
ms.sourcegitcommit: 40d612240dc5bea418cd27fdacdf85ea177e2df3
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/29/2019
ms.locfileid: "66322600"
---
# <a name="solutions-overview"></a>Çözümlere genel bakış

Bir çözümü, bir uygulama oluşturmak için birlikte çalışan bir veya daha fazla proje gruplandırmasıdır. Çözüme ilişkin proje ve durum bilgilerini iki farklı çözümü dosyalarında depolanır. [Çözüm (.sln) dosyasını](solution-dot-sln-file.md) metin tabanlı kaynak kodu denetimi altında yerleştirilmiş ve kullanıcılar arasında paylaşılan. [Çözüm kullanıcı seçeneği (.suo) dosyası](solution-user-options-dot-suo-file.md) ikili. Sonuç olarak, .suo dosya kaynak kodu denetimi altında yerleştirilmiş ve kullanıcıya özgü bilgileri içerir.

Her iki çözüm dosya türünün herhangi bir VSPackage yazabilirsiniz. Dosya yapısı nedeniyle, kendisine yazmak için uygulanan iki farklı arabirimi vardır. <xref:Microsoft.VisualStudio.Shell.Interop.IVsPersistSolutionProps> Arabirimi .sln dosyasına metin bilgi yazar ve <xref:Microsoft.VisualStudio.Shell.Interop.IVsPersistSolutionOpts> arabirimi ikili akışlar .suo dosyasına yazar.

> [!NOTE]
> Bir proje açıkça bir giriş kendisi için çözüm dosyasına yazmak zorunda değildir; ortam, proje için işler. Bu nedenle, ek içeriği özellikle çözüm dosyasına eklemek istediğiniz sürece, bu şekilde, VSPackage kaydetme gerekmez.

Çözüm Kalıcılık destekleyen her bir VSPackage üç arabirimi kullanan <xref:Microsoft.VisualStudio.Shell.Interop.IVsSolutionPersistence> ortamı tarafından uygulanan ve VSPackage'ı tarafından çağrılır, arabirimi ve `IVsPersistSolutionProps` ve `IVsPersistSolutionOpts`, uygulanan hem de bir işlem olan VSPackage'ı. `IVsPersistSolutionOpts` Arabirimi yalnızca gereken gizli bilgileri tarafından VSPackage .suo dosyasına yazılması ise uygulanacak.

Bir çözümü açtığınızda, aşağıdaki süreç gerçekleşir.

1. Ortam çözümü okur.

2. Ortam bulursa bir `CLSID`, karşılık gelen VSPackage'ı yükler.

3. VSPackage yüklendiği varsa, ortam çağrıları `QueryInterface` için <xref:Microsoft.VisualStudio.Shell.Interop.IVsPackage> VSPackage gerektiren arabirimi için arabirim.

   - Bir .sln dosyasından okurken, ortam çağırır `QueryInterface` için `IVsPersistSolutionProps`.

   - Bir .suo dosyasından okurken, ortam çağırır `QueryInterface` için `IVsPersistSolutionOpts`.

   Bu dosyaların kullanımıyla ilgili belirli bilgileri bulunabilir [çözüm (. Sln) dosya](../../extensibility/internals/solution-dot-sln-file.md) ve [çözüm kullanıcı seçenekleri (. Suo) dosyası](../../extensibility/internals/solution-user-options-dot-suo-file.md).

> [!NOTE]
> İki proje yapılandırmalarını oluşan ve üçüncü bir derlemeden hariç olmak üzere yeni bir çözüm yapılandırması oluşturmak istiyorsanız, otomasyon ve özellik sayfaları kullanıcı arabirimini kullanmanız gerekir. Çözüm yapı yöneticisi yapılandırmaları ve özellikleri doğrudan değiştiremezsiniz, ancak çözüm derleme Yöneticisi kullanarak işleyebileceğiniz `SolutionBuild` DTE sınıfında otomasyon modeli. Çözümleri yapılandırma hakkında daha fazla bilgi için bkz. [çözüm yapılandırması](../../extensibility/internals/solution-configuration.md).

## <a name="see-also"></a>Ayrıca bkz.

- <xref:Microsoft.VisualStudio.Shell.Interop.IVsPackage>
- <xref:Microsoft.VisualStudio.Shell.Interop.IVsPersistSolutionOpts>
- <xref:Microsoft.VisualStudio.Shell.Interop.IVsPersistSolutionProps>
- <xref:Microsoft.VisualStudio.Shell.Interop.IVsSolutionPersistence>
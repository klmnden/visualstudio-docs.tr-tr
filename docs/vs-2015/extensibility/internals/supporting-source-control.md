---
title: Kaynak denetimini destekleme | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-sdk
ms.topic: conceptual
helpviewer_keywords:
- source control [Visual Studio SDK], supporting
ms.assetid: 567acde3-354e-4f39-8d99-0ef86c103396
caps.latest.revision: 19
ms.author: gregvanl
manager: jillfra
ms.openlocfilehash: d1166197a5c79dcb0d1ddf4018227914346a6172
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "68156068"
---
# <a name="supporting-source-control"></a>Kaynak Denetimini Destekleme
[!INCLUDE[vs2017banner](../../includes/vs2017banner.md)]

[!INCLUDE[vsprvs](../../includes/vsprvs-md.md)] Dosya kullanıma alma, iade etme işlemleri ve diğer kaynak denetim işlemlerini Proje veya Düzenleyicisi için destekler. Kaynak denetimi istemci olarak [!INCLUDE[vsprvs](../../includes/vsprvs-md.md)] gibi kaynak denetim paketi ile etkileşim kuracak şekilde tasarlanmıştır [!INCLUDE[vsvss](../../includes/vsvss-md.md)], arşivleme, sürüm oluşturma ve denetim özellikleri için dinamik olarak tanımlanan bir dosya kümesini sağlar.  
  
## <a name="in-this-section"></a>Bu Bölümde  
 [Kaynak Denetimi Paketleri için Model](../../extensibility/internals/model-for-source-control-packages.md)  
 Bir proje türü uygulanmalı arabirimleri açıklar kaynak denetimi desteklemek için.  
  
 [Tasarım Kararları](../../extensibility/internals/source-control-design-decisions.md)  
 Soruların yanıtlarını proje türüne nasıl uygulayacağınıza değiştirme sağlar.  
  
 [Yapılandırma Ayrıntıları](../../extensibility/internals/source-control-configuration-details.md)  
 Kaynak denetimini destekleyen bir proje türü uygulamasını nasıl değiştiğini açıklar.  
  
 [Projeler ve Düzenleyiciler için Ek Yönergeler](../../extensibility/internals/additional-source-control-guidelines-for-projects-and-editors.md)  
 Proje türleri ve düzenleyiciler için en iyi uygulamaları açıklar.  
  
 [Çalışma Zamanı Ayrıntıları](../../extensibility/internals/source-control-runtime-details.md)  
 Bir kullanıcı, bir kaynak denetim sistemine eklediğinde, bir proje kaydetme işlemini açıklamaktadır.  
  
## <a name="reference"></a>Başvuru  
 <xref:Microsoft.VisualStudio.Shell.Interop.IVsQueryEditQuerySave2>  
 Ortam ya da bir dosya hakkında bellekte değiştirilemez veya kaydedilmiş olan kaynak denetim paketi belirtir.  
  
 <xref:Microsoft.VisualStudio.Shell.Interop.IVsSccManager2>  
 Projeler ve hiyerarşileri kendilerini kaynak denetimiyle kaydetmesini ve kaynak denetimi durumu hakkında bilgi sağlar.  
  
 <xref:Microsoft.VisualStudio.Shell.Interop.IVsSccProject2>  
 Kaynak denetimi proje dosyaları ve proje öğeleri için sağlamak üzere proje sistemindeki uygulanır.  
  
 <xref:Microsoft.VisualStudio.Shell.Interop.IVsTrackProjectDocuments2>  
 Ortam eklemek, kaldırmak veya bir dosya veya bir çözüm dizini yeniden adlandırma izni için Sorgulanacak projeleri tarafından kullanılır.  
  
 <xref:Microsoft.VisualStudio.Shell.Interop.IVsTrackProjectDocumentsEvents2>  
 Proje dosyaları veya dizinleri için yapılan değişiklikler istemcileri bildirir.  
  
## <a name="related-sections"></a>İlgili Bölümler  
 [Proje Türleri](../../extensibility/internals/project-types.md)  
 Temel yapı taşları projelerine genel bir bakış sağlar [!INCLUDE[vsprvs](../../includes/vsprvs-md.md)] tümleşik geliştirme ortamı (IDE). Projeler oluşturmak ve kodu derleme nasıl kontrol açıklayan ek konulara bağlantılar sağlanmaktadır.

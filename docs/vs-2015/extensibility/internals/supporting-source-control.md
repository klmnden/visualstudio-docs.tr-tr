---
title: Kaynak denetimini destekleme | Microsoft Docs
ms.custom: ''
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.reviewer: ''
ms.suite: ''
ms.technology:
- vs-ide-sdk
ms.tgt_pltfrm: ''
ms.topic: article
helpviewer_keywords:
- source control [Visual Studio SDK], supporting
ms.assetid: 567acde3-354e-4f39-8d99-0ef86c103396
caps.latest.revision: 19
ms.author: gregvanl
manager: ghogen
ms.openlocfilehash: 12a7cb2de6f3710f7b9e608f008d72d3b0b0e777
ms.sourcegitcommit: 9ceaf69568d61023868ced59108ae4dd46f720ab
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/12/2018
ms.locfileid: "49279584"
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


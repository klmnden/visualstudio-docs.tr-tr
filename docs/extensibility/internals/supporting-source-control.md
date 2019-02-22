---
title: Kaynak denetimini destekleme | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
helpviewer_keywords:
- source control [Visual Studio SDK], supporting
ms.assetid: 567acde3-354e-4f39-8d99-0ef86c103396
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: 35fb66927272435e773dbaee44019103892b028d
ms.sourcegitcommit: d0425b6b7d4b99e17ca6ac0671282bc718f80910
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/21/2019
ms.locfileid: "56616995"
---
# <a name="supporting-source-control"></a>Kaynak Denetimini Destekleme
[!INCLUDE[vsprvs](../../code-quality/includes/vsprvs_md.md)] Dosya kullanıma alma, iade etme işlemleri ve diğer kaynak denetim işlemlerini Proje veya Düzenleyicisi için destekler. Kaynak denetimi istemci olarak [!INCLUDE[vsprvs](../../code-quality/includes/vsprvs_md.md)] gibi kaynak denetim paketi ile etkileşim kuracak şekilde tasarlanmıştır [!INCLUDE[vsvss](../../extensibility/includes/vsvss_md.md)], arşivleme, sürüm oluşturma ve denetim özellikleri için dinamik olarak tanımlanan bir dosya kümesini sağlar.

## <a name="in-this-section"></a>Bu Bölümde
- [Kaynak Denetimi Paketleri için Model](../../extensibility/internals/model-for-source-control-packages.md)

 Bir proje türü uygulanmalı arabirimleri açıklar kaynak denetimi desteklemek için.

- [Tasarım Kararları](../../extensibility/internals/source-control-design-decisions.md)

 Soruların yanıtlarını proje türüne nasıl uygulayacağınıza değiştirme sağlar.

- [Yapılandırma Ayrıntıları](../../extensibility/internals/source-control-configuration-details.md)

 Kaynak denetimini destekleyen bir proje türü uygulamasını nasıl değiştiğini açıklar.

- [Projeler ve Düzenleyiciler için Ek Yönergeler](../../extensibility/internals/additional-source-control-guidelines-for-projects-and-editors.md)

 Proje türleri ve düzenleyiciler için en iyi uygulamaları açıklar.

- [Çalışma Zamanı Ayrıntıları](../../extensibility/internals/source-control-runtime-details.md)

 Bir kullanıcı, bir kaynak denetim sistemine eklediğinde, bir proje kaydetme işlemini açıklamaktadır.

## <a name="reference"></a>Başvuru
 <xref:Microsoft.VisualStudio.Shell.Interop.IVsQueryEditQuerySave2> Ortam ya da bir dosya hakkında bellekte değiştirilemez veya kaydedilmiş olan kaynak denetim paketi belirtir.

 <xref:Microsoft.VisualStudio.Shell.Interop.IVsSccManager2> Projeler ve hiyerarşileri kendilerini kaynak denetimiyle kaydetmesini ve kaynak denetimi durumu hakkında bilgi sağlar.

 <xref:Microsoft.VisualStudio.Shell.Interop.IVsSccProject2> Kaynak denetimi proje dosyaları ve proje öğeleri için sağlamak üzere proje sistemindeki uygulanır.

 <xref:Microsoft.VisualStudio.Shell.Interop.IVsTrackProjectDocuments2> Ortam eklemek, kaldırmak veya bir dosya veya bir çözüm dizini yeniden adlandırma izni için Sorgulanacak projeleri tarafından kullanılır.

 <xref:Microsoft.VisualStudio.Shell.Interop.IVsTrackProjectDocumentsEvents2> Proje dosyaları veya dizinleri için yapılan değişiklikler istemcileri bildirir.

## <a name="related-sections"></a>İlgili Bölümler
- [Proje Türleri](../../extensibility/internals/project-types.md)

 Temel yapı taşları projelerine genel bir bakış sağlar [!INCLUDE[vsprvs](../../code-quality/includes/vsprvs_md.md)] tümleşik geliştirme ortamı (IDE). Projeler oluşturmak ve kodu derleme nasıl kontrol açıklayan ek konulara bağlantılar sağlanmaktadır.
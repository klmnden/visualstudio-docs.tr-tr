---
title: Kalıcılığı ve çalışmasını Belge tablosu | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
helpviewer_keywords:
- persistence, managing
- IVsPersistHierarchyItem interface, implementing
- architecture, persistence
- running document table (RDT), architecture
ms.assetid: 27117eae-6c58-4189-a61a-1397a43b5ecf
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: ceb66051d3a1ab0119f4b80a68f0f2990e569fe8
ms.sourcegitcommit: 2193323efc608118e0ce6f6b2ff532f158245d56
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/25/2019
ms.locfileid: "54929776"
---
# <a name="persistence-and-the-running-document-table"></a>Kalıcılık ve Çalıştırılan Belge Tablosu
İçinde [!INCLUDE[vsprvs](../../code-quality/includes/vsprvs_md.md)] IDE, proje tamamen bunlar hizmetini kullanarak gerçekleştirmek, kendi proje öğelerinin Kalıcılık yönetmekten sorumlu <xref:Microsoft.VisualStudio.Shell.Interop.SVsRunningDocumentTable>. Visual Studio ortamında Kalıcılık temel birimini belgelerdir. Proje açma, kaydetme ve çalıştırılan Belge tablosu (RDT), bütün açık belgeleri durumunu izleyen bir kaynak olan belgelerin yeniden adlandırma koordine edin.  
  
## <a name="managing-persistence"></a>Kalıcılık yönetme  
 Projelerini denetleyecek ortamın Kalıcılık hizmet uygulayarak <xref:Microsoft.VisualStudio.Shell.Interop.IVsPersistHierarchyItem> arabirimi. Ortam hiçbir zaman doğrudan kendi kalıcı hale getirmek için bir belge ister, ancak sahip olan proje (veya hiyerarşi) belgeyi kaydetmek ister. Bu proje öğesi verisini yerel dosyaları, uzak dosyaları, bir veritabanı, bir depo veya diğer Orta kaydetmek için projeyi için mümkün kılar.  
  
 Genel ortam RDT tutar. Tüm açık pencereleri girişlerinde ortamı korur ve bunların kılar RDT belgelerde bir çözüm kapatıldığında gibi özel bildirimleri alın. Ayrıca, RDT, karşılık gelen düğümlerini izlemek ortam için mümkün kılar **Çözüm Gezgini**. Proje dosyaları hem proje öğesi belgeleri de dahil olmak üzere, açık, kalıcı nesne başına tek bir kayıtta RDT tutar.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Çalıştırılan Belge tablosu](../../extensibility/internals/running-document-table.md)   
 [IDE’de Seçim ve Para Birimi](../../extensibility/internals/selection-and-currency-in-the-ide.md)
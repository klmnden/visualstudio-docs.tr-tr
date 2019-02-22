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
ms.openlocfilehash: deb5472776bc9c4a4d6bb0ccd8830cba5eea3d04
ms.sourcegitcommit: d0425b6b7d4b99e17ca6ac0671282bc718f80910
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/21/2019
ms.locfileid: "56640275"
---
# <a name="persistence-and-the-running-document-table"></a>Kalıcılık ve Çalıştırılan Belge Tablosu
İçinde [!INCLUDE[vsprvs](../../code-quality/includes/vsprvs_md.md)] IDE, proje tamamen bunlar hizmetini kullanarak gerçekleştirmek, kendi proje öğelerinin Kalıcılık yönetmekten sorumlu <xref:Microsoft.VisualStudio.Shell.Interop.SVsRunningDocumentTable>. Visual Studio ortamında Kalıcılık temel birimini belgelerdir. Proje açma, kaydetme ve çalıştırılan Belge tablosu (RDT), bütün açık belgeleri durumunu izleyen bir kaynak olan belgelerin yeniden adlandırma koordine edin.

## <a name="managing-persistence"></a>Kalıcılık yönetme
 Projelerini denetleyecek ortamın Kalıcılık hizmet uygulayarak <xref:Microsoft.VisualStudio.Shell.Interop.IVsPersistHierarchyItem> arabirimi. Ortam hiçbir zaman doğrudan kendi kalıcı hale getirmek için bir belge ister, ancak sahip olan proje (veya hiyerarşi) belgeyi kaydetmek ister. Bu proje öğesi verisini yerel dosyaları, uzak dosyaları, bir veritabanı, bir depo veya diğer Orta kaydetmek için projeyi için mümkün kılar.

 Genel ortam RDT tutar. Tüm açık pencereleri girişlerinde ortamı korur ve bunların kılar RDT belgelerde bir çözüm kapatıldığında gibi özel bildirimleri alın. Ayrıca, RDT, karşılık gelen düğümlerini izlemek ortam için mümkün kılar **Çözüm Gezgini**. Proje dosyaları hem proje öğesi belgeleri de dahil olmak üzere, açık, kalıcı nesne başına tek bir kayıtta RDT tutar.

## <a name="see-also"></a>Ayrıca Bkz.
- [Çalıştırılan Belge Tablosu](../../extensibility/internals/running-document-table.md)
- [IDE’de Seçim ve Para Birimi](../../extensibility/internals/selection-and-currency-in-the-ide.md)
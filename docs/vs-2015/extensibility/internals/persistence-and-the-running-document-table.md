---
title: Kalıcılığı ve çalışmasını Belge tablosu | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-sdk
ms.topic: conceptual
helpviewer_keywords:
- persistence, managing
- IVsPersistHierarchyItem interface, implementing
- architecture, persistence
- running document table (RDT), architecture
ms.assetid: 27117eae-6c58-4189-a61a-1397a43b5ecf
caps.latest.revision: 11
ms.author: gregvanl
manager: jillfra
ms.openlocfilehash: 2c422ad1735312c82c8dc027c4adf73c1b033685
ms.sourcegitcommit: 8b538eea125241e9d6d8b7297b72a66faa9a4a47
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54765751"
---
# <a name="persistence-and-the-running-document-table"></a>Kalıcılık ve Çalıştırılan Belge Tablosu
[!INCLUDE[vs2017banner](../../includes/vs2017banner.md)]

İçinde [!INCLUDE[vsprvs](../../includes/vsprvs-md.md)] IDE, proje tamamen bunlar hizmetini kullanarak gerçekleştirmek, kendi proje öğelerinin Kalıcılık yönetmekten sorumlu <xref:Microsoft.VisualStudio.Shell.Interop.SVsRunningDocumentTable>. Visual Studio ortamında Kalıcılık temel birimini belgelerdir. Proje açma, kaydetme ve çalıştırılan Belge tablosu (RDT), bütün açık belgeleri durumunu izleyen bir kaynak olan belgelerin yeniden adlandırma koordine edin.  
  
## <a name="managing-persistence"></a>Kalıcılık yönetme  
 Projelerini denetleyecek ortamın Kalıcılık hizmet uygulayarak <xref:Microsoft.VisualStudio.Shell.Interop.IVsPersistHierarchyItem> arabirimi. Ortam hiçbir zaman doğrudan kendi kalıcı hale getirmek için bir belge ister, ancak sahip olan proje (veya hiyerarşi) belgeyi kaydetmek ister. Bu proje öğesi verisini yerel dosyaları, uzak dosyaları, bir veritabanı, bir depo veya diğer Orta kaydetmek için projeyi için mümkün kılar.  
  
 Genel ortam RDT tutar. Tüm açık pencereleri girişlerinde ortamı korur ve bunların kılar RDT belgelerde bir çözüm kapatıldığında gibi özel bildirimleri alın. Ayrıca, RDT, karşılık gelen düğümlerini izlemek ortam için mümkün kılar **Çözüm Gezgini**. Proje dosyaları hem proje öğesi belgeleri de dahil olmak üzere, açık, kalıcı nesne başına tek bir kayıtta RDT tutar.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Çalıştırılan Belge tablosu](../../extensibility/internals/running-document-table.md)   
 [IDE’de Seçim ve Para Birimi](../../extensibility/internals/selection-and-currency-in-the-ide.md)

---
title: Geri alma ve eski API'yi kullanarak yönetme | Microsoft Docs
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
- editors [Visual Studio SDK], legacy - undo management
ms.assetid: 838c0ddf-fdf3-4df1-8d21-79610b8ba0b1
caps.latest.revision: 15
ms.author: gregvanl
manager: ghogen
ms.openlocfilehash: bb2ff049635d75608114be380c9697faf0585725
ms.sourcegitcommit: 9ceaf69568d61023868ced59108ae4dd46f720ab
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/12/2018
ms.locfileid: "49177898"
---
# <a name="managing-undo-and-redo-by-using-the-legacy-api"></a>Yönetme geri alma ve eski API'yi kullanarak yineleme
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Düzenleyiciler, bunlar kod değiştirdiğinizde, son değişikliklerini ters kullanıcıların geri alma işlemlerinin desteklemesi gerekir. Çoğu düzenleyicileri altında uygulanan [!INCLUDE[vsprvs](../includes/vsprvs-md.md)] ve [!INCLUDE[dnprdnshort](../includes/dnprdnshort-md.md)] otomatik olarak tümleşik geliştirme ortamı (IDE) tarafından sağlanan geri alma desteği sağlayabilirsiniz.  
  
## <a name="in-this-section"></a>Bu Bölümde  
 [Nasıl Yapılır: Geri Alma Yönetimini Uygulama](../extensibility/how-to-implement-undo-management.md)  
 Geri alma özelliği, tek veya birden çok görünüm için düzenleyicileri sağlar.  
  
 [Nasıl Yapılır: Geri Alma Yığınını Temizleme](../extensibility/how-to-clear-the-undo-stack.md)  
 Bir geri alma yığını Temizle açıklar.  
  
 [Nasıl Yapılır: Bağlantılı Geri Alma Yönetimini Kullanma](../extensibility/how-to-use-linked-undo-management.md)  
 Bağlantılı geri alma yönetim, düzenleyicisine içerir.  
  
## <a name="reference"></a>Başvuru  
 <xref:Microsoft.VisualStudio.TextManager.Interop.IVsChangeTrackingUndoManager>  
 Birden çok görünüm destekleyen bir düzenleyici için geri alma yönetimi sağlar.  
  
## <a name="related-sections"></a>İlgili Bölümler


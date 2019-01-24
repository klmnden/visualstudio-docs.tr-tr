---
title: Geri alma ve eski API'yi kullanarak yönetme | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-sdk
ms.topic: conceptual
helpviewer_keywords:
- editors [Visual Studio SDK], legacy - undo management
ms.assetid: 838c0ddf-fdf3-4df1-8d21-79610b8ba0b1
caps.latest.revision: 15
ms.author: gregvanl
manager: jillfra
ms.openlocfilehash: 7c2133c75b32e56c1a054740bd829bd04cac97cc
ms.sourcegitcommit: 8b538eea125241e9d6d8b7297b72a66faa9a4a47
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54797309"
---
# <a name="managing-undo-and-redo-by-using-the-legacy-api"></a>Yönetme geri alma ve eski API'yi kullanarak yineleme
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Düzenleyiciler, bunlar kod değiştirdiğinizde, son değişikliklerini ters kullanıcıların geri alma işlemlerinin desteklemesi gerekir. Çoğu düzenleyicileri altında uygulanan [!INCLUDE[vsprvs](../includes/vsprvs-md.md)] ve [!INCLUDE[dnprdnshort](../includes/dnprdnshort-md.md)] otomatik olarak tümleşik geliştirme ortamı (IDE) tarafından sağlanan geri alma desteği sağlayabilirsiniz.  
  
## <a name="in-this-section"></a>Bu Bölümde  
 [Nasıl yapılır: Uygulama geri alma yönetimi](../extensibility/how-to-implement-undo-management.md)  
 Geri alma özelliği, tek veya birden çok görünüm için düzenleyicileri sağlar.  
  
 [Nasıl yapılır: Geri alma yığını Temizle](../extensibility/how-to-clear-the-undo-stack.md)  
 Bir geri alma yığını Temizle açıklar.  
  
 [Nasıl yapılır: Bağlantılı geri alma Yönetimi'ni kullanın](../extensibility/how-to-use-linked-undo-management.md)  
 Bağlantılı geri alma yönetim, düzenleyicisine içerir.  
  
## <a name="reference"></a>Başvuru  
 <xref:Microsoft.VisualStudio.TextManager.Interop.IVsChangeTrackingUndoManager>  
 Birden çok görünüm destekleyen bir düzenleyici için geri alma yönetimi sağlar.  
  
## <a name="related-sections"></a>İlgili Bölümler

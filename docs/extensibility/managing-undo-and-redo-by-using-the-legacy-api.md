---
title: Geri alma ve eski API'yi kullanarak yönetme | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
helpviewer_keywords:
- editors [Visual Studio SDK], legacy - undo management
ms.assetid: 838c0ddf-fdf3-4df1-8d21-79610b8ba0b1
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: adf6a2405ae3d3408f9cf04199ba05dff9232326
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62856432"
---
# <a name="manage-undo-and-redo-by-using-the-legacy-api"></a>Geri alma yönetmek ve eski API'yi kullanarak yineleme
Düzenleyiciler, bunlar kod değiştirdiğinizde, son değişikliklerini ters kullanıcıların geri alma işlemlerinin desteklemesi gerekir. Çoğu düzenleyicileri altında uygulanan [!INCLUDE[vsprvs](../code-quality/includes/vsprvs_md.md)] ve [!INCLUDE[dnprdnshort](../code-quality/includes/dnprdnshort_md.md)] otomatik olarak tümleşik geliştirme ortamı (IDE) tarafından sağlanan geri alma desteği sağlayabilirsiniz.

## <a name="in-this-section"></a>Bu bölümde
- [Nasıl yapılır: Uygulama geri alma Yönetim](../extensibility/how-to-implement-undo-management.md) tek veya birden çok görünüm düzenleyicilerle geri alma yeteneği sağlar.

- [Nasıl yapılır: Geri alma yığını Temizle](../extensibility/how-to-clear-the-undo-stack.md) bir geri alma yığını Temizle açıklar.

- [Nasıl yapılır: Bağlantılı geri alma Yönetimi](../extensibility/how-to-use-linked-undo-management.md) Incorporates düzenleyiciniz geri yönetime bağlı.

## <a name="reference"></a>Başvuru
 <xref:Microsoft.VisualStudio.TextManager.Interop.IVsChangeTrackingUndoManager> Birden çok görünüm destekleyen bir düzenleyici için geri alma yönetimi sağlar.

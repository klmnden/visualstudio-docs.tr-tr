---
title: Geri alma ve eski API'yi kullanarak yönetme | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
helpviewer_keywords:
- editors [Visual Studio SDK], legacy - undo management
ms.assetid: 838c0ddf-fdf3-4df1-8d21-79610b8ba0b1
author: madskristensen
ms.author: madsk
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: a8a93b4fd12cd9a0bd2e5a5f3c70486e370545a9
ms.sourcegitcommit: 12f2851c8c9bd36a6ab00bf90a020c620b364076
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/06/2019
ms.locfileid: "66747644"
---
# <a name="manage-undo-and-redo-by-using-the-legacy-api"></a>Geri alma yönetmek ve eski API'yi kullanarak yineleme
Düzenleyiciler, bunlar kod değiştirdiğinizde, son değişikliklerini ters kullanıcıların geri alma işlemlerinin desteklemesi gerekir. Çoğu düzenleyicileri altında uygulanan [!INCLUDE[vsprvs](../code-quality/includes/vsprvs_md.md)] ve .NET Framework tümleşik geliştirme ortamı (IDE) otomatik olarak sağlanan geri alma desteğinin olabilir.

## <a name="in-this-section"></a>Bu bölümde
- [Nasıl yapılır: Uygulama geri alma Yönetim](../extensibility/how-to-implement-undo-management.md) tek veya birden çok görünüm düzenleyicilerle geri alma yeteneği sağlar.

- [Nasıl yapılır: Geri alma yığını Temizle](../extensibility/how-to-clear-the-undo-stack.md) bir geri alma yığını Temizle açıklar.

- [Nasıl yapılır: Bağlantılı geri alma Yönetimi](../extensibility/how-to-use-linked-undo-management.md) Incorporates düzenleyiciniz geri yönetime bağlı.

## <a name="reference"></a>Başvuru
 <xref:Microsoft.VisualStudio.TextManager.Interop.IVsChangeTrackingUndoManager> Birden çok görünüm destekleyen bir düzenleyici için geri alma yönetimi sağlar.

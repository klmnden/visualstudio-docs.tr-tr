---
title: Bağlantı sağlayıcıları | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
helpviewer_keywords:
- port suppliers
- debugging [Debugging SDK], port suppliers
ms.assetid: a8f3db96-1a13-4e93-9ef6-0861880369e0
author: madskristensen
ms.author: madsk
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: 5909587cbed118d618ea1605c8a169024028adf0
ms.sourcegitcommit: 40d612240dc5bea418cd27fdacdf85ea177e2df3
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/29/2019
ms.locfileid: "66351469"
---
# <a name="port-suppliers"></a>Bağlantı noktası sağlayıcıları
Hata ayıklayıcı mimarisinde bir *bağlantı noktası sağlayıcısı*:

- Sunucu tarafından bulunur ve bu sunucuya gönderilen istek bağlantı noktaları sağlar.

- Ekleyebilir ve bağlantı noktalarını içeren sunucudan kaldırın.

- Sunucuya yayımlamış tüm bağlantı noktaları sıralayabilirsiniz.

- Tarafından temsil edilen bir [IDebugPortSupplier2](../../extensibility/debugger/reference/idebugportsupplier2.md) kayıt defteri aracılığıyla Visual Studio ile kayıtlı arabirim. Bu arabirim, çağrılarak alınabilir [GetPortSupplier](../../extensibility/debugger/reference/idebugcoreserver2-getportsupplier.md).

  [!INCLUDE[vsprvs](../../code-quality/includes/vsprvs_md.md)] Varsayılan bağlantı noktası sağlayıcısı ve varsayılan bir bağlantı noktası sağlar. Özel bir bağlantı noktası uygulanması gerekiyorsa, özel bağlantı noktası sağlayıcısı Ayrıca bu özel bağlantı sağlamak için uygulanması gerekir.

## <a name="see-also"></a>Ayrıca bkz.
- [Sunucular](../../extensibility/debugger/servers-visual-studio-sdk.md)
- [Bağlantı Noktaları](../../extensibility/debugger/ports.md)
- [Hata ayıklayıcı kavramları](../../extensibility/debugger/debugger-concepts.md)
- [IDebugPortSupplier2](../../extensibility/debugger/reference/idebugportsupplier2.md)
- [GetPortSupplier](../../extensibility/debugger/reference/idebugcoreserver2-getportsupplier.md)
---
title: Bağlantı sağlayıcıları | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
helpviewer_keywords:
- port suppliers
- debugging [Debugging SDK], port suppliers
ms.assetid: a8f3db96-1a13-4e93-9ef6-0861880369e0
author: gregvanl
ms.author: gregvanl
manager: douge
ms.workload:
- vssdk
ms.openlocfilehash: e134b9b4adeb45693a9841a0a867a9c3630bf2aa
ms.sourcegitcommit: 37fb7075b0a65d2add3b137a5230767aa3266c74
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/02/2019
ms.locfileid: "53835110"
---
# <a name="port-suppliers"></a>Bağlantı noktası sağlayıcıları
Hata ayıklayıcı mimarisinde bir *bağlantı noktası sağlayıcısı*:  
  
- Sunucu tarafından bulunur ve bu sunucuya gönderilen istek bağlantı noktaları sağlar.  
  
- Ekleyebilir ve bağlantı noktalarını içeren sunucudan kaldırın.  
  
- Sunucuya yayımlamış tüm bağlantı noktaları sıralayabilirsiniz.  
  
- Tarafından temsil edilen bir [IDebugPortSupplier2](../../extensibility/debugger/reference/idebugportsupplier2.md) kayıt defteri aracılığıyla Visual Studio ile kayıtlı arabirim. Bu arabirim, çağrılarak alınabilir [GetPortSupplier](../../extensibility/debugger/reference/idebugcoreserver2-getportsupplier.md).  
  
  [!INCLUDE[vsprvs](../../code-quality/includes/vsprvs_md.md)] Varsayılan bağlantı noktası sağlayıcısı ve varsayılan bir bağlantı noktası sağlar. Özel bir bağlantı noktası uygulanması gerekiyorsa, özel bağlantı noktası sağlayıcısı Ayrıca bu özel bağlantı sağlamak için uygulanması gerekir.  
  
## <a name="see-also"></a>Ayrıca bkz.  
 [Sunucuları](../../extensibility/debugger/servers-visual-studio-sdk.md)   
 [Bağlantı noktaları](../../extensibility/debugger/ports.md)   
 [Hata ayıklayıcı kavramları](../../extensibility/debugger/debugger-concepts.md)   
 [IDebugPortSupplier2](../../extensibility/debugger/reference/idebugportsupplier2.md)   
 [GetPortSupplier](../../extensibility/debugger/reference/idebugcoreserver2-getportsupplier.md)
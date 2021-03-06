---
title: Bağlantı sağlayıcıları | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-sdk
ms.topic: conceptual
helpviewer_keywords:
- port suppliers
- debugging [Debugging SDK], port suppliers
ms.assetid: a8f3db96-1a13-4e93-9ef6-0861880369e0
caps.latest.revision: 16
ms.author: gregvanl
manager: jillfra
ms.openlocfilehash: e90871927c30399dea4691381baa749db2b3e8bf
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "68153703"
---
# <a name="port-suppliers"></a>Bağlantı Noktası Sağlayıcıları
[!INCLUDE[vs2017banner](../../includes/vs2017banner.md)]

Hata ayıklayıcı mimarisi bakımından bir **bağlantı noktası sağlayıcısı**:  
  
- Sunucu tarafından bulunur ve bu sunucuya gönderilen istek bağlantı noktaları sağlar.  
  
- Ekleyebilir ve bağlantı noktalarını içeren sunucudan kaldırın.  
  
- Sunucuya yayımlamış tüm bağlantı noktaları sıralayabilirsiniz.  
  
- Tarafından temsil edilen bir [IDebugPortSupplier2](../../extensibility/debugger/reference/idebugportsupplier2.md) kayıt defteri aracılığıyla Visual Studio ile kayıtlı arabirim. Bu arabirim, çağrılarak alınabilir [GetPortSupplier](../../extensibility/debugger/reference/idebugcoreserver2-getportsupplier.md).  
  
  [!INCLUDE[vsprvs](../../includes/vsprvs-md.md)] Varsayılan bağlantı noktası sağlayıcısı ve varsayılan bir bağlantı noktası sağlar. Özel bir bağlantı noktası uygulanması gerekiyorsa, özel bağlantı noktası sağlayıcısı Ayrıca bu özel bağlantı sağlamak için uygulanması gerekir.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Sunucuları](../../extensibility/debugger/servers-visual-studio-sdk.md)   
 [Bağlantı noktaları](../../extensibility/debugger/ports.md)   
 [Hata ayıklayıcı kavramları](../../extensibility/debugger/debugger-concepts.md)   
 [IDebugPortSupplier2](../../extensibility/debugger/reference/idebugportsupplier2.md)   
 [GetPortSupplier](../../extensibility/debugger/reference/idebugcoreserver2-getportsupplier.md)

---
title: Bağlantı noktaları | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-sdk
ms.topic: conceptual
helpviewer_keywords:
- ports
- debugging [Debugging SDK], ports
ms.assetid: 1d7f3aa7-7eff-4cab-bc53-0a566b1a9363
caps.latest.revision: 14
ms.author: gregvanl
manager: jillfra
ms.openlocfilehash: 73003e00fef5c37db4a702e7a4a1121600673844
ms.sourcegitcommit: 8b538eea125241e9d6d8b7297b72a66faa9a4a47
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54760798"
---
# <a name="ports"></a>Bağlantı Noktaları
[!INCLUDE[vs2017banner](../../includes/vs2017banner.md)]

Hata ayıklayıcı mimarisi bakımından bir **bağlantı noktası**:  
  
- Bir dizi işlemleri için bir kapsayıcı, bir sunucu üzerinde çalışıyor. Örneğin, bir bağlantı noktası seri kablo Windows CE tabanlı bir cihaz için veya ağa bağlı DCOM olmayan bir makineye bağlantı temsil edebilir. Yerel bağlantı noktası adı verilen bir özel bağlantı noktası, yerel makine üzerinde çalışan tüm işlemler içeriyor.  
  
- Kendi adına veya tanımlayıcısına göre belirleyebilirsiniz.  
  
- Bağlantı noktası üzerinde çalışan tüm işlemler listeleme ve başlatabileceğini ve bu işlemleri sonlandırın.  
  
- Tarafından temsil edilen bir [IDebugPort2](../../extensibility/debugger/reference/idebugport2.md) geçirerek oluşturulduğu arabirimi bir [IDebugPortRequest2](../../extensibility/debugger/reference/idebugportrequest2.md) bağımsız değişkeni [AddPort](../../extensibility/debugger/reference/idebugportsupplier2-addport.md).  
  
  [!INCLUDE[vsprvs](../../includes/vsprvs-md.md)] tüm Windows tabanlı işlemler, yerel ve yönetilen işleyen varsayılan bağlantı noktası sağlar. Özel bir bağlantı noktası bağlantılar için Windows tabanlı olmayan dış cihazlarla uygulanmalıdır. Bu tür özel bağlantı noktaları sağlamanız gerekiyorsa, özel bağlantı noktası sağlayıcısı ayrıca uygulanması gerekir.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Sunucuları](../../extensibility/debugger/servers-visual-studio-sdk.md)   
 [İşlemler](../../extensibility/debugger/processes.md)   
 [Hata ayıklayıcı kavramları](../../extensibility/debugger/debugger-concepts.md)   
 [IDebugPort2](../../extensibility/debugger/reference/idebugport2.md)   
 [IDebugPortRequest2](../../extensibility/debugger/reference/idebugportrequest2.md)   
 [AddPort](../../extensibility/debugger/reference/idebugportsupplier2-addport.md)

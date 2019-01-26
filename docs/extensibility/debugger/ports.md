---
title: Bağlantı noktaları | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
helpviewer_keywords:
- ports
- debugging [Debugging SDK], ports
ms.assetid: 1d7f3aa7-7eff-4cab-bc53-0a566b1a9363
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: e62eb8c220276737cfbe0cd275b0fc81afaa859c
ms.sourcegitcommit: 2193323efc608118e0ce6f6b2ff532f158245d56
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/25/2019
ms.locfileid: "55012241"
---
# <a name="ports"></a>Bağlantı Noktaları
Hata ayıklayıcı mimarisinde bir *bağlantı noktası*:  
  
- Bir dizi işlemleri için bir kapsayıcı, bir sunucu üzerinde çalışıyor. Örneğin, bir bağlantı noktası seri kablo Windows CE tabanlı bir cihaz için veya ağa bağlı DCOM olmayan bir makineye bağlantı temsil edebilir. Yerel bağlantı noktası adı verilen bir özel bağlantı noktası, yerel makine üzerinde çalışan tüm işlemler içeriyor.  
  
- Kendi adına veya tanımlayıcısına göre belirleyebilirsiniz.  
  
- Bağlantı noktası üzerinde çalışan tüm işlemler listeleme ve başlatabileceğini ve bu işlemleri sonlandırın.  
  
- Tarafından temsil edilen bir [IDebugPort2](../../extensibility/debugger/reference/idebugport2.md) geçirerek oluşturulduğu arabirimi bir [IDebugPortRequest2](../../extensibility/debugger/reference/idebugportrequest2.md) bağımsız değişkeni [AddPort](../../extensibility/debugger/reference/idebugportsupplier2-addport.md).  
  
  [!INCLUDE[vsprvs](../../code-quality/includes/vsprvs_md.md)] tüm Windows tabanlı işlemler, yerel ve yönetilen işleyen varsayılan bağlantı noktası sağlar. Özel bir bağlantı noktası bağlantılar için Windows tabanlı olmayan dış cihazlarla ayarlanmalıdır. Bu tür özel bağlantı noktaları sağlamanız gerekiyorsa, özel bağlantı noktası sağlayıcısı ayarlamanız gerekir.  
  
## <a name="see-also"></a>Ayrıca bkz.  
 [Sunucuları](../../extensibility/debugger/servers-visual-studio-sdk.md)   
 [İşlemler](../../extensibility/debugger/processes.md)   
 [Hata ayıklayıcı kavramları](../../extensibility/debugger/debugger-concepts.md)   
 [IDebugPort2](../../extensibility/debugger/reference/idebugport2.md)   
 [IDebugPortRequest2](../../extensibility/debugger/reference/idebugportrequest2.md)   
 [AddPort](../../extensibility/debugger/reference/idebugportsupplier2-addport.md)
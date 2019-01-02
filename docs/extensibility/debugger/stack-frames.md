---
title: Yığın çerçevesi | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
helpviewer_keywords:
- stack frames, debugging
- debugging [Debugging SDK], stack frames
- stack frames
ms.assetid: b5e439d4-1e9d-4e13-9cad-bb8b136d4ca8
author: gregvanl
ms.author: gregvanl
manager: douge
ms.workload:
- vssdk
ms.openlocfilehash: 1a7029f537d6d7ebcb956aa200cb8f22c160e540
ms.sourcegitcommit: 37fb7075b0a65d2add3b137a5230767aa3266c74
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/02/2019
ms.locfileid: "53959722"
---
# <a name="stack-frames"></a>Yığın çerçeveleri
Hata ayıklayıcı mimarisinde bir *yığın çerçevesi*:  
  
-   Bir iş parçacığı yürütme bağlamı sağlayan bir yığının bir soyutlamadır. Bir iş parçacığı her zaman içinde bir işlevi yürütür. Bir yığın çerçevesi için işlevi ve bağımsız değişkenler, yerel değişkenleri tutar. Visual Studio ile hata ayıklamak için dil veya ortam ayıklanan yığın çerçeveleri desteklemesi gerekir.  
  
-   İçin her ikisi de tanımlamak ve kendisini açıklar ve ilişkili iş parçacığı döndürebilir. Bir yığın çerçevesi, dosyadaki geçerli yönerge işaretçisini ve ilgili belgeleri gösteren kod bağlamı ve ifade değerlendirme bağlamı da döndürebilir.  
  
-   Adı, türü ve değeri yerel değişkenleri ve bağımsız değişkenleri açıklar ve çeşitli IDE hata ayıklama pencerelerinde göründüğü özellikleri vardır.  
  
-   Tarafından temsil edilen bir [IDebugStackFrame2](../../extensibility/debugger/reference/idebugstackframe2.md) arabirimi, genellikle bir hata ayıklama altyapısı (DE) veya bir iş parçacığının söz konusu kümelerdeki sanal makine tarafından oluşturuldu.  
  
## <a name="see-also"></a>Ayrıca bkz.  
 [Hata ayıklayıcı bağlamları](../../extensibility/debugger/debugger-contexts.md)   
 [Hata ayıklayıcı kavramları](../../extensibility/debugger/debugger-concepts.md)   
 [Hata ayıklama altyapısı](../../extensibility/debugger/debug-engine.md)   
 [IDebugStackFrame2](../../extensibility/debugger/reference/idebugstackframe2.md)
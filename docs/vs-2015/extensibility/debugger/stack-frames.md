---
title: Yığın çerçevesi | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-sdk
ms.topic: conceptual
helpviewer_keywords:
- stack frames, debugging
- debugging [Debugging SDK], stack frames
- stack frames
ms.assetid: b5e439d4-1e9d-4e13-9cad-bb8b136d4ca8
caps.latest.revision: 12
ms.author: gregvanl
manager: jillfra
ms.openlocfilehash: d3050e89db2f5cbb138f3d358b10c7cd936c560e
ms.sourcegitcommit: 1fc6ee928733e61a1f42782f832ead9f7946d00c
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/22/2019
ms.locfileid: "60106767"
---
# <a name="stack-frames"></a>Yığın Çerçeveleri
[!INCLUDE[vs2017banner](../../includes/vs2017banner.md)]

Hata ayıklayıcı mimarisi bakımından bir **yığın çerçevesi**:  
  
- Bir iş parçacığı yürütme bağlamı sağlayan bir yığının bir soyutlamadır. Bir iş parçacığı her zaman içinde bir işlevi yürütür. Bir yığın çerçevesi için işlevi ve bağımsız değişkenler, yerel değişkenleri tutar. Visual Studio ile hata ayıklamak için dil veya ortam ayıklanan yığın çerçeveleri desteklemesi gerekir.  
  
- İçin her ikisi de tanımlamak ve kendisini açıklar ve ilişkili iş parçacığı döndürebilir. Bir yığın çerçevesi, dosyadaki geçerli yönerge işaretçisini yanı sıra ilgili belgeleri gösteren kod bağlamı ve ifade değerlendirme bağlamı da döndürebilir.  
  
- Adı, türü ve değeri yerel değişkenleri ve bağımsız değişkenleri açıklar ve çeşitli IDE hata ayıklama pencerelerinde göründüğü özellikleri vardır.  
  
- Tarafından temsil edilen bir [IDebugStackFrame2](../../extensibility/debugger/reference/idebugstackframe2.md) arabirimi, genellikle bir hata ayıklama altyapısı (DE) veya bir iş parçacığının söz konusu kümelerdeki sanal makine tarafından oluşturuldu.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Hata ayıklayıcı bağlamları](../../extensibility/debugger/debugger-contexts.md)   
 [Hata ayıklayıcı kavramları](../../extensibility/debugger/debugger-concepts.md)   
 [Hata ayıklama altyapısı](../../extensibility/debugger/debug-engine.md)   
 [IDebugStackFrame2](../../extensibility/debugger/reference/idebugstackframe2.md)

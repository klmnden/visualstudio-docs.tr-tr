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
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: 4d38f53b6841c03e769c8d1f1af967cf903a0b32
ms.sourcegitcommit: b0d8e61745f67bd1f7ecf7fe080a0fe73ac6a181
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/22/2019
ms.locfileid: "56684098"
---
# <a name="stack-frames"></a>Yığın çerçeveleri
Hata ayıklayıcı mimarisinde bir *yığın çerçevesi*:

-   Bir iş parçacığı yürütme bağlamı sağlayan bir yığının bir soyutlamadır. Bir iş parçacığı her zaman içinde bir işlevi yürütür. Bir yığın çerçevesi için işlevi ve bağımsız değişkenler, yerel değişkenleri tutar. Visual Studio ile hata ayıklamak için dil veya ortam ayıklanan yığın çerçeveleri desteklemesi gerekir.

-   İçin her ikisi de tanımlamak ve kendisini açıklar ve ilişkili iş parçacığı döndürebilir. Bir yığın çerçevesi, dosyadaki geçerli yönerge işaretçisini ve ilgili belgeleri gösteren kod bağlamı ve ifade değerlendirme bağlamı da döndürebilir.

-   Adı, türü ve değeri yerel değişkenleri ve bağımsız değişkenleri açıklar ve çeşitli IDE hata ayıklama pencerelerinde göründüğü özellikleri vardır.

-   Tarafından temsil edilen bir [IDebugStackFrame2](../../extensibility/debugger/reference/idebugstackframe2.md) arabirimi, genellikle bir hata ayıklama altyapısı (DE) veya bir iş parçacığının söz konusu kümelerdeki sanal makine tarafından oluşturuldu.

## <a name="see-also"></a>Ayrıca bkz.
- [Hata ayıklayıcı bağlamları](../../extensibility/debugger/debugger-contexts.md)
- [Hata ayıklayıcı kavramları](../../extensibility/debugger/debugger-concepts.md)
- [Hata ayıklama altyapısı](../../extensibility/debugger/debug-engine.md)
- [IDebugStackFrame2](../../extensibility/debugger/reference/idebugstackframe2.md)
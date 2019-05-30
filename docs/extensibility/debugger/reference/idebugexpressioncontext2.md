---
title: IDebugExpressionContext2 | Microsoft Docs
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- IDebugExpressionContext2
helpviewer_keywords:
- IDebugExpressionContext2 interface
ms.assetid: 577fdaae-4b2d-4112-9839-ab899535fa6f
author: madskristensen
ms.author: madsk
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: 3ad9c3d6bb1b0a5baccbcf5bf47eb02a8bb5efa5
ms.sourcegitcommit: 40d612240dc5bea418cd27fdacdf85ea177e2df3
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/29/2019
ms.locfileid: "66325861"
---
# <a name="idebugexpressioncontext2"></a>IDebugExpressionContext2
İfade değerlendirme bağlamının bu arabirimi temsil eder

## <a name="syntax"></a>Sözdizimi

```
IDebugExpressionContext2 : IUnknown
```

## <a name="notes-for-implementers"></a>Uygulayanlar için Notlar
 Hata ayıklama altyapısı (DE), bir ifade değerlendirilebilen bir bağlamı temsil etmek için bu arabirimi uygular.

## <a name="notes-for-callers"></a>Arayanlar İçin Notlar
 Bir çağrı [GetExpressionContext](../../../extensibility/debugger/reference/idebugstackframe2-getexpressioncontext.md) bu döndürür arabirimi. Bu arabirim, yalnızca hata ayıklanan programa duraklatıldı ve bir yığın çerçevesini kullanılabilir olduğunda erişilebilir.

## <a name="methods-in-vtable-order"></a>Vtable sırayla yöntemleri
 Aşağıdaki tabloda yöntemlerini gösterilmektedir `IDebugExpressionContext2`.

|Yöntem|Açıklama|
|------------|-----------------|
|[GetName](../../../extensibility/debugger/reference/idebugexpressioncontext2-getname.md)|Değerlendirme bağlamı adını alır.|
|[ParseText](../../../extensibility/debugger/reference/idebugexpressioncontext2-parsetext.md)|Metin tabanlı bir ifade değerlendirme ayrıştırır.|

## <a name="remarks"></a>Açıklamalar
 Değerlendirme bağlamı, ifade değerlendirmesi gerçekleştirmek için kapsam olarak düşünülebilir.

 Bir program durdu, oturum hata ayıklama Yöneticisi (SDM) bir yığın çerçevesi bir çağrı ile DE elde [EnumFrameInfo](../../../extensibility/debugger/reference/idebugthread2-enumframeinfo.md). SDM sonra çağıran [GetExpressionContext](../../../extensibility/debugger/reference/idebugstackframe2-getexpressioncontext.md) almak için `IDebugExpressionContext2` arabirimi. Bu çağrı takip [ParseText](../../../extensibility/debugger/reference/idebugexpressioncontext2-parsetext.md) oluşturmak için bir [IDebugExpression2](../../../extensibility/debugger/reference/idebugexpression2.md) değerlendirilecek hazır ayrıştırılmış ifadeyi temsil eden arabirim.

## <a name="requirements"></a>Gereksinimler
 Üstbilgi: msdbg.h

 Ad alanı: Microsoft.VisualStudio.Debugger.Interop

 Derleme: Microsoft.VisualStudio.Debugger.Interop.dll

## <a name="see-also"></a>Ayrıca bkz.
- [Temel Arabirimler](../../../extensibility/debugger/reference/core-interfaces.md)
- [GetExpressionContext](../../../extensibility/debugger/reference/idebugstackframe2-getexpressioncontext.md)
- [IDebugExpression2](../../../extensibility/debugger/reference/idebugexpression2.md)
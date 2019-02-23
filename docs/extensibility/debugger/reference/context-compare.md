---
title: CONTEXT_COMPARE | Microsoft Docs
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- CONTEXT_COMPARE
helpviewer_keywords:
- CONTEXT_COMPARE enumeration
ms.assetid: 701ed61c-a320-4c20-a335-0b840024abc0
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: 21628bda9dc0437672b0b755bb64f1c882b0acbf
ms.sourcegitcommit: b0d8e61745f67bd1f7ecf7fe080a0fe73ac6a181
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/22/2019
ms.locfileid: "56689180"
---
# <a name="contextcompare"></a>CONTEXT_COMPARE
İki bellek bağlamları karşılaştırma ölçütü belirtir.

## <a name="syntax"></a>Sözdizimi

```cpp
enum enum_CONTEXT_COMPARE {
    CONTEXT_EQUAL                 = 0x0001,
    CONTEXT_LESS_THAN             = 0x0002,
    CONTEXT_GREATER_THAN          = 0x0003,
    CONTEXT_LESS_THAN_OR_EQUAL    = 0x0004,
    CONTEXT_GREATER_THAN_OR_EQUAL = 0x0005,
    CONTEXT_SAME_SCOPE            = 0x0006,
    CONTEXT_SAME_FUNCTION         = 0x0007,
    CONTEXT_SAME_MODULE           = 0x0008,
    CONTEXT_SAME_PROCESS          = 0x0009
};
typedef DWORD CONTEXT_COMPARE;
```

```csharp
public enum enum_CONTEXT_COMPARE {
    CONTEXT_EQUAL                 = 0x0001,
    CONTEXT_LESS_THAN             = 0x0002,
    CONTEXT_GREATER_THAN          = 0x0003,
    CONTEXT_LESS_THAN_OR_EQUAL    = 0x0004,
    CONTEXT_GREATER_THAN_OR_EQUAL = 0x0005,
    CONTEXT_SAME_SCOPE            = 0x0006,
    CONTEXT_SAME_FUNCTION         = 0x0007,
    CONTEXT_SAME_MODULE           = 0x0008,
    CONTEXT_SAME_PROCESS          = 0x0009
};
```

## <a name="members"></a>Üyeler
CONTEXT_EQUAL hedef bellek bağlamına eşittir listedeki ilk bellek bağlam bulun.

CONTEXT_LESS_THAN hedef bellek bağlam'dan küçük listedeki ilk bellek bağlam bulun.

CONTEXT_GREATER_THAN hedef bellek bağlamını anlamaktan büyük listedeki ilk bellek bağlam bulun.

CONTEXT_LESS_THAN_OR_EQUAL hedef bellek bağlam küçük veya ona eşit listedeki ilk bellek bağlam bulun.

CONTEXT_GREATER_THAN_OR_EQUAL büyüktür veya eşittir hedef bellek bağlam listedeki ilk bellek bağlam bulun.

CONTEXT_SAME_SCOPE hedef bellek bağlamı ile aynı kapsamda olan listede ilk bellek bağlam bulun.

CONTEXT_SAME_FUNCTION hedef bellek kapsamla aynı işlevde listesinde ilk bellek içeriği bulabilirsiniz.

CONTEXT_SAME_MODULE aynı modülde hedef bellek içeriği olarak listede ilk bellek içeriği bulabilirsiniz.

CONTEXT_SAME_PROCESS ilk bellek içeriği hedef bellek içerik olarak aynı işlemde olduğundan listede bulun.

## <a name="remarks"></a>Açıklamalar
Bağımsız değişken olarak geçirilen [karşılaştırma](../../../extensibility/debugger/reference/idebugmemorycontext2-compare.md) yöntemi.

Bu değerler, belirtilen karşılaştırma ölçütleri karşılayan bir listedeki ilk bellek içeriği bulmak için kullanılır. Bir bellek bağlamı kendisine karşı karşılaştırmak için bellek içerikleri bir listesi verilir `IDebugMemoryContext2::Compare` yöntemi. Karşılaştırma işleci olan listede ilk bellek bağlam `true` sonra döndürülür.

## <a name="requirements"></a>Gereksinimler
Üstbilgi: msdbg.h

Ad alanı: Microsoft.VisualStudio.Debugger.Interop

Derleme: Microsoft.VisualStudio.Debugger.Interop.dll

## <a name="see-also"></a>Ayrıca Bkz.
- [Sabit Listeleri](../../../extensibility/debugger/reference/enumerations-visual-studio-debugging.md)
- [Compare](../../../extensibility/debugger/reference/idebugmemorycontext2-compare.md)

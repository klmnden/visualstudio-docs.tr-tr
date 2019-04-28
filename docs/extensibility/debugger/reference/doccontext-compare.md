---
title: DOCCONTEXT_COMPARE | Microsoft Docs
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- DOCCONTEXT_COMPARE
helpviewer_keywords:
- DOCCONTEXT_COMPARE enumeration
ms.assetid: ed947c34-b07e-4b69-8381-b6e7cb842862
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: e36e9c3c0870cb81dd02f646636eeb758f1ddb62
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62877893"
---
# <a name="doccontextcompare"></a>DOCCONTEXT_COMPARE
İki belge bağlamları karşılaştırma ölçütü belirtir.

## <a name="syntax"></a>Sözdizimi

```cpp
enum enum_DOCCONTEXT_COMPARE {
    DOCCONTEXT_EQUAL         = 0x0001,
    DOCCONTEXT_LESS_THAN     = 0x0002,
    DOCCONTEXT_GREATER_THAN  = 0x0003,
    DOCCONTEXT_SAME_DOCUMENT = 0x0004
};
typedef DWORD DOCCONTEXT_COMPARE;
```

```csharp
enum enum_DOCCONTEXT_COMPARE {
    DOCCONTEXT_EQUAL         = 0x0001,
    DOCCONTEXT_LESS_THAN     = 0x0002,
    DOCCONTEXT_GREATER_THAN  = 0x0003,
    DOCCONTEXT_SAME_DOCUMENT = 0x0004
};
```

## <a name="members"></a>Üyeler
DOCCONTEXT_EQUAL hedef belge bağlamına eşittir listedeki ilk belge bağlamı bulun.

DOCCONTEXT_LESS_THAN hedef belge bağlamı'dan küçük listedeki ilk belge bağlamı bulun.

DOCCONTEXT_GREATER_THAN hedef belge bağlamı büyük listedeki ilk belge bağlamı bulun.

DOCCONTEXT_SAME_DOCUMENT aynı belgede hedef belge bağlamı olarak listede ilk belge içeriği bulabilirsiniz.

## <a name="remarks"></a>Açıklamalar
Bağımsız değişken olarak geçirilen [karşılaştırma](../../../extensibility/debugger/reference/idebugdocumentcontext2-compare.md) yöntemi.

Bu değerler, listedeki ilk belge içeriği bulmak için karşılaştırma ölçütleri belirtmek için kullanılır. Bir belge bağlamına belge bağlamları listesini kendisine karşı karşılaştırmak için verilen `IDebugDocumentContext2::Compare` yöntemi. Karşılaştırma işleci olan listede ilk belge bağlamı `true` sonra döndürülür.

## <a name="requirements"></a>Gereksinimler
Üstbilgi: msdbg.h

Ad alanı: Microsoft.VisualStudio.Debugger.Interop

Derleme: Microsoft.VisualStudio.Debugger.Interop.dll

## <a name="see-also"></a>Ayrıca Bkz.
- [Sabit Listeleri](../../../extensibility/debugger/reference/enumerations-visual-studio-debugging.md)
- [Compare](../../../extensibility/debugger/reference/idebugdocumentcontext2-compare.md)

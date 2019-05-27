---
title: INTERCEPT_EXCEPTION_ACTION | Microsoft Docs
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- INTERCEPT_EXCEPTION_ACTION
helpviewer_keywords:
- INTERCEPT_EXCEPTION_ACTION enumeration
ms.assetid: e647f1eb-2932-4447-8c78-3b0d706fb972
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
dev_langs:
- CPP
- CSharp
ms.openlocfilehash: b73b021201a3fc11509c429eda3877c24d6be6e3
ms.sourcegitcommit: 19ec963ed6d585719cb83ba677434ea6580e0d1f
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/24/2019
ms.locfileid: "66210126"
---
# <a name="interceptexceptionaction"></a>INTERCEPT_EXCEPTION_ACTION
Özel durumları yakalayıp olduğunda gerçekleştirilecek eylemleri belirtir.

## <a name="syntax"></a>Sözdizimi

```cpp
enum enum_INTERCEPT_EXCEPTION_ACTION
{
    IEA_INTERCEPT = 0x0001
}
typedef DWORD INTERCEPT_EXCEPTION_ACTION;
```

```csharp
public enum enum_INTERCEPT_EXCEPTION_ACTION
{
    IEA_INTERCEPT = 0x0001
}
```

## <a name="parameters"></a>Parametreler

`IEA_INTERCEPT`\
Geçerli özel durumun engellemesine olanak tanır. Bu, şu anda desteklenen tek değerdir ve belirtilmesi gerekir.

## <a name="remarks"></a>Açıklamalar
Bu değerleri yöntemlere geçirilen [Interceptcurrentexception](../../../extensibility/debugger/reference/idebugstackframe3-interceptcurrentexception.md) yöntemi.

## <a name="requirements"></a>Gereksinimler
Üstbilgi: msdbg.h

Ad alanı: Microsoft.VisualStudio.Debugger.Interop

Derleme: Microsoft.VisualStudio.Debugger.Interop.dll

## <a name="see-also"></a>Ayrıca bkz.
- [Sabit Listeleri](../../../extensibility/debugger/reference/enumerations-visual-studio-debugging.md)
- [InterceptCurrentException](../../../extensibility/debugger/reference/idebugstackframe3-interceptcurrentexception.md)

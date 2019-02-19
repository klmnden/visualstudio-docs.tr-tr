---
title: CANSTOP_REASON | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
f1_keywords:
- CANSTOP_REASON
helpviewer_keywords:
- CANSTOP_REASON enumeration
ms.assetid: 6da944eb-36cd-4a8c-8d71-544c775cfcc1
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: 98621fbea4fc114616ccf23ada9b372c88461970
ms.sourcegitcommit: 7153e2fc717d32e0e9c8a9b8c406dc4053c9fd53
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/19/2019
ms.locfileid: "56413052"
---
# <a name="canstopreason"></a>CANSTOP_REASON
Bir program yürütme belirli bir noktaya ulaştıktan sonra yürütmeyi durdurmak, belirlemek için kullanılır.

## <a name="syntax"></a>Sözdizimi

```cpp
enum enum_CANSTOP_REASON {
    CANSTOP_ENTRYPOINT = 0x0000,
    CANSTOP_STEPIN     = 0x0001
};
typedef DWORD CANSTOP_REASON;
```

```csharp
public enum enum_CANSTOP_REASON {
    CANSTOP_ENTRYPOINT = 0x0000,
    CANSTOP_STEPIN     = 0x0001
};
```

## <a name="members"></a>Üyeler
CANSTOP_ENTRYPOINT  
Belirli bir programın giriş noktasını belirtir.

CANSTOP_STEPIN  
Bir işlevin Adımlama belirtir.

## <a name="remarks"></a>Açıklamalar
Bağımsız değişken olarak geçirilen [GetReason](../../../extensibility/debugger/reference/idebugcanstopevent2-getreason.md) oturum hata ayıklama Yöneticisi (SDM) ile programın giriş noktası ulaştıktan sonra veya bir işlev veya metot Adımlama durdurmak uygun olup olmadığını onaylamak için yöntemi.

## <a name="requirements"></a>Gereksinimler
Üstbilgi: msdbg.h

Ad alanı: Microsoft.VisualStudio.Debugger.Interop

Derleme: Microsoft.VisualStudio.Debugger.Interop.dll

## <a name="see-also"></a>Ayrıca Bkz.
[Sabit Listeleri](../../../extensibility/debugger/reference/enumerations-visual-studio-debugging.md)  
[GetReason](../../../extensibility/debugger/reference/idebugcanstopevent2-getreason.md)

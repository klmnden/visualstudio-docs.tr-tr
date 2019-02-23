---
title: DEBUG_REASON | Microsoft Docs
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- DEBUG_REASON
helpviewer_keywords:
- DEBUG_REASON enumeration
ms.assetid: ad2ee898-8648-4671-9078-d32873862346
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: 03b2db1fd58af6a8b2f8a57846e7753cdbc82352
ms.sourcegitcommit: b0d8e61745f67bd1f7ecf7fe080a0fe73ac6a181
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/22/2019
ms.locfileid: "56707269"
---
# <a name="debugreason"></a>DEBUG_REASON
Hata ayıklama için işlem neden başlatıldı belirtir.

## <a name="syntax"></a>Sözdizimi

```cpp
enum enum_DEBUG_REASON {
    DEBUG_REASON_ERROR         = 0,
    DEBUG_REASON_USER_LAUNCHED = 1,
    DEBUG_REASON_USER_ATTACHED = 2,
    DEBUG_REASON_AUTO_ATTACHED = 3,
    DEBUG_REASON_CAUSALITY     = 4
};
typedef DWORD DEBUG_REASON;
```

```csharp
public enum enum_DEBUG_REASON {
    DEBUG_REASON_ERROR         = 0,
    DEBUG_REASON_USER_LAUNCHED = 1,
    DEBUG_REASON_USER_ATTACHED = 2,
    DEBUG_REASON_AUTO_ATTACHED = 3,
    DEBUG_REASON_CAUSALITY     = 4
};
```

#### <a name="parameters"></a>Parametreler
DEBUG_REASON_ERROR bir özel olmayan bir hata oluştu (yok, diğer uygun neden olduğunda bu bir varsayılan koşul olarak kullanılır).

Kullanıcının talebi üzerine DEBUG_REASON_USER_LAUNCHED işlemi başlatıldı.

DEBUG_REASON_USER_ATTACHED zaten çalışan işlemi kullanıcı tarafından eklendi.

DEBUG_REASON_AUTO_ATTACHED işlemi başlatıldığında tarafından otomatik olarak depolamaya bağlanmıştır.

İşlem şu nedenle başlatıldı DEBUG_REASON_CAUSALITY bir *Just-ın-Time* (JIT) hata ayıklama olay.

## <a name="remarks"></a>Açıklamalar
Öğesinden döndürülen [GetDebugReason](../../../extensibility/debugger/reference/idebugprocess3-getdebugreason.md) yöntemi.

## <a name="requirements"></a>Gereksinimler
Üstbilgi: msdbg.h

Ad alanı: Microsoft.VisualStudio.Debugger.Interop

Derleme: Microsoft.VisualStudio.Debugger.Interop.dll

## <a name="see-also"></a>Ayrıca Bkz.
- [Sabit Listeleri](../../../extensibility/debugger/reference/enumerations-visual-studio-debugging.md)
- [GetDebugReason](../../../extensibility/debugger/reference/idebugprocess3-getdebugreason.md)

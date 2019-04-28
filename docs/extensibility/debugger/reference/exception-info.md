---
title: EXCEPTION_INFO | Microsoft Docs
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- EXCEPTION_INFO
helpviewer_keywords:
- EXCEPTION_INFO structure
ms.assetid: d046957a-b97d-420b-b46b-c67cbaef709e
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: 4c5863c9ebb790ebcbc267f62cc2a0a1fd14603c
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62924277"
---
# <a name="exceptioninfo"></a>EXCEPTION_INFO
Bir özel durum veya çalışma zamanı hata ayıklanacak program tarafından oluşturulan açıklar.

## <a name="syntax"></a>Sözdizimi

```cpp
typedef struct tagEXCEPTION_INFO {
    IDebugProgram2* pProgram;
    BSTR            bstrProgramName;
    BSTR            bstrExceptionName;
    DWORD           dwCode;
    EXCEPTION_STATE dwState;
    GUID            guidType;
} EXCEPTION_INFO;
```

```csharp
public struct EXCEPTION_INFO {
    public IDebugProgram2 pProgram;
    public string         bstrProgramName;
    public string         bstrExceptionName;
    public uint           dwCode;
    public uint           dwState;
    public Guid           guidType;
};
```

## <a name="members"></a>Üyeler
pProgram [IDebugProgram2](../../../extensibility/debugger/reference/idebugprogram2.md) özel durumun gerçekleştiği program temsil eden nesne.

programın adını bstrProgramName içinde özel durum oluştu.

bstrExceptionName özel durumun adı.

özel durum veya çalışma zamanı hatası kimlik kodunu dwCode.

dwState bir değerden [EXCEPTION_STATE](../../../extensibility/debugger/reference/exception-state.md) özel durumu tanımlayan sabit listesi.

guidType GUID dil tanımlayıcısı, ya da `guidLang` veya `guidEng`.

## <a name="remarks"></a>Açıklamalar
Bu yapı için bir parametre olarak geçirilen [SetException](../../../extensibility/debugger/reference/idebugengine2-setexception.md) ve [RemoveSetException](../../../extensibility/debugger/reference/idebugengine2-removesetexception.md) yöntemleri. Bu yapı ayrıca geçirilir [GetException](../../../extensibility/debugger/reference/idebugexceptionevent2-getexception.md) doldurulması için yöntemi.

## <a name="requirements"></a>Gereksinimler
Üstbilgi: msdbg.h

Ad alanı: Microsoft.VisualStudio.Debugger.Interop

Derleme: Microsoft.VisualStudio.Debugger.Interop.dll

## <a name="see-also"></a>Ayrıca Bkz.
- [Yapılar ve Birleşimler](../../../extensibility/debugger/reference/structures-and-unions.md)
- [EXCEPTION_STATE](../../../extensibility/debugger/reference/exception-state.md)
- [IDebugProgram2](../../../extensibility/debugger/reference/idebugprogram2.md)
- [SetException](../../../extensibility/debugger/reference/idebugengine2-setexception.md)
- [RemoveSetException](../../../extensibility/debugger/reference/idebugengine2-removesetexception.md)
- [GetException](../../../extensibility/debugger/reference/idebugexceptionevent2-getexception.md)

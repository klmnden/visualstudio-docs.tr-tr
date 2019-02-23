---
title: PROGRAM_DESTROY_FLAGS | Microsoft Docs
ms.date: 11/04/2016
ms.topic: reference
helpviewer_keywords:
- PROGRAM_DESTROY_FLAGS enumeration
ms.assetid: be00d4a3-d5b8-4159-b632-64577f534883
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: e232570edd4fcca95089324e30f3cbd725bdb9f8
ms.sourcegitcommit: b0d8e61745f67bd1f7ecf7fe080a0fe73ac6a181
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/22/2019
ms.locfileid: "56685618"
---
# <a name="programdestroyflags"></a>PROGRAM_DESTROY_FLAGS
Geçerli numaralandırır programının değerlerini bayrakları yok.

## <a name="syntax"></a>Sözdizimi

```cpp
enum enum_PPROGRAM_DESTROY_FLAGS
{
   PROGRAM_DESTROY_CONTINUE_DEBUGGING = 0x1
};
typedef DWORD PROGRAM_DESTROY_FLAGS;
```

```csharp
public enum enum_PPROGRAM_DESTROY_FLAGS
{
   PROGRAM_DESTROY_CONTINUE_DEBUGGING = 0x1
};
```

## <a name="terms"></a>Koşulları
 PROGRAM_DESTROY_CONTINUE_DEBUGGING yok programı, ancak hata ayıklamaya devam.

## <a name="remarks"></a>Açıklamalar
 Sabit listesi tarafından döndürülen [GetFlags](../../../extensibility/debugger/reference/idebugprogramdestroyeventflags2-getflags.md) yöntemi.

## <a name="requirements"></a>Gereksinimler
 Üst bilgi: Msdbg.h

 Ad alanı: Microsoft.VisualStudio.Debugger.Interop

 Derleme: Microsoft.VisualStudio.Debugger.Interop.dll

## <a name="see-also"></a>Ayrıca Bkz.
- [Sabit Listeleri](../../../extensibility/debugger/reference/enumerations-visual-studio-debugging.md)
- [GetFlags](../../../extensibility/debugger/reference/idebugprogramdestroyeventflags2-getflags.md)
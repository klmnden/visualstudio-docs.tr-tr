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
dev_langs:
- CPP
- CSharp
ms.openlocfilehash: 4d29522b942fae7e5bb5190c72eb989445f222d9
ms.sourcegitcommit: 19ec963ed6d585719cb83ba677434ea6580e0d1f
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/24/2019
ms.locfileid: "66212724"
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

## <a name="fields"></a>Alanlar
 `PROGRAM_DESTROY_CONTINUE_DEBUGGING`\
 Program yok, ancak hata ayıklamaya devam.

## <a name="remarks"></a>Açıklamalar
 Sabit listesi tarafından döndürülen [GetFlags](../../../extensibility/debugger/reference/idebugprogramdestroyeventflags2-getflags.md) yöntemi.

## <a name="requirements"></a>Gereksinimler
 Üst bilgi: Msdbg.h

 Ad alanı: Microsoft.VisualStudio.Debugger.Interop

 Derleme: Microsoft.VisualStudio.Debugger.Interop.dll

## <a name="see-also"></a>Ayrıca bkz.
- [Sabit Listeleri](../../../extensibility/debugger/reference/enumerations-visual-studio-debugging.md)
- [GetFlags](../../../extensibility/debugger/reference/idebugprogramdestroyeventflags2-getflags.md)
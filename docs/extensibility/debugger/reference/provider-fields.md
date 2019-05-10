---
title: PROVIDER_FIELDS | Microsoft Docs
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- PROVIDER_FIELDS
helpviewer_keywords:
- PROVIDER_FIELDS enumeration
ms.assetid: 39631545-2b0e-45b4-978b-d63656484b02
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
dev_langs:
- CPP
- CSharp
ms.openlocfilehash: 838a7dc0024e69335bf5c49c664bd491a6949d08
ms.sourcegitcommit: 50f0c3f2763a05de8482b3579026d9c76c0e226c
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/09/2019
ms.locfileid: "65460916"
---
# <a name="providerfields"></a>PROVIDER_FIELDS
Bir program sağlayıcı ile ilişkili özellikleri belirtir.

## <a name="syntax"></a>Sözdizimi

```cpp
enum enum_PROVIDER_FIELDS {
   PFIELD_PROGRAM_NODES       = 0x01,
   PFIELD_IS_DEBUGGER_PRESENT = 0x02
};
typedef DWORD PROVIDER_FIELDS;
```

```csharp
public enum enum_PROVIDER_FIELDS {
   PFIELD_PROGRAM_NODES       = 0x01,
   PFIELD_IS_DEBUGGER_PRESENT = 0x02
};
```

## <a name="fields"></a>Alanlar
 `PFIELD_PROGRAM_NODES`\
 `ProgramNodes` Alan geçerlidir.

 `PFIELD_IS_DEBUGGER_PRESENT`\
 `fIsDebuggerPresent` Alan geçerlidir.

## <a name="remarks"></a>Açıklamalar
 Bu değerleri döndürülür `Fields` üyesi [PROVIDER_PROCESS_DATA](../../../extensibility/debugger/reference/provider-process-data.md) yapısı yapının hangi alanların açıkça doldurulmuştur belirtmek için.

 Bu değerler, bit düzeyinde ile birleştirilebilir `OR`.

## <a name="requirements"></a>Gereksinimler
 Üstbilgi: msdbg.h

 Ad alanı: Microsoft.VisualStudio.Debugger.Interop

 Derleme: Microsoft.VisualStudio.Debugger.Interop.dll

## <a name="see-also"></a>Ayrıca bkz.
- [Sabit Listeleri](../../../extensibility/debugger/reference/enumerations-visual-studio-debugging.md)
- [PROVIDER_PROCESS_DATA](../../../extensibility/debugger/reference/provider-process-data.md)
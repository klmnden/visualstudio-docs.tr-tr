---
title: BP_LOCATION_TYPE | Microsoft Docs
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- BP_LOCATION_TYPE
helpviewer_keywords:
- BP_LOCATION_TYPE structure
ms.assetid: 0248430a-3b61-4809-87a9-e9b6bb7d1130
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: 1695c61a829cf1439ed773e48088430f36f8c653
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62924997"
---
# <a name="bplocationtype"></a>BP_LOCATION_TYPE
Bir kesme noktası istek için bir kesme noktası konumu türünü belirtir.

## <a name="syntax"></a>Sözdizimi

```cpp
enum enum_BP_LOCATION_TYPE {
    BPLT_NONE               = 0x00000000,
    BPLT_FILE_LINE          = 0x00010000,
    BPLT_FUNC_OFFSET        = 0x00020000,
    BPLT_CONTEXT            = 0x00030000,
    BPLT_STRING             = 0x00040000,
    BPLT_ADDRESS            = 0x00050000,
    BPLT_RESOLUTION         = 0x00060000,
    BPLT_CODE_FILE_LINE     = BPT_CODE | BPLT_FILE_LINE,
    BPLT_CODE_FUNC_OFFSET   = BPT_CODE | BPLT_FUNC_OFFSET,
    BPLT_CODE_CONTEXT       = BPT_CODE | BPLT_CONTEXT,
    BPLT_CODE_STRING        = BPT_CODE | BPLT_STRING,
    BPLT_CODE_ADDRESS       = BPT_CODE | BPLT_ADDRESS ,
    BPLT_DATA_STRING        = BPT_DATA | BPLT_STRING,
    BPLT_TYPE_MASK          = 0x0000FFFF,
    BPLT_LOCATION_TYPE_MASK = 0xFFFF0000
};
typedef DWORD BP_LOCATION_TYPE;
```

```csharp
public enum enum_BP_LOCATION_TYPE {
    BPLT_NONE               = 0x00000000,
    BPLT_FILE_LINE          = 0x00010000,
    BPLT_FUNC_OFFSET        = 0x00020000,
    BPLT_CONTEXT            = 0x00030000,
    BPLT_STRING             = 0x00040000,
    BPLT_ADDRESS            = 0x00050000,
    BPLT_RESOLUTION         = 0x00060000,
    BPLT_CODE_FILE_LINE     = BPT_CODE | BPLT_FILE_LINE,
    BPLT_CODE_FUNC_OFFSET   = BPT_CODE | BPLT_FUNC_OFFSET,
    BPLT_CODE_CONTEXT       = BPT_CODE | BPLT_CONTEXT,
    BPLT_CODE_STRING        = BPT_CODE | BPLT_STRING,
    BPLT_CODE_ADDRESS       = BPT_CODE | BPLT_ADDRESS ,
    BPLT_DATA_STRING        = BPT_DATA | BPLT_STRING,
    BPLT_TYPE_MASK          = 0x0000FFFF,
    BPLT_LOCATION_TYPE_MASK = 0xFFFF0000
};
```

## <a name="members"></a>Üyeler
BPLT_NONE hiçbir kesme noktası konumu belirtir.

BPLT_FILE_LINE bir dosya satır kesme noktası konumu türünü belirtir.

BPLT_FUNC_OFFSET işlevi offset kesme noktası konumu türünü belirtir.

BPLT_CONTEXT bağlamı olarak kesme noktası konumu türünü belirtir.

BPLT_STRING kesme noktası konum türü bir dize olarak belirtir.

BPLT_ADDRESS kesme noktası konum türü bir adresi belirtir.

BPLT_RESOLUTION bir çözüm kesme noktası konumu türünü belirtir.

BPLT_CODE_FILE_LINE bir kaynak kod satırı kesme noktası konumu türünü belirtir.

BPLT_CODE_FUNC_OFFSET kod işlevi offset kesme noktası konumu türünü belirtir.

BPLT_CODE_CONTEXT kod bağlamı olarak kesme noktası konumu türünü belirtir.

BPLT_CODE_STRING kesme noktası konum türü bir kod dize olarak belirtir.

BPLT_CODE_ADDRESS bir kod adresiyle kesme noktası konumu türünü belirtir.

BPLT_DATA_STRING kesme noktası konum türü verileri dize olarak belirtir.

BPLT_TYPE_MASK belirtir bir bit maskesi, böylece kesme noktası türü, değer dışında ayıklanabilir.

BPLT_LOCATION_TYPE_MASK belirtir bir bit maskesi, böylece kesme noktası konum türü değeri dışında ayıklanabilir.

## <a name="remarks"></a>Açıklamalar
Bir parametre olarak geçirilen [GetLocationType](../../../extensibility/debugger/reference/idebugbreakpointrequest2-getlocationtype.md) yöntemi.

Bir kesme noktası konum türü, bir kesme noktası türü ve konum türü oluşur. Bu bir kesme noktası konum türü hiçbir zaman yalnızca bir kesme noktası türü olduğu anlamına gelir (örneğin, `BPT_CODE`) veya bir konum türü (örneğin, `BPLT_FILE_LINE`). Şu anda desteklenen tüm kesme noktası konumu türleri için önceden tanımlanmış sabitleri bu numaralandırmada dahil edilir (`BPLT_CODE_FILE_LINE` aracılığıyla `BPLT_DATA_STRING`).

`BPT_CODE` ve `BPT_DATA` üyeleri [BP_TYPE](../../../extensibility/debugger/reference/bp-type.md) sabit listesi.

## <a name="requirements"></a>Gereksinimler
Üstbilgi: msdbg.h

Ad alanı: Microsoft.VisualStudio.Debugger.Interop

Derleme: Microsoft.VisualStudio.Debugger.Interop.dll

## <a name="see-also"></a>Ayrıca Bkz.
- [Sabit Listeleri](../../../extensibility/debugger/reference/enumerations-visual-studio-debugging.md)
- [GetLocationType](../../../extensibility/debugger/reference/idebugbreakpointrequest2-getlocationtype.md)
- [BP_TYPE](../../../extensibility/debugger/reference/bp-type.md)

---
title: PORT_SUPPLIER_DESCRIPTION_FLAGS | Microsoft Docs
ms.date: 11/04/2016
ms.topic: reference
helpviewer_keywords:
- PORT_SUPPLIER_DESCRIPTION_FLAGS enumeration
ms.assetid: 5acee0ee-3a20-41c9-a7dc-0dadae6a5ba5
author: madskristensen
ms.author: madsk
manager: jillfra
ms.workload:
- vssdk
dev_langs:
- CPP
- CSharp
ms.openlocfilehash: 01cf70b473d2c430741df2021d27b3047e782b79
ms.sourcegitcommit: 40d612240dc5bea418cd27fdacdf85ea177e2df3
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/29/2019
ms.locfileid: "66309479"
---
# <a name="portsupplierdescriptionflags"></a>PORT_SUPPLIER_DESCRIPTION_FLAGS

Bağlantı noktası sağlayıcısı hakkında alınabilir meta verileri tanımlar.

## <a name="syntax"></a>Sözdizimi

```cpp
enum enum_PORT_SUPPLIER_DESCRIPTION_FLAGS
{
    PSDFLAG_SHOW_WARNING_ICON = 0x1
};
typedef DWORD PORT_SUPPLIER_DESCRIPTION_FLAGS;
```

```csharp
public enum enum_PORT_SUPPLIER_DESCRIPTION_FLAGS
{
    PSDFLAG_SHOW_WARNING_ICON = 0x1
};
```

## <a name="fields"></a>Alanlar

`PSDFLAG_SHOW_WARNING_ICON`\
Seçili değilse kullanıcı Arabiriminde uyarı simgesi görüntülenir.

## <a name="remarks"></a>Açıklamalar

Bu sabit listesi tarafından döndürülen [GetDescription](../../../extensibility/debugger/reference/idebugportsupplierdescription2-getdescription.md) yöntemi.

## <a name="requirements"></a>Gereksinimler

Üst bilgi: Msdbg.h

Ad alanı: Microsoft.VisualStudio.Debugger.Interop

Derleme: Microsoft.VisualStudio.Debugger.Interop.dll

## <a name="see-also"></a>Ayrıca bkz.

- [Sabit Listeleri](../../../extensibility/debugger/reference/enumerations-visual-studio-debugging.md)
- [GetDescription](../../../extensibility/debugger/reference/idebugportsupplierdescription2-getdescription.md)

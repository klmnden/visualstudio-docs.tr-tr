---
title: MESSAGETYPE | Microsoft Docs
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- MESSAGETYPE
helpviewer_keywords:
- MESSAGETYPE enumeration
ms.assetid: 800cc77d-3c27-4763-a9df-552a9384bd49
author: madskristensen
ms.author: madsk
manager: jillfra
ms.workload:
- vssdk
dev_langs:
- CPP
- CSharp
ms.openlocfilehash: 8c17860bb47f493031e6db1134aec498611b07f1
ms.sourcegitcommit: 40d612240dc5bea418cd27fdacdf85ea177e2df3
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/29/2019
ms.locfileid: "66339200"
---
# <a name="messagetype"></a>MESSAGETYPE
Neden ve ileti türünü belirtir.

## <a name="syntax"></a>Sözdizimi

```cpp
enum enum_MESSAGETYPE { 
   MT_OUTPUTSTRING      = 0x0000001,
   MT_MESSAGEBOX        = 0x00000002,
   MT_TYPE_MASK         = 0x000000FF,
   MT_REASON_EXCEPTION  = 0x00000100,
   MT_REASON_TRACEPOINT = 0x00000200,
   MT_REASON_MASK       = 0x0000FF00
};
typedef DWORD MESSAGETYPE;
```

```csharp
public enum enum_MESSAGETYPE { 
   MT_OUTPUTSTRING      = 0x0000001,
   MT_MESSAGEBOX        = 0x00000002,
   MT_TYPE_MASK         = 0x000000FF,
   MT_REASON_EXCEPTION  = 0x00000100,
   MT_REASON_TRACEPOINT = 0x00000200,
   MT_REASON_MASK       = 0x0000FF00
};
```

## <a name="fields"></a>Alanlar
 `MT_OUTPUTSTRING`\
 İleti için çıkış penceresine gönderilen olduğunu gösterir. Bu gelen birbirini dışlayan `MT_MESSAGEBOX`.

 `MT_MESSAGEBOX`\
 İleti bir ileti kutusunda gösterilecek gösterir. Bu gelen birbirini dışlayan `MT_OUTPUTSTRING`.

 `MT_TYPE_MASK`\
 İleti için hedef yalıtmak için bir maske değeri.

 `MT_REASON_EXCEPTION`\
 Bir özel durum sonucu olarak bir ileti kutusu gösterilmekte olduğunu gösterir. Bu gelen birbirini dışlayan `MT_REASON_TRACEPOINT`.

 `MT_REASON_TRACEPOINT`\
 Bir ileti kutusu sonucunda bir izleme noktasına ulaşma gösterilmekte olduğunu gösterir. Bu birbirini dışlayan olan `MT_REASON_EXCEPTION`.

 `MT_REASON_MASK`\
 Gösterilen iletiyi nedeni yalıtmak için bir maske değeri.

## <a name="remarks"></a>Açıklamalar
 Bu değerleri döndürülen [GetMessage](../../../extensibility/debugger/reference/idebugmessageevent2-getmessage.md) ve [GetErrorMessage](../../../extensibility/debugger/reference/idebugerrorevent2-geterrormessage.md) yöntemleri.

 Neden değerlerinden birleştirilebilir bit düzeyinde kullanarak çıkış hedef değerlerden biriyle `OR`.

## <a name="requirements"></a>Gereksinimler
 Üstbilgi: msdbg.h

 Ad alanı: Microsoft.VisualStudio.Debugger.Interop

 Derleme: Microsoft.VisualStudio.Debugger.Interop.dll

## <a name="see-also"></a>Ayrıca bkz.
- [Sabit Listeleri](../../../extensibility/debugger/reference/enumerations-visual-studio-debugging.md)
- [GetMessage](../../../extensibility/debugger/reference/idebugmessageevent2-getmessage.md)
- [GetErrorMessage](../../../extensibility/debugger/reference/idebugerrorevent2-geterrormessage.md)
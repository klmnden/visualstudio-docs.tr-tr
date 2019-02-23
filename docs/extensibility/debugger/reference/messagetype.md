---
title: MESSAGETYPE | Microsoft Docs
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- MESSAGETYPE
helpviewer_keywords:
- MESSAGETYPE enumeration
ms.assetid: 800cc77d-3c27-4763-a9df-552a9384bd49
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: 16d2b9ae9c446d4c8082a8c35c9e4d1810233b95
ms.sourcegitcommit: b0d8e61745f67bd1f7ecf7fe080a0fe73ac6a181
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/22/2019
ms.locfileid: "56687516"
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

## <a name="members"></a>Üyeler
 MT_OUTPUTSTRING için çıkış penceresine ileti gönderilmesi gerektiğini gösterir. Bu gelen birbirini dışlayan `MT_MESSAGEBOX`.

 İleti bir ileti kutusunda gösterilecek MT_MESSAGEBOX gösterir. Bu gelen birbirini dışlayan `MT_OUTPUTSTRING`.

 İleti için hedef yalıtmak için bir maske değeri MT_TYPE_MASK.

 MT_REASON_EXCEPTION bir özel durum sonucu olarak görüntülenen bir ileti kutusu gösterir. Bu gelen birbirini dışlayan `MT_REASON_TRACEPOINT`.

 MT_REASON_TRACEPOINT bir izleme noktasına ulaşma sonucu olarak bir ileti kutusu gösterilmekte olduğunu gösterir. Bu birbirini dışlayan olan `MT_REASON_EXCEPTION`.

 Gösterilen iletiyi nedeni yalıtmak için bir maske değeri MT_REASON_MASK.

## <a name="remarks"></a>Açıklamalar
 Bu değerleri döndürülen [GetMessage](../../../extensibility/debugger/reference/idebugmessageevent2-getmessage.md) ve [GetErrorMessage](../../../extensibility/debugger/reference/idebugerrorevent2-geterrormessage.md) yöntemleri.

 Neden değerlerinden birleştirilebilir bit düzeyinde kullanarak çıkış hedef değerlerden biriyle `OR`.

## <a name="requirements"></a>Gereksinimler
 Üstbilgi: msdbg.h

 Ad alanı: Microsoft.VisualStudio.Debugger.Interop

 Derleme: Microsoft.VisualStudio.Debugger.Interop.dll

## <a name="see-also"></a>Ayrıca Bkz.
- [Sabit Listeleri](../../../extensibility/debugger/reference/enumerations-visual-studio-debugging.md)
- [GetMessage](../../../extensibility/debugger/reference/idebugmessageevent2-getmessage.md)
- [GetErrorMessage](../../../extensibility/debugger/reference/idebugerrorevent2-geterrormessage.md)
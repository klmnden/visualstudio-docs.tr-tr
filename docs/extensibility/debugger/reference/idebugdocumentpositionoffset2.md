---
title: IDebugDocumentPositionOffset2 | Microsoft Docs
ms.date: 11/04/2016
ms.topic: reference
helpviewer_keywords:
- IDebugDocumentPositionOffset2 interface
ms.assetid: f1b05db3-50d8-453f-a72f-e68b239236a4
author: madskristensen
ms.author: madsk
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: 3793d54249fca1dc867cfe4072326245a67852cb
ms.sourcegitcommit: 40d612240dc5bea418cd27fdacdf85ea177e2df3
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/29/2019
ms.locfileid: "66333265"
---
# <a name="idebugdocumentpositionoffset2"></a>IDebugDocumentPositionOffset2
Bir karakter uzaklığı olarak kaynak dosyada bir konumu temsil eder.

## <a name="syntax"></a>Sözdizimi

```
IDebugDocumentPositionOffset2 : IUnknown
```

## <a name="notes-for-implementers"></a>Uygulayanlar için Notlar
 IDE tarafından uygulanan ve hata ayıklama motoru tarafından tüketilen.

## <a name="methods"></a>Yöntemler
 Aşağıdaki tabloda yöntemlerini gösterilmektedir `IDebugDocumentPositionOffset2`.

|Yöntem|Açıklama|
|------------|-----------------|
|[GetRange](../../../extensibility/debugger/reference/idebugdocumentpositionoffset2-getrange.md)|Geçerli belge konumunu aralığını alır.|

## <a name="remarks"></a>Açıklamalar
 Bu aynı bilgileri döndürür [GetRange](../../../extensibility/debugger/reference/idebugdocumentposition2-getrange.md) ancak `char` belgenin başından kaydırır. Bu bir diskte diğer bir deyişle, normalde döndürülen satır ve sütun bilgisi yerine karakterlerin tek boyutlu dizi var gibi bu belgeyi sunar.

## <a name="requirements"></a>Gereksinimler
 Üst bilgi: Msdbg.h

 Ad alanı: Microsoft.VisualStudio.Debugger.Interop

 Derleme: Microsoft.VisualStudio.Debugger.Interop.dll

## <a name="see-also"></a>Ayrıca bkz.
- [IDebugDocumentPosition2](../../../extensibility/debugger/reference/idebugdocumentposition2.md)
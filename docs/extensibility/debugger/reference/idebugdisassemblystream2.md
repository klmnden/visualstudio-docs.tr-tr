---
title: IDebugDisassemblyStream2 | Microsoft Docs
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- IDebugDisassemblyStream2
helpviewer_keywords:
- IDebugDisassemblyStream2 interface
ms.assetid: b03cab0c-3f0b-4cc6-88dc-acb3b48c567a
author: madskristensen
ms.author: madsk
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: cf91235b1321b13571505c51af077643c606c4a7
ms.sourcegitcommit: 40d612240dc5bea418cd27fdacdf85ea177e2df3
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/29/2019
ms.locfileid: "66310304"
---
# <a name="idebugdisassemblystream2"></a>IDebugDisassemblyStream2
Bu arabirim, yönergelerin akışını temsil eder.

## <a name="syntax"></a>Sözdizimi

```
IDebugDisassemblyStream2 : IUnknown
```

## <a name="notes-for-implementers"></a>Uygulayanlar için Notlar
 Hata ayıklama altyapısı, bir programın kod ayrıştırılmış kodu desteklemek için bu arabirimi uygular.

## <a name="notes-for-callers"></a>Arayanlar İçin Notlar
 Bir çağrı [GetDisassemblyStream](../../../extensibility/debugger/reference/idebugprogram2-getdisassemblystream.md) yöntemi bu arabirimi döndürür.

## <a name="methods-in-vtable-order"></a>Vtable sırayla yöntemleri
 Aşağıdaki tabloda yöntemlerini gösterilmektedir `IDebugDisassemblyStream2`.

|Yöntem|Açıklama|
|------------|-----------------|
|[Read](../../../extensibility/debugger/reference/idebugdisassemblystream2-read.md)|Ayrıştırılmış kodu stream'de geçerli konumundan başlayarak yönergeleri okur.|
|[Seek](../../../extensibility/debugger/reference/idebugdisassemblystream2-seek.md)|Ayrıştırılmış kod akış yönergeler belirtilen konuma göre verilen sayıda okuma imleci taşır.|
|[GetCodeLocationId](../../../extensibility/debugger/reference/idebugdisassemblystream2-getcodelocationid.md)|Belirli kod bağlamı için bir kod konum tanımlayıcısı döndürür.|
|[GetCodeContext](../../../extensibility/debugger/reference/idebugdisassemblystream2-getcodecontext.md)|Belirtilen kod konumu tanımlayıcısına karşılık gelen bir kod bağlam nesnesi döndürür.|
|[GetCurrentLocation](../../../extensibility/debugger/reference/idebugdisassemblystream2-getcurrentlocation.md)|Geçerli kod konumu temsil eden bir kod konum tanımlayıcısı döndürür.|
|[GetDocument](../../../extensibility/debugger/reference/idebugdisassemblystream2-getdocument.md)|Bu çözümü stream ile ilişkili kaynak belge alır.|
|[GetScope](../../../extensibility/debugger/reference/idebugdisassemblystream2-getscope.md)|Bu çözümü akış kapsamı alır.|
|[GetSize](../../../extensibility/debugger/reference/idebugdisassemblystream2-getsize.md)|Bu çözümü akış boyutunu alır.|

## <a name="remarks"></a>Açıklamalar
 Ayrıştırılmış kod akışı, tüm adres veya yalnızca bir işlev veya modül alanı içinde temsil etmek için oluşturulabilir. Her yönerge tarafından temsil edilen bir [DisassemblyData](../../../extensibility/debugger/reference/disassemblydata.md) yapısı için bir çağrı tarafından döndürülen [okuma](../../../extensibility/debugger/reference/idebugdisassemblystream2-read.md) yöntemi.

## <a name="requirements"></a>Gereksinimler
 Üstbilgi: msdbg.h

 Ad alanı: Microsoft.VisualStudio.Debugger.Interop

 Derleme: Microsoft.VisualStudio.Debugger.Interop.dll

## <a name="see-also"></a>Ayrıca bkz.
- [Temel Arabirimler](../../../extensibility/debugger/reference/core-interfaces.md)
- [GetDisassemblyStream](../../../extensibility/debugger/reference/idebugprogram2-getdisassemblystream.md)
- [DisassemblyData](../../../extensibility/debugger/reference/disassemblydata.md)
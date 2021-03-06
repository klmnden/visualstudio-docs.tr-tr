---
title: IDebugDocumentText2 | Microsoft Docs
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- IDebugDocumentText2
helpviewer_keywords:
- IDebugDocumentText2 interface
ms.assetid: e85f50a3-211c-4220-a9f4-789950ba2782
author: madskristensen
ms.author: madsk
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: 43716ce3b01464d2937fd75ce90ec5028679ef47
ms.sourcegitcommit: 40d612240dc5bea418cd27fdacdf85ea177e2df3
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/29/2019
ms.locfileid: "66330639"
---
# <a name="idebugdocumenttext2"></a>IDebugDocumentText2
Bu arabirim, bir metin belgesi temsil eder.

## <a name="syntax"></a>Sözdizimi

```
IDebugDocumentText2 : IDebugDocument2
```

## <a name="notes-for-implementers"></a>Uygulayanlar için Notlar
 Metin biçiminde sağlaması gerekir kaynak kodu olduğunda, hata ayıklama altyapısı (DE) Bu arabirim uygular. Bir DE kullanılıyorsa, bu en sık karşılaşılan durum olduğundan [IDebugDocument2](../../../extensibility/debugger/reference/idebugdocument2.md) arabirimi, bu da uygulamanız gerekir `IDebugDocumentText2` arabirimi.

## <a name="notes-for-callers"></a>Arayanlar İçin Notlar
 Kullanım `QueryInterface` bu arabirimden elde etmek için yöntemi bir `IDebugDocument2` arabirimi.

## <a name="methods-in-vtable-order"></a>Vtable sırayla yöntemleri
 Yöntemlere ek olarak `IDebugDocument2` arabirimi bu arabirim, aşağıdaki yöntemleri uygular:

|Yöntem|Açıklama|
|------------|-----------------|
|[GetSize](../../../extensibility/debugger/reference/idebugdocumenttext2-getsize.md)|Belgedeki bu konumda metin boyutunu alır.|
|[GetText](../../../extensibility/debugger/reference/idebugdocumenttext2-gettext.md)|Belge belirtilen konumda metin alır.|

## <a name="remarks"></a>Açıklamalar
 Bu arabirimi uygulayan bir nesne de uygulamalıdır <xref:System.Runtime.InteropServices.ComTypes.IConnectionPointContainer> arabirim, hangi kaynakları <xref:System.Runtime.InteropServices.ComTypes.IConnectionPoint> için arabirim bir [IDebugDocumentTextEvents2](../../../extensibility/debugger/reference/idebugdocumenttextevents2.md) nesne.

## <a name="requirements"></a>Gereksinimler
 Üstbilgi: msdbg.h

 Ad alanı: Microsoft.VisualStudio.Debugger.Interop

 Derleme: Microsoft.VisualStudio.Debugger.Interop.dll

## <a name="see-also"></a>Ayrıca bkz.
- [IDebugDocument2](../../../extensibility/debugger/reference/idebugdocument2.md)
- [IDebugDocumentTextEvents2](../../../extensibility/debugger/reference/idebugdocumenttextevents2.md)
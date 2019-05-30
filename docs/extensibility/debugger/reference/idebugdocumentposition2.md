---
title: IDebugDocumentPosition2 | Microsoft Docs
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- IDebugDocumentPosition2
helpviewer_keywords:
- IDebugDocumentPosition2 interface
ms.assetid: 0e838ced-12bb-4efc-b811-2b7c034b77b0
author: madskristensen
ms.author: madsk
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: 36c2fbce0154a5ebefd04ea3614d16db16799510
ms.sourcegitcommit: 40d612240dc5bea418cd27fdacdf85ea177e2df3
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/29/2019
ms.locfileid: "66333430"
---
# <a name="idebugdocumentposition2"></a>IDebugDocumentPosition2
Bu arabirim, kaynak dosyada soyut bir konumu temsil eder.

## <a name="syntax"></a>Sözdizimi

```
IDebugDocumentPosition2 : IUnknown
```

## <a name="notes-for-implementers"></a>Uygulayanlar için Notlar
 Visual Studio, genellikle bu arabirimi uygular. Kendi kaynak kodu sağlamalısınız, hata ayıklama altyapısı (DE) da bu arabirimi uygulayan (ne DE uygular olarak [IDebugDocument2](../../../extensibility/debugger/reference/idebugdocument2.md) arabirimi).

## <a name="notes-for-callers"></a>Arayanlar İçin Notlar
 Bu arabirim için bağımsız değişken olarak geçirilen [EnumCodeContexts](../../../extensibility/debugger/reference/idebugprogram2-enumcodecontexts.md). Ayrıca bir parçası olarak sağlanan bir [BP_LOCATION](../../../extensibility/debugger/reference/bp-location.md) birleşim (özellikle bir [BP_LOCATION_CODE_FILE_LINE](../../../extensibility/debugger/reference/bp-location-code-file-line.md) yapısı) sırayla parçası olan [BP_REQUEST_INFO](../../../extensibility/debugger/reference/bp-request-info.md) yapısı Bu, bir bekleyen kesme noktasının oluşturulurken kullanılır.

## <a name="methods-in-vtable-order"></a>Vtable sırayla yöntemleri
 Aşağıdaki tabloda yöntemlerini gösterilmektedir `IDebugDocumentPosition2`.

|Yöntem|Açıklama|
|------------|-----------------|
|[GetFileName](../../../extensibility/debugger/reference/idebugdocumentposition2-getfilename.md)|Bu belge konumu içeren kaynak dosyasının dosya adını alır.|
|[GetDocument](../../../extensibility/debugger/reference/idebugdocumentposition2-getdocument.md)|İçeren belge alır.|
|[IsPositionInDocument](../../../extensibility/debugger/reference/idebugdocumentposition2-ispositionindocument.md)|Bu konum verilen belgedeki dahil olup olmadığını belirler.|
|[GetRange](../../../extensibility/debugger/reference/idebugdocumentposition2-getrange.md)|Aralık, bu belgenin konumunu alır.|

## <a name="requirements"></a>Gereksinimler
 Üstbilgi: msdbg.h

 Ad alanı: Microsoft.VisualStudio.Debugger.Interop

 Derleme: Microsoft.VisualStudio.Debugger.Interop.dll

## <a name="see-also"></a>Ayrıca bkz.
- [EnumCodeContexts](../../../extensibility/debugger/reference/idebugprogram2-enumcodecontexts.md)
- [IDebugProgram2](../../../extensibility/debugger/reference/idebugprogram2.md)
- [BP_LOCATION_CODE_FILE_LINE](../../../extensibility/debugger/reference/bp-location-code-file-line.md)
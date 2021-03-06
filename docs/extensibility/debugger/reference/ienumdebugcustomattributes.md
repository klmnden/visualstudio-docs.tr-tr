---
title: IEnumDebugCustomAttributes | Microsoft Docs
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- IEnumCustomAttributes
helpviewer_keywords:
- IEnumDebugCustomAttributes interface
ms.assetid: 11aa768d-1852-44d6-9de3-17f9bafaded2
author: madskristensen
ms.author: madsk
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: e706999595033ac76508eaa5e3b3f995839ceaea
ms.sourcegitcommit: 40d612240dc5bea418cd27fdacdf85ea177e2df3
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/29/2019
ms.locfileid: "66321550"
---
# <a name="ienumdebugcustomattributes"></a>IEnumDebugCustomAttributes
Özel öznitelikleri numaralandırır.

## <a name="syntax"></a>Sözdizimi

```
IEnumCustomAttributes : IUnknown
```

## <a name="notes-for-implementers"></a>Uygulayanlar için Notlar
 Sembol sağlayıcısı özel öznitelikler desteklemek için bu arabirimi uygulayan (aracılığıyla [IDebugCustomAttribute](../../../extensibility/debugger/reference/idebugcustomattribute.md) arabirimi).

## <a name="notes-for-callers"></a>Arayanlar İçin Notlar
- [EnumCustomAttributes](../../../extensibility/debugger/reference/idebugcustomattributequery2-enumcustomattributes.md) bu arabirimi döndürür.

## <a name="methods-in-vtable-order"></a>Vtable sırayla yöntemleri
 Aşağıdaki tabloda yöntemlerini gösterilmektedir `IEnumDebugCustomAttributes`.

|Yöntem|Açıklama|
|------------|-----------------|
|[Next](../../../extensibility/debugger/reference/ienumdebugcustomattributes-next.md)|Özel özniteliklerin bir numaralandırma dizisinde belirtilen bir sayı alır.|
|[Skip](../../../extensibility/debugger/reference/ienumdebugcustomattributes-skip.md)|Özel öznitelikler bir numaralandırma dizisinde belirtilen sayıda atlar.|
|[Reset](../../../extensibility/debugger/reference/ienumdebugcustomattributes-reset.md)|Bir numaralandırma sıralı başlangıç durumuna sıfırlar.|
|[Clone](../../../extensibility/debugger/reference/ienumdebugcustomattributes-clone.md)|Geçerli Numaralandırıcı aynı numaralandırma duruma içeren bir numaralandırıcı oluşturur.|
|[GetCount](../../../extensibility/debugger/reference/ienumdebugcustomattributes-getcount.md)|Özel öznitelik sayısı bir numaralandırıcı alır.|

## <a name="requirements"></a>Gereksinimler
 Üstbilgi: sh.h

 Ad alanı: Microsoft.VisualStudio.Debugger.Interop

 Derleme: Microsoft.VisualStudio.Debugger.Interop.dll

## <a name="see-also"></a>Ayrıca bkz.
- [Sembol Sağlayıcısı Arabirimleri](../../../extensibility/debugger/reference/symbol-provider-interfaces.md)
- [EnumCustomAttributes](../../../extensibility/debugger/reference/idebugcustomattributequery2-enumcustomattributes.md)
- [IDebugCustomAttribute](../../../extensibility/debugger/reference/idebugcustomattribute.md)
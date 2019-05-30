---
title: IEnumDebugFrameInfo2 | Microsoft Docs
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- IEnumDebugFrameInfo2
helpviewer_keywords:
- IEnumDebugFrameInfo2
ms.assetid: 994e30ad-435a-4f9e-9272-d96d9e01099c
author: madskristensen
ms.author: madsk
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: 6579481f44006cc3f77e57a9c9ecbd327c3b7409
ms.sourcegitcommit: 40d612240dc5bea418cd27fdacdf85ea177e2df3
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/29/2019
ms.locfileid: "66350288"
---
# <a name="ienumdebugframeinfo2"></a>IEnumDebugFrameInfo2
Bu arabirim numaralandırır [FRAMEINFO](../../../extensibility/debugger/reference/frameinfo.md) yapıları.

## <a name="syntax"></a>Sözdizimi

```
IEnumDebugFrameInfo2 : IUnknown
```

## <a name="notes-for-implementers"></a>Uygulayanlar için Notlar
 Hata ayıklama altyapısı (DE), geçerli çağrı yığınını açıklayan yapıların listesini sağlamak için bu arabirimi uygular.

## <a name="notes-for-callers"></a>Arayanlar İçin Notlar
 Visual Studio çağrıları [EnumFrameInfo](../../../extensibility/debugger/reference/idebugthread2-enumframeinfo.md) bir kesme noktası olduğunda bu arabirimi almak için özel durum ya da durdurmak ayıklanan bir programda gerçekleşir.

## <a name="methods-in-vtable-order"></a>Vtable sırayla yöntemleri
 Aşağıdaki tabloda yöntemlerini gösterilmektedir `IEnumDebugFrameInfo2`.

|Yöntem|Açıklama|
|------------|-----------------|
|[Next](../../../extensibility/debugger/reference/ienumdebugframeinfo2-next.md)|Belirtilen sayıda alır [FRAMEINFO](../../../extensibility/debugger/reference/frameinfo.md) yapıları, bir sabit listesi sırası.|
|[Skip](../../../extensibility/debugger/reference/ienumdebugframeinfo2-skip.md)|Belirtilen sayıda atlar [FRAMEINFO](../../../extensibility/debugger/reference/frameinfo.md) yapıları, bir sabit listesi sırası.|
|[Reset](../../../extensibility/debugger/reference/ienumdebugframeinfo2-reset.md)|Bir numaralandırma sıralı başlangıç durumuna sıfırlar.|
|[Clone](../../../extensibility/debugger/reference/ienumdebugframeinfo2-clone.md)|Geçerli Numaralandırıcı aynı numaralandırma duruma içeren bir numaralandırıcı oluşturur.|
|[GetCount](../../../extensibility/debugger/reference/ienumdebugframeinfo2-getcount.md)|Sayısını alır [FRAMEINFO](../../../extensibility/debugger/reference/frameinfo.md) yapılarda bir numaralandırıcı.|

## <a name="remarks"></a>Açıklamalar
 Visual Studio bu arabirim, bir kesme noktası, özel durum veya hata ayıklanan programa duraklatma kullanıcı tarafından oluşturulan işleme ilk adımı olarak alır. Listesini [FRAMEINFO](../../../extensibility/debugger/reference/frameinfo.md) yapılarını temsil eder, geçerli çağrı yığınını, liste ve eski işlevin başında geçerli işlev çağrısıyla listesinin sonunda çağırın. Her `FRAMEINFO` ifade değerlendirmesi yapılamıyor ve yerel değişkenler baktığı konumunda bir bağlamı bir yığın çerçevesini temsil eder.

## <a name="requirements"></a>Gereksinimler
 Üstbilgi: msdbg.h

 Ad alanı: Microsoft.VisualStudio.Debugger.Interop

 Derleme: Microsoft.VisualStudio.Debugger.Interop.dll

## <a name="see-also"></a>Ayrıca bkz.
- [Temel Arabirimler](../../../extensibility/debugger/reference/core-interfaces.md)
- [EnumFrameInfo](../../../extensibility/debugger/reference/idebugthread2-enumframeinfo.md)
- [FRAMEINFO](../../../extensibility/debugger/reference/frameinfo.md)
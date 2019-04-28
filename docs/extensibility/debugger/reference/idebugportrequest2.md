---
title: IDebugPortRequest2 | Microsoft Docs
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- IDebugPortRequest2
helpviewer_keywords:
- IDebugPortRequest2 interface
ms.assetid: 556e610d-7c4b-44a8-965a-76a9d02b601a
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: 8e2b78986b997358d7f15c9c8c73bb4bd0f73aaf
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62871486"
---
# <a name="idebugportrequest2"></a>IDebugPortRequest2
Bu arabirim bir bağlantı noktası açıklar. Bu açıklama, bağlantı noktası için bağlantı noktası sağlayıcısı eklemek için kullanılır.

## <a name="syntax"></a>Sözdizimi

```
IDebugPortRequest2 : IUnknown
```

## <a name="notes-for-implementers"></a>Uygulayanlar için Notlar
 Visual Studio, genellikle hata ayıklama bağlantı noktası bağlantı noktası sağlayıcısı alma işleminde bu arabirimi uygular.

## <a name="notes-for-callers"></a>Arayanlar İçin Notlar
 Bu arabirim yöntemlere geçirilen [AddPort](../../../extensibility/debugger/reference/idebugportsupplier2-addport.md) hata ayıklama bağlantı oluşturmak için. Bir çağrı [GetPortRequest](../../../extensibility/debugger/reference/idebugport2-getportrequest.md) ilk başta bağlantı noktası oluşturmak için kullanılan istek temsil eden bu arabirimi döndürür.

## <a name="methods-in-vtable-order"></a>Vtable sırayla yöntemleri
 Aşağıdaki tabloda yöntemlerini gösterilmektedir `IDebugPortRequest2`.

|Yöntem|Açıklama|
|------------|-----------------|
|[GetPortName](../../../extensibility/debugger/reference/idebugportrequest2-getportname.md)|Oluşturmak için bağlantı noktası adını alır.|

## <a name="remarks"></a>Açıklamalar
 Hata ayıklama altyapısı genellikle bağlantı noktası sağlayıcısı ile etkileşime girmez ve bu arabirim için herhangi bir kullanıma sahip olur.

## <a name="requirements"></a>Gereksinimler
 Üstbilgi: msdbg.h

 Ad alanı: Microsoft.VisualStudio.Debugger.Interop

 Derleme: Microsoft.VisualStudio.Debugger.Interop.dll

## <a name="see-also"></a>Ayrıca Bkz.
- [Temel Arabirimler](../../../extensibility/debugger/reference/core-interfaces.md)
- [AddPort](../../../extensibility/debugger/reference/idebugportsupplier2-addport.md)
- [GetPortRequest](../../../extensibility/debugger/reference/idebugport2-getportrequest.md)
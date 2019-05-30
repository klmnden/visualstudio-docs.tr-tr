---
title: IDebugProcessSecurity | Microsoft Docs
ms.date: 11/04/2016
ms.topic: reference
helpviewer_keywords:
- IDebugProcessSecurity interface
ms.assetid: 8a52ddca-bd99-49c0-9778-469dce7abd44
author: madskristensen
ms.author: madsk
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: 74202c4342ae5880f277299b6bb94dcdadff26f5
ms.sourcegitcommit: 40d612240dc5bea418cd27fdacdf85ea177e2df3
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/29/2019
ms.locfileid: "66311415"
---
# <a name="idebugprocesssecurity"></a>IDebugProcessSecurity
`IDebugProcessSecurity` işleme iliştirdikten güvenli olduğunu kullanıcıyı uyarmak için bağlantı noktası sağlayıcısı tarafından uygulanır.

## <a name="syntax"></a>Sözdizimi

```
IDebugProcessSecurity : IUnknown
```

## <a name="methods-in-vtable-order"></a>Vtable sırayla yöntemleri
 Aşağıdaki tabloda yöntemlerini gösterilmektedir `IDebugProcessSecurity`.

|Yöntem|Açıklama|
|------------|-----------------|
|[GetUserName](../../../extensibility/debugger/reference/idebugprocesssecurity-getusername.md)|Kullanıcı adı bağlantı noktası tedarikçiden alır.|
|[QueryCanSafelyAttach](../../../extensibility/debugger/reference/idebugprocesssecurity-querycansafelyattach.md)|Hata ayıklama işlemine iliştirme'güvenli olmayan bir kullanıcıyı uyarır.|

## <a name="remarks"></a>Açıklamalar
 Bir uyarı gösterir ve kullanıcının olduğu iliştirmekte olduğunuz işlemin güvensiz kabul edilebilir iptal izin vermek için bu arabirimi uygulayın.

## <a name="requirements"></a>Gereksinimler
 Üstbilgi: msdbg.h

 Ad alanı: Microsoft.VisualStudio.Debugger.Interop

 Derleme: Microsoft.VisualStudio.Debugger.Interop.dll

## <a name="see-also"></a>Ayrıca bkz.
- [Bağlantı Noktaları](../../../extensibility/debugger/ports.md)
- [Bağlantı Noktası Sağlayıcıları](../../../extensibility/debugger/port-suppliers.md)
- [Temel Arabirimler](../../../extensibility/debugger/reference/core-interfaces.md)
- [IDebugProcess2](../../../extensibility/debugger/reference/idebugprocess2.md)
---
title: IDebugThread2::EnumFrameInfo | Microsoft Docs
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- IDebugThread2::EnumFrameInfo
helpviewer_keywords:
- IDebugThread2::EnumFrameInfo
ms.assetid: 17914a71-10ea-4b6f-8982-e364f87dca53
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
dev_langs:
- CPP
- CSharp
ms.openlocfilehash: 1954a66c5104ec96b9b941e8bd1171c1fba88003
ms.sourcegitcommit: 19ec963ed6d585719cb83ba677434ea6580e0d1f
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/24/2019
ms.locfileid: "66199711"
---
# <a name="idebugthread2enumframeinfo"></a>IDebugThread2::EnumFrameInfo
Bu iş parçacığı için yığın çerçevesi bir listesini alır.

## <a name="syntax"></a>Sözdizimi

```cpp
HRESULT EnumFrameInfo ( 
   FRAMEINFO_FLAGS        dwFieldSpec,
   UINT                   nRadix,
   IEnumDebugFrameInfo2** ppEnum
);
```

```csharp
int EnumFrameInfo ( 
   enum_FRAMEINFO_FLAGS     dwFieldSpec,
   uint                     nRadix,
   out IEnumDebugFrameInfo2 ppEnum
);
```

## <a name="parameters"></a>Parametreler
`dwFieldSpec`\
[in] Bayraklarının bir birleşimi [FRAMEINFO_FLAGS](../../../extensibility/debugger/reference/frameinfo-flags.md) hangi alanları belirten numaralandırma [FRAMEINFO](../../../extensibility/debugger/reference/frameinfo.md) doldurulması için yapılardır. Belirtin `FIF_FUNCNAME_FORMAT` işlev adı tek bir dize olarak biçimlendirmek için bayrak.

`nRadix`\
[in] Numaralandırıcı sayısal bilgilerinde biçimlendirmede kullanılan taban.

`ppEnum`\
[out] Döndürür bir [IEnumDebugFrameInfo2](../../../extensibility/debugger/reference/ienumdebugframeinfo2.md) listesini içeren nesne [FRAMEINFO](../../../extensibility/debugger/reference/frameinfo.md) yapıları açıklayan yığın çerçevesi.

## <a name="return-value"></a>Dönüş Değeri
 Başarılı olursa döndürür `S_OK`; Aksi takdirde bir hata kodu döndürür.

## <a name="remarks"></a>Açıklamalar
 İş parçacığının çerçeveler, ilk numaralandırılmış geçerli çerçeve ve son numaralandırılan eski çerçeve ile sırayla numaralandırılır.

## <a name="see-also"></a>Ayrıca bkz.
- [IDebugThread2](../../../extensibility/debugger/reference/idebugthread2.md)
- [FRAMEINFO_FLAGS](../../../extensibility/debugger/reference/frameinfo-flags.md)
- [IEnumDebugFrameInfo2](../../../extensibility/debugger/reference/ienumdebugframeinfo2.md)
- [FRAMEINFO](../../../extensibility/debugger/reference/frameinfo.md)
---
title: IDebugPortRequest2::GetPortName | Microsoft Docs
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- IDebugPortRequest2::GetPortName
helpviewer_keywords:
- IDebugPortRequest2::GetPortName
ms.assetid: 53e2a3a4-bb34-4a02-a983-6bd84ea70587
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
dev_langs:
- CPP
- CSharp
ms.openlocfilehash: 63cda29c6f21cda89742ba218808bc76ffae627a
ms.sourcegitcommit: 19ec963ed6d585719cb83ba677434ea6580e0d1f
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/24/2019
ms.locfileid: "66204485"
---
# <a name="idebugportrequest2getportname"></a>IDebugPortRequest2::GetPortName
Bağlantı noktası adını alır.

## <a name="syntax"></a>Sözdizimi

```cpp
HRESULT GetPortName( 
   BSTR* pbstrPortName
);
```

```csharp
int GetPortName( 
   out string pbstrPortName
);
```

## <a name="parameters"></a>Parametreler
`pbstrPortName`\
[out] Bağlantı noktası adını döndürür.

## <a name="return-value"></a>Dönüş Değeri
 Başarılı olursa döndürür `S_OK`; Aksi takdirde bir hata kodu döndürür.

## <a name="remarks"></a>Açıklamalar
 [IDebugPortRequest2](../../../extensibility/debugger/reference/idebugportrequest2.md) arabirimi genellikle geçirilen bir hata ayıklama paketi (istemci) bir bağlantı almak için bir bağlantı noktası sağlayıcısı için (sunucu) için bir bağlantı noktası. Hata ayıklama paketi hem de bağlantı noktası sağlayıcısı bağlantı noktası için olası seçeneklerin farkındayız. Bağlantı noktası, basit bir dize tanımlayabilir, ardından `IDebugPortRequest2::GetPortName` yöntemi bağlantı kurmak için yeterli bilgi vardır. Aksi takdirde, ek arabirimleri sunucusu kullanılarak elde edilebilir istemci tarafından sağlanabilir `IDebugPortRequest2::QueryInterface`.

## <a name="see-also"></a>Ayrıca bkz.
- [IDebugPortRequest2](../../../extensibility/debugger/reference/idebugportrequest2.md)
---
title: IDebugPortSupplier3::EnumPersistedPorts | Microsoft Docs
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- IDebugPortSupplier3::EnumPersistedPorts
helpviewer_keywords:
- IDebugPortSupplier3::EnumPersistedPorts
ms.assetid: 1c3dead3-5d6c-4067-8418-4015f0b0dd07
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: c646974a1d1303482785ffd0240b3374e2ed071f
ms.sourcegitcommit: b0d8e61745f67bd1f7ecf7fe080a0fe73ac6a181
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/22/2019
ms.locfileid: "56688946"
---
# <a name="idebugportsupplier3enumpersistedports"></a>IDebugPortSupplier3::EnumPersistedPorts
Bu yöntem, kalıcı bağlantı noktalarının listesi numaralandırmasına izin veren bir nesneyi alır.

## <a name="syntax"></a>Sözdizimi

```cpp
HRESULT EnumPersistedPorts(
   BSTR_ARRAY         PortNames,
   IEnumDebugPorts2** ppEnum
);
```

```csharp
int EnumPersistedPorts(
   BSTR_ARRAY           PortNames,
   out IEnumDebugPorts2 ppEnum
);
```

#### <a name="parameters"></a>Parametreler
 `PortNames`

 [in] A [BSTR_ARRAY](../../../extensibility/debugger/reference/bstr-array.md) bulun ve kalıcı bağlantı noktaları arasında döndürmek için bağlantı noktası adları listesini içeren yapısı. Yalnızca kalıcı bağlantı noktalarından şu adlara sahip döndürülür.

 `ppEnum`

 [out] Uygulayan bir nesne [IEnumDebugPorts2](../../../extensibility/debugger/reference/ienumdebugports2.md) arabirimi.

## <a name="return-value"></a>Dönüş Değeri
 Başarılı olursa döndürür `S_OK`; Aksi takdirde bir hata kodu döndürür.

## <a name="remarks"></a>Açıklamalar
 Bağlantı noktası sağlayıcısı örneği ve bağlantı noktası sağlayıcısı kaldırıldığında kaydedilen kalıcı bağlantı noktaları yüklenir.

## <a name="see-also"></a>Ayrıca Bkz.
- [IDebugPortSupplier3](../../../extensibility/debugger/reference/idebugportsupplier3.md)
- [IEnumDebugPorts2](../../../extensibility/debugger/reference/ienumdebugports2.md)
- [BSTR_ARRAY](../../../extensibility/debugger/reference/bstr-array.md)
---
title: IDebugCoreServer3::GetServerFriendlyName | Microsoft Docs
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- IDebugCoreServer3::GetServerFriendlyName
helpviewer_keywords:
- IDebugCoreServer3::GetServerFriendlyName
ms.assetid: 7035b904-b3d7-4d9b-98d9-65714b8a8b9f
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: 0dec32c47354f43cee33077985c122c92aaebc6f
ms.sourcegitcommit: b0d8e61745f67bd1f7ecf7fe080a0fe73ac6a181
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/22/2019
ms.locfileid: "56718124"
---
# <a name="idebugcoreserver3getserverfriendlyname"></a>IDebugCoreServer3::GetServerFriendlyName
Sunucu için bir kolay ad alır.

## <a name="syntax"></a>Sözdizimi

```cpp
HRESULT GetServerFriendlyName(
   BSTR* pbstrName
);
```

```csharp
int GetServerFriendlyName(
   out string pbstrName
);
```

#### <a name="parameters"></a>Parametreler
 `pbstrName`

 [out] Sunucu için bir kolay ad döndürür.

> [!NOTE]
>  Dize boşaltma için çağıran sorumludur.

## <a name="return-value"></a>Dönüş Değeri
 Başarılı olursa döndürür `S_OK`; Aksi halde hata kodu döndürür.

## <a name="remarks"></a>Açıklamalar
 Kullanıcı tarafından başlatılan sunucular için bu yöntem tarafından döndürülen adı tam sunucu adıdır. Otomatik başlatılan sunucular için makineye sunucusunun çalıştığını adıdır.

 Makine odaklı bir adı için arama [GetServerName](../../../extensibility/debugger/reference/idebugcoreserver3-getservername.md) yöntemi.

## <a name="see-also"></a>Ayrıca Bkz.
- [IDebugCoreServer3](../../../extensibility/debugger/reference/idebugcoreserver3.md)
- [GetServerName](../../../extensibility/debugger/reference/idebugcoreserver3-getservername.md)
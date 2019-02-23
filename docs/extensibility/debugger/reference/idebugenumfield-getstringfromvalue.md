---
title: IDebugEnumField::GetStringFromValue | Microsoft Docs
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- IDebugEnumField::GetStringFromValue
helpviewer_keywords:
- IDebugEnumField::GetStringFromValue method
ms.assetid: 5f95fd0c-fdce-497f-9f54-2ad8749494e9
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: 98d7e976e0cd37ad1397666471c89da3d47d45d3
ms.sourcegitcommit: b0d8e61745f67bd1f7ecf7fe080a0fe73ac6a181
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/22/2019
ms.locfileid: "56710376"
---
# <a name="idebugenumfieldgetstringfromvalue"></a>IDebugEnumField::GetStringFromValue
Bu yöntem, değeri verilen numaralandırma sabiti adını alır.

## <a name="syntax"></a>Sözdizimi

```cpp
HRESULT GetStringFromValue(
   ULONGLONG value,
   BSTR*     pbstrValue
);
```

```csharp
int GetStringFromValue(
   ulong      value,
   out string pbstrValue
);
```

#### <a name="parameters"></a>Parametreler
 `value`

 [in] Alınacağı adı numaralandırma sabit değeri.

 `pbstrValue`

 [out] Sabit listesi sabitinin adı döndürür.

## <a name="return-value"></a>Dönüş Değeri
 Başarılı olursa döndürür `S_OK`; Aksi halde döndürür `S_FALSE` değeri ilişkili adı yok ya da bir hata kodu döndürür.

## <a name="remarks"></a>Açıklamalar
 İlk numaralandırmada tanımlanan adla aynı değeri ile ilişkili birden fazla adı varsa, döndürülür.

## <a name="see-also"></a>Ayrıca Bkz.
- [IDebugEnumField](../../../extensibility/debugger/reference/idebugenumfield.md)
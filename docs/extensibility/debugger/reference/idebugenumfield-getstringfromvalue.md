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
dev_langs:
- CPP
- CSharp
ms.openlocfilehash: 25becdae62dbdda78e04404528eeb099a4914265
ms.sourcegitcommit: 19ec963ed6d585719cb83ba677434ea6580e0d1f
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/24/2019
ms.locfileid: "66212401"
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

## <a name="parameters"></a>Parametreler
`value`\
[in] Alınacağı adı numaralandırma sabit değeri.

`pbstrValue`\
[out] Sabit listesi sabitinin adı döndürür.

## <a name="return-value"></a>Dönüş Değeri
 Başarılı olursa döndürür `S_OK`; Aksi halde döndürür `S_FALSE` değeri ilişkili adı yok ya da bir hata kodu döndürür.

## <a name="remarks"></a>Açıklamalar
 İlk numaralandırmada tanımlanan adla aynı değeri ile ilişkili birden fazla adı varsa, döndürülür.

## <a name="see-also"></a>Ayrıca bkz.
- [IDebugEnumField](../../../extensibility/debugger/reference/idebugenumfield.md)
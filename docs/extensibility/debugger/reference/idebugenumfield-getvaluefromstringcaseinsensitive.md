---
title: IDebugEnumField::GetValueFromStringCaseInsensitive | Microsoft Docs
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- IDebugEnumField::GetValueFromStringCaseInsensitive
helpviewer_keywords:
- IDebugEnumField::GetValueFromStringCaseInsensitive method
ms.assetid: ef95b38e-d9b2-4fb5-a166-7c2e14641dc7
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
dev_langs:
- CPP
- CSharp
ms.openlocfilehash: 163e675d0ef4b47e0a0bf82d730adcc081eddec3
ms.sourcegitcommit: 19ec963ed6d585719cb83ba677434ea6580e0d1f
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/24/2019
ms.locfileid: "66200101"
---
# <a name="idebugenumfieldgetvaluefromstringcaseinsensitive"></a>IDebugEnumField::GetValueFromStringCaseInsensitive
Bu yöntem, numaralandırma sabiti adla ilişkilendirilmiş değeri döndürmek için büyük küçük harf duyarsız arama kullanır.

## <a name="syntax"></a>Sözdizimi

```cpp
HRESULT GetValueFromStringCaseInsensitive(
   LPCOLESTR  pszValue,
   ULONGLONG* pvalue
);
```

```csharp
int GetValueFromStringCaseInsensitive(
   string    pszValue,
   out ulong pValue
);
```

## <a name="parameters"></a>Parametreler
`pszValue`\
[in] Değerin alınacağı adını belirten dize. C++ için geniş karakter dizesi bu olduğunu unutmayın.

`pValue`\
[out] İlişkili sayısal değeri döndürür.

## <a name="return-value"></a>Dönüş Değeri
 Başarılı olursa döndürür `S_OK`; Aksi halde döndürür `S_FALSE`, ad sabit listesi veya bir hata kodu bir parçası değil.

## <a name="remarks"></a>Açıklamalar
 Bu yöntem, büyük/küçük harf duyarlıdır. Büyük küçük harfe duyarlı bir arama (örneğin, bir dilde burada adları büyük/küçük harfe C++ gibi) gerekiyorsa kullanın [GetValueFromString](../../../extensibility/debugger/reference/idebugenumfield-getvaluefromstring.md).

## <a name="see-also"></a>Ayrıca bkz.
- [IDebugEnumField](../../../extensibility/debugger/reference/idebugenumfield.md)
- [GetValueFromString](../../../extensibility/debugger/reference/idebugenumfield-getvaluefromstring.md)
---
title: IDebugEnumField::GetValueFromString | Microsoft Docs
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- IDebugEnumField::GetValueFromString
helpviewer_keywords:
- IDebugEnumField::GetValueFromString method
ms.assetid: 1ef8ac5e-a3e0-4078-b876-7f5615aedcbb
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: e714e6b2028605eb9c820f904cedf9ed4c23eab8
ms.sourcegitcommit: b0d8e61745f67bd1f7ecf7fe080a0fe73ac6a181
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/22/2019
ms.locfileid: "56716031"
---
# <a name="idebugenumfieldgetvaluefromstring"></a>IDebugEnumField::GetValueFromString
Bu yöntem, numaralandırma sabiti adla ilişkilendirilmiş değeri döndürür.

## <a name="syntax"></a>Sözdizimi

```cpp
HRESULT GetValueFromString(
   LPCOLESTR  pszValue,
   ULONGLONG* pvalue
);
```

```csharp
int GetValueFromString(
   string    pszValue,
   out ulong pValue
);
```

#### <a name="parameters"></a>Parametreler
 `pszValue`

 [in] Değerin alınacağı adını belirten dize. C++ için geniş karakter dizesi bu olduğunu unutmayın.

 `pValue`

 [out] İlişkili sayısal değeri döndürür.

## <a name="return-value"></a>Dönüş Değeri
 Başarılı olursa döndürür `S_OK`; Aksi halde döndürür `S_FALSE`, ad sabit listesi veya bir hata kodu bir parçası değil.

## <a name="remarks"></a>Açıklamalar
 Bu yöntem, büyük/küçük harf duyarlıdır. Büyük küçük harf duyarsız arama (örneğin, bir dilde adları olmadığı büyük küçük harfe duyarlı Visual Basic gibi) gerekiyorsa kullanın [GetValueFromStringCaseInsensitive](../../../extensibility/debugger/reference/idebugenumfield-getvaluefromstringcaseinsensitive.md).

## <a name="see-also"></a>Ayrıca Bkz.
- [IDebugEnumField](../../../extensibility/debugger/reference/idebugenumfield.md)
- [GetValueFromStringCaseInsensitive](../../../extensibility/debugger/reference/idebugenumfield-getvaluefromstringcaseinsensitive.md)
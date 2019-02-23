---
title: IDebugMethodField::EnumStaticLocals | Microsoft Docs
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- IDebugMethodField::EnumStaticLocals
helpviewer_keywords:
- IDebugMethodField::EnumStaticLocals method
ms.assetid: e0c522c4-f759-4c32-ae87-7abcb573e77d
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: 4fb50271801d895ca73dbbc915ff95320183d032
ms.sourcegitcommit: b0d8e61745f67bd1f7ecf7fe080a0fe73ac6a181
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/22/2019
ms.locfileid: "56680275"
---
# <a name="idebugmethodfieldenumstaticlocals"></a>IDebugMethodField::EnumStaticLocals
Yöntem statik yerel değişkenler için bir numaralandırıcı oluşturur.

## <a name="syntax"></a>Sözdizimi

```cpp
HRESULT EnumStaticLocals( 
   IEnumDebugFields** ppLocals
);
```

```csharp
int EnumStaticLocals(
   out IEnumDebugFields ppLocals
);
```

#### <a name="parameters"></a>Parametreler
 `ppLocals`

 [out] Döndürür bir [IEnumDebugFields](../../../extensibility/debugger/reference/ienumdebugfields.md) statik yerel öğeleri listesini temsil eden nesne. Hiçbir statik yerel öğeler varsa, bir null değer döndürür.

## <a name="return-value"></a>Dönüş Değeri
 Başarılıysa S_OK döndürür veya hiçbir statik yerel öğeler varsa S_FALSE döndürür. Aksi takdirde bir hata kodu döndürür.

## <a name="remarks"></a>Açıklamalar
 Her öğe bir [IDebugField](../../../extensibility/debugger/reference/idebugfield.md) statik yerel öğeler farklı türleri temsil eden nesne. Çağrı [GetKind](../../../extensibility/debugger/reference/idebugfield-getkind.md) tam olarak hangi tür statik yerel bir nesneyi temsil belirlemek için her bir nesne üzerindeki yöntemi.

## <a name="see-also"></a>Ayrıca Bkz.
- [IDebugMethodField](../../../extensibility/debugger/reference/idebugmethodfield.md)
- [IEnumDebugFields](../../../extensibility/debugger/reference/ienumdebugfields.md)
- [IDebugField](../../../extensibility/debugger/reference/idebugfield.md)
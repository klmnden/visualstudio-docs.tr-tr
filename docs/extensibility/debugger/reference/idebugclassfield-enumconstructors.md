---
title: IDebugClassField::EnumConstructors | Microsoft Docs
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- IDebugClassField::EnumConstructors
helpviewer_keywords:
- IDebugClassField::EnumConstructors method
ms.assetid: 66a250b2-75a0-45aa-8d58-40f91cc4bf7b
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: 5ecc2e2fba9dbddc12a58866c7edcde51b148af1
ms.sourcegitcommit: b0d8e61745f67bd1f7ecf7fe080a0fe73ac6a181
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/22/2019
ms.locfileid: "56719123"
---
# <a name="idebugclassfieldenumconstructors"></a>IDebugClassField::EnumConstructors
Bu sınıf için oluşturucuları için bir numaralandırıcı oluşturur.

## <a name="syntax"></a>Sözdizimi

```cpp
HRESULT EnumConstructors( 
   CONSTRUCTOR_ENUM   cMatch,
   IEnumDebugFields** ppEnum
);
```

```csharp
int EnumConstructors(
   CONSTRUCTOR_ENUM     cMatch,
   out IEnumDebugFields ppEnum
);
```

#### <a name="parameters"></a>Parametreler
 `cMatch`

 [in] Bir değer [CONSTRUCTOR_ENUM](../../../extensibility/debugger/reference/constructor-enum.md) oluşturucular için sabit listesi türünü belirten sabit listesi.

 `ppEnum`

 [out] Döndürür bir [IEnumDebugFields](../../../extensibility/debugger/reference/ienumdebugfields.md) oluşturucular listesini temsil eden nesne. Hiç Oluşturucusu yoksa null değeri döndürür.

## <a name="return-value"></a>Dönüş Değeri
 Başarılıysa S_OK döndürür veya hiç Oluşturucusu varsa S_FALSE döndürür. Aksi takdirde bir hata kodu döndürür.

## <a name="remarks"></a>Açıklamalar
 Her öğenin sabit bir [IDebugMethodField](../../../extensibility/debugger/reference/idebugmethodfield.md) Oluşturucu yöntemi tanımlayan nesne.

 Oluşturucular listesi, genellikle derleyici tarafından sağlanan varsayılan oluşturucular içermez.

## <a name="see-also"></a>Ayrıca Bkz.
- [IDebugClassField](../../../extensibility/debugger/reference/idebugclassfield.md)
- [IEnumDebugFields](../../../extensibility/debugger/reference/ienumdebugfields.md)
- [IDebugMethodField](../../../extensibility/debugger/reference/idebugmethodfield.md)
- [CONSTRUCTOR_ENUM](../../../extensibility/debugger/reference/constructor-enum.md)
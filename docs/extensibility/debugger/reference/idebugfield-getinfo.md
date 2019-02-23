---
title: IDebugField::GetInfo | Microsoft Docs
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- IDebugField::GetInfo
helpviewer_keywords:
- IDebugField::GetInfo method
ms.assetid: 7d508200-89ce-400f-a8ea-f28e7610cb2b
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: 96ce3c428785bd6b817cb8ce0f97f14a87180d0c
ms.sourcegitcommit: b0d8e61745f67bd1f7ecf7fe080a0fe73ac6a181
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/22/2019
ms.locfileid: "56700682"
---
# <a name="idebugfieldgetinfo"></a>IDebugField::GetInfo
Bu yöntem, alanın görüntülenebilir bilgilerini alır.

## <a name="syntax"></a>Sözdizimi

```cpp
HRESULT GetInfo( 
   FIELD_INFO_FIELDS dwFields,
   FIELD_INFO* pFieldInfo
);
```

```csharp
int GetInfo(
   enum_FIELD_INFO_FIELDS dwFields,
   FIELD_INFO[] pFieldInfo
);
```

#### <a name="parameters"></a>Parametreler
 `dwFields`

 [in] Bir birleşimi [FIELD_INFO_FIELDS](../../../extensibility/debugger/reference/field-info-fields.md) görüntülenecek bilgi seçer sabitler. Alanın bir sembol temsil ediyorsa, genellikle sembol adı ve türü budur.

 `pFieldInfo`

 [out] Bilgi sağlanan içinde döndürür [FIELD_INFO](../../../extensibility/debugger/reference/field-info.md) yapısı.

## <a name="return-value"></a>Dönüş Değeri
 Başarılı olursa döndürür `S_OK`; Aksi takdirde bir hata kodu döndürür.

## <a name="see-also"></a>Ayrıca Bkz.
- [IDebugField](../../../extensibility/debugger/reference/idebugfield.md)
- [FIELD_INFO](../../../extensibility/debugger/reference/field-info.md)
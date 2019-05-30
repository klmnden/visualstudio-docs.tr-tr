---
title: IDebugField::GetInfo | Microsoft Docs
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- IDebugField::GetInfo
helpviewer_keywords:
- IDebugField::GetInfo method
ms.assetid: 7d508200-89ce-400f-a8ea-f28e7610cb2b
author: madskristensen
ms.author: madsk
manager: jillfra
ms.workload:
- vssdk
dev_langs:
- CPP
- CSharp
ms.openlocfilehash: 53c0de1b956202f95b4995855ec5bdda0ebe59d3
ms.sourcegitcommit: 40d612240dc5bea418cd27fdacdf85ea177e2df3
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/29/2019
ms.locfileid: "66352621"
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

## <a name="parameters"></a>Parametreler
`dwFields`\
[in] Bir birleşimi [FIELD_INFO_FIELDS](../../../extensibility/debugger/reference/field-info-fields.md) görüntülenecek bilgi seçer sabitler. Alanın bir sembol temsil ediyorsa, genellikle sembol adı ve türü budur.

`pFieldInfo`\
[out] Bilgi sağlanan içinde döndürür [FIELD_INFO](../../../extensibility/debugger/reference/field-info.md) yapısı.

## <a name="return-value"></a>Dönüş Değeri
 Başarılı olursa döndürür `S_OK`; Aksi takdirde bir hata kodu döndürür.

## <a name="see-also"></a>Ayrıca bkz.
- [IDebugField](../../../extensibility/debugger/reference/idebugfield.md)
- [FIELD_INFO](../../../extensibility/debugger/reference/field-info.md)
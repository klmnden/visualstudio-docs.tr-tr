---
title: IDebugField::GetTypeInfo | Microsoft Docs
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- IDebugField::GetTypeInfo
helpviewer_keywords:
- IDebugField::GetTypeInfo method
ms.assetid: bb5acfa3-04c3-4088-be84-9ff8926cd16f
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: 7b881c3b5946428bf829ca4d971bb73f814b6d45
ms.sourcegitcommit: b0d8e61745f67bd1f7ecf7fe080a0fe73ac6a181
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/22/2019
ms.locfileid: "56700997"
---
# <a name="idebugfieldgettypeinfo"></a>IDebugField::GetTypeInfo
Bu yöntem, tür bağımsız bilgilerini simge veya türü alır.

## <a name="syntax"></a>Sözdizimi

```cpp
HRESULT GetTypeInfo( 
   TYPE_INFO* pTypeInfo
);
```

```csharp
int GetTypeInfo(
   TYPE_INFO[] pTypeInfo
);
```

#### <a name="parameters"></a>Parametreler
 `pTypeInfo`

 [out] Döndürür tür bilgilerini sağlanan [TYPE_INFO](../../../extensibility/debugger/reference/type-info.md) yapısı.

## <a name="return-value"></a>Dönüş Değeri
 Başarılı olursa döndürür `S_OK`; Aksi takdirde bir hata kodu döndürür.

## <a name="remarks"></a>Açıklamalar
 Tür bağımsız bilgileri, örneğin, AppDomain, modül ve simge içeren sınıf verilebilir.

## <a name="see-also"></a>Ayrıca Bkz.
- [GetType](../../../extensibility/debugger/reference/idebugfield-gettype.md)
- [IDebugField](../../../extensibility/debugger/reference/idebugfield.md)
- [TYPE_INFO](../../../extensibility/debugger/reference/type-info.md)
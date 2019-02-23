---
title: IDebugObject2::CreateAlias | Microsoft Docs
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- IDebugObject2::CreateAlias
helpviewer_keywords:
- IDebugObject2::CreateAlias method
ms.assetid: 54a05920-5d13-4f67-962b-d1a7f013dff9
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: 226d584a2773a342b8247ff337e686be2da6bf9b
ms.sourcegitcommit: b0d8e61745f67bd1f7ecf7fe080a0fe73ac6a181
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/22/2019
ms.locfileid: "56690649"
---
# <a name="idebugobject2createalias"></a>IDebugObject2::CreateAlias
Benzersiz bir kimliği veya bu nesne için diğer ad oluşturur veya mevcut bir diğer adı döndürür.

## <a name="syntax"></a>Sözdizimi

```cpp
HRESULT CreateAlias(
   IDebugAlias** ppAlias
);
```

```csharp
int CreateAlias(
   out IDebugAlias ppAlias
);
```

#### <a name="parameters"></a>Parametreler
 `ppAlias`

 [out] Yeni (veya varolan) diğer adı.

## <a name="return-value"></a>Dönüş Değeri
 Başarılıysa S_OK döndürür; Aksi takdirde bir hata kodu döndürür.

## <a name="remarks"></a>Açıklamalar
 Bir diğer ad nesne bellekte olsa da belirli bir nesneyi temsil eden bir etikettir.

## <a name="see-also"></a>Ayrıca Bkz.
- [IDebugObject2](../../../extensibility/debugger/reference/idebugobject2.md)
- [IDebugAlias](../../../extensibility/debugger/reference/idebugalias.md)
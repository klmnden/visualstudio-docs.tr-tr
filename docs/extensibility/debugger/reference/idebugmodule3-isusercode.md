---
title: IDebugModule3::IsUserCode | Microsoft Docs
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- IDebugModule3::IsUserCode
helpviewer_keywords:
- IDebugModule3::IsUserCode
ms.assetid: 77022946-bb8b-4114-aa81-614df6e54b13
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: 39bbef1e8b831473b196d0609459b80a05e5fc2c
ms.sourcegitcommit: b0d8e61745f67bd1f7ecf7fe080a0fe73ac6a181
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/22/2019
ms.locfileid: "56718501"
---
# <a name="idebugmodule3isusercode"></a>IDebugModule3::IsUserCode
Veya modülü kullanıcı kod olup olmadığını gösteren şirket bilgilerini alır.

## <a name="syntax"></a>Sözdizimi

```cpp
HRESULT IsUserCode(
   BOOL* pfUser
);
```

```csharp
int IsUserCode(
   out int pfUser
);
```

#### <a name="parameters"></a>Parametreler
 `pfUser`

 [out] Sıfır olmayan (`TRUE`) kullanıcı kodu modülü temsil ediyorsa, sıfır (`FALSE`) kullanmıyorsa.

## <a name="return-value"></a>Dönüş Değeri
 Başarılı olursa döndürür `S_OK`; Aksi halde hata kodu döndürür.

## <a name="see-also"></a>Ayrıca Bkz.
- [IDebugModule3](../../../extensibility/debugger/reference/idebugmodule3.md)
---
title: IDebugObject2::IsUserData | Microsoft Docs
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- IDebugObject2::IsUserData
helpviewer_keywords:
- IDebugObject2::IsUserData method
ms.assetid: 6ffa0d0e-f742-496d-acc7-db74c248bc45
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: 04c47390f15ff59658ba25f5c8f93918a15f47d6
ms.sourcegitcommit: b0d8e61745f67bd1f7ecf7fe080a0fe73ac6a181
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/22/2019
ms.locfileid: "56700100"
---
# <a name="idebugobject2isuserdata"></a>IDebugObject2::IsUserData
Nesne kullanıcı verilerini temsil edip etmediğini belirler.

## <a name="syntax"></a>Sözdizimi

```cpp
HRESULT IsUserData(
   BOOL* pfUser
);
```

```csharp
int IsUserData(
   out int pfUser
);
```

#### <a name="parameters"></a>Parametreler
 `pfUser`

 [out] Sıfır olmayan döndürür (`TRUE`) kullanıcı verilerini; nesne temsil ediyorsa sıfır (`FALSE`) kullanmıyorsa.

## <a name="return-value"></a>Dönüş Değeri
 Başarılıysa S_OK döndürür; Aksi takdirde bir hata kodu döndürür.

## <a name="remarks"></a>Açıklamalar
 Kullanıcı verilerini JustMyCode (bir modül olarak kullanıcı kodu ve bu nedenle bir yığın izlemesi görünür işaretler kullanıcı tarafından yapılandırılabilen bir seçeneği) olarak belirlenmiş bir modülün parçası olan herhangi bir nesnedir.

## <a name="see-also"></a>Ayrıca Bkz.
- [IDebugObject2](../../../extensibility/debugger/reference/idebugobject2.md)
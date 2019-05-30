---
title: IDebugObject2::IsUserData | Microsoft Docs
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- IDebugObject2::IsUserData
helpviewer_keywords:
- IDebugObject2::IsUserData method
ms.assetid: 6ffa0d0e-f742-496d-acc7-db74c248bc45
author: madskristensen
ms.author: madsk
manager: jillfra
ms.workload:
- vssdk
dev_langs:
- CPP
- CSharp
ms.openlocfilehash: 94c3f6adc9dd75e1ed4ecc4c5fd7f37635099566
ms.sourcegitcommit: 40d612240dc5bea418cd27fdacdf85ea177e2df3
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/29/2019
ms.locfileid: "66317249"
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

## <a name="parameters"></a>Parametreler
`pfUser`\
[out] Sıfır olmayan döndürür (`TRUE`) kullanıcı verilerini; nesne temsil ediyorsa sıfır (`FALSE`) kullanmıyorsa.

## <a name="return-value"></a>Dönüş Değeri
 Başarılıysa S_OK döndürür; Aksi takdirde bir hata kodu döndürür.

## <a name="remarks"></a>Açıklamalar
 Kullanıcı verilerini JustMyCode (bir modül olarak kullanıcı kodu ve bu nedenle bir yığın izlemesi görünür işaretler kullanıcı tarafından yapılandırılabilen bir seçeneği) olarak belirlenmiş bir modülün parçası olan herhangi bir nesnedir.

## <a name="see-also"></a>Ayrıca bkz.
- [IDebugObject2](../../../extensibility/debugger/reference/idebugobject2.md)
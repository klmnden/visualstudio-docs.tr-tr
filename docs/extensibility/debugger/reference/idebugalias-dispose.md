---
title: IDebugAlias::Dispose | Microsoft Docs
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- IDebugAlias::Dispose
helpviewer_keywords:
- IDebugAlias::Dispose method
ms.assetid: e84909a4-d378-4f48-bf25-2c014c77c8e3
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: d35b5819aa0354581721f02a931aa7bdf679b70d
ms.sourcegitcommit: b0d8e61745f67bd1f7ecf7fe080a0fe73ac6a181
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/22/2019
ms.locfileid: "56714965"
---
# <a name="idebugaliasdispose"></a>IDebugAlias::Dispose
Bu diğer adı kaldırılmak üzere işaretler.

## <a name="syntax"></a>Sözdizimi

```cpp
HRESULT Dispose();
```

```csharp
int Dispose();
```

#### <a name="parameters"></a>Parametreler
 Yok.

## <a name="return-value"></a>Dönüş Değeri
 Başarılıysa S_OK döndürür; Aksi takdirde bir hata kodu döndürür.

## <a name="remarks"></a>Açıklamalar
 Bu yöntem çağrıldığında, diğer ad artık kullanılamıyor.

## <a name="see-also"></a>Ayrıca Bkz.
- [IDebugAlias](../../../extensibility/debugger/reference/idebugalias.md)
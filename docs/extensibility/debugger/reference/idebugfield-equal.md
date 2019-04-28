---
title: IDebugField::Equal | Microsoft Docs
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- IDebugField::Equal
helpviewer_keywords:
- IDebugField::Equal method
ms.assetid: 75369fe6-ddd3-497d-80d1-2488e6100e9f
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: ed978355aa752730cfb43390b3e4b6f80d327f83
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62919464"
---
# <a name="idebugfieldequal"></a>IDebugField::Equal
Bu yöntem, bu alan için eşitlik belirtilen alan ile karşılaştırır.

## <a name="syntax"></a>Sözdizimi

```cpp
HRESULT Equal( 
   IDebugField* pField
);
```

```csharp
int Equal(
   IDebugField pField
);
```

#### <a name="parameters"></a>Parametreler
 `pField`

 [in] Buna karşılaştırmak için alan.

## <a name="return-value"></a>Dönüş Değeri
 Alanları aynıysa döndürür `S_OK`. Alanları farklı ise döndürür `S_FALSE.` Aksi takdirde bir hata kodu döndürür.

## <a name="see-also"></a>Ayrıca Bkz.
- [IDebugField](../../../extensibility/debugger/reference/idebugfield.md)
---
title: SccGetVersion işlevi | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
f1_keywords:
- SccGetVersion
helpviewer_keywords:
- SccGetVersion function
ms.assetid: a6e786bf-744e-4272-9e21-0be44d23b1a1
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: 7e2b3818aaa5097313d9150b365544267768507f
ms.sourcegitcommit: b0d8e61745f67bd1f7ecf7fe080a0fe73ac6a181
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/22/2019
ms.locfileid: "56708946"
---
# <a name="sccgetversion-function"></a>SccGetVersion İşlevi
Bu işlev, kaynak denetimi eklentisi tarafından desteklenen kaynak denetimi eklentisi API sürüm numarasını alır.

## <a name="syntax"></a>Sözdizimi

```cpp
LONG SccGetVersion(void);
```

#### <a name="parameters"></a>Parametreler
 Yok.

## <a name="return-value"></a>Dönüş Değeri
 A `LONG` desteklenen kaynak denetimi eklentisi API sürüm numarasını içeren veri türü:

|WORD|Açıklama|
|----------|-----------------|
|GET_Y_LPARAM KULLANIN|Ana sürüm|
|GET_X_LPARAM|Alt sürüm|

## <a name="remarks"></a>Açıklamalar
 Örneğin, bir kaynak denetimi Eklentisi Kaynak Denetimi Eklentisi API sürümü 1.3 destekliyorsa, bu işlev 0x0103 döndürür.

## <a name="see-also"></a>Ayrıca Bkz.
- [Kaynak Denetimi Eklentisi API İşlevleri](../extensibility/source-control-plug-in-api-functions.md)
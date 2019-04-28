---
title: IDiaPropertyStorage::Enum | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
dev_langs:
- C++
helpviewer_keywords:
- IDiaPropertyStorage::Enum
ms.assetid: 00e462da-980a-40b3-a2d6-75a25ee809e5
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: e39693f63ea706ecdfa30a9ce0202444f51d4f57
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62839686"
---
# <a name="idiapropertystorageenum"></a>IDiaPropertyStorage::Enum
İçinde bu özellikleri için bir numaralandırıcı alır.

## <a name="syntax"></a>Sözdizimi

```C++
HRESULT Enum ( 
   IEnumSTATPROPSTG** ppenum
);
```

#### <a name="parameters"></a>Parametreler
 `ppenum`

[out] Döndürür bir `IEnumSTATPROPSTG` (Microsoft.VisualStudio.OLE.Interop uzayında) özelliklerini numaralandırması temsil eden nesne.

## <a name="return-value"></a>Dönüş Değeri
 Başarılı olursa döndürür `S_OK`; Aksi takdirde bir hata kodu döndürür.

## <a name="see-also"></a>Ayrıca Bkz.
- [IDiaPropertyStorage](../../debugger/debug-interface-access/idiapropertystorage.md)
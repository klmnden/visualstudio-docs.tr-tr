---
title: Idiaaddressmap::get_relativevirtualaddressenabled | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
dev_langs:
- C++
helpviewer_keywords:
- IDiaAddressMap::get_relativeVirtualAddressEnabled method
ms.assetid: 4c48af81-7148-4d9a-818e-dbe62cbfc638
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 18a242a47978fbd6acb2b6161ada2199ced8c434
ms.sourcegitcommit: d0425b6b7d4b99e17ca6ac0671282bc718f80910
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/21/2019
ms.locfileid: "56604424"
---
# <a name="idiaaddressmapgetrelativevirtualaddressenabled"></a>IDiaAddressMap::get_relativeVirtualAddressEnabled
Göreli sanal adreslerine (RVA) kullanılması ve hesaplama etkin olup olmadığını gösterir.

## <a name="syntax"></a>Sözdizimi

```C++
HRESULT get_relativeVirtualAddressEnabled ( 
   BOOL* pRetVal
);
```

#### <a name="parameters"></a>Parametreler
 pRetVal

[out] Döndürür `TRUE` RVA hesaplanması etkinse.

## <a name="return-value"></a>Dönüş Değeri
 Başarılı olursa döndürür `S_OK`; Aksi takdirde bir hata kodu döndürür.

## <a name="remarks"></a>Açıklamalar
 Parçaları bir PDB dosyasındaki ilk yüklenmiş olan, RVA etkinleştirilir. RVA kullanımını geçici olarak çağırarak devre dışı bırakılabilir [Idiaaddressmap::put_relativevirtualaddressenabled](../../debugger/debug-interface-access/idiaaddressmap-put-relativevirtualaddressenabled.md) yöntemi.

 Ayrıca, yeni görüntüyü üstbilgileri çağırarak kurulabilir [Idiaaddressmap::set_imageheaders](../../debugger/debug-interface-access/idiaaddressmap-set-imageheaders.md) yöntemine bir çağrı tarafından izlenen `put_relativeVirtualAddressEnabled` kullanarak yeni görüntüyü üstbilgileri RVA kullanımını etkinleştirmek için yöntemi.

## <a name="see-also"></a>Ayrıca Bkz.
- [IDiaAddressMap](../../debugger/debug-interface-access/idiaaddressmap.md)
- [IDiaAddressMap::set_imageHeaders](../../debugger/debug-interface-access/idiaaddressmap-set-imageheaders.md)
- [IDiaAddressMap::put_relativeVirtualAddressEnabled](../../debugger/debug-interface-access/idiaaddressmap-put-relativevirtualaddressenabled.md)
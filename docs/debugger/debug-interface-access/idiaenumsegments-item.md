---
title: Idiaenumsegments::Item | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
dev_langs:
- C++
helpviewer_keywords:
- IDiaEnumSegments::Item method
ms.assetid: ee44dd55-39a0-4b7b-97ff-2e1226eeb2bd
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 87751dcca1e2109db53c9d6dd4594bc969ffc684
ms.sourcegitcommit: d0425b6b7d4b99e17ca6ac0671282bc718f80910
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/21/2019
ms.locfileid: "56616511"
---
# <a name="idiaenumsegmentsitem"></a>IDiaEnumSegments::Item
Bir segmenti yoluyla dizin alır.

## <a name="syntax"></a>Sözdizimi

```C++
HRESULT Item ( 
   DWORD         index,
   IDiaSegment** segment
);
```

#### <a name="parameters"></a>Parametreler
 dizin

[in] Dizin [Idiasegment](../../debugger/debug-interface-access/idiasegment.md) alınacak nesne. İçin 0 aralığındaki dizinidir `count`-1, burada `count` tarafından döndürülen [Idiaenumsegments::get_Count](../../debugger/debug-interface-access/idiaenumsegments-get-count.md) yöntemi.

 Segment

[out] Döndürür bir [Idiasegment](../../debugger/debug-interface-access/idiasegment.md) istenen kesimini temsil eden nesne.

## <a name="return-value"></a>Dönüş Değeri
 Başarılı olursa döndürür `S_OK`; Aksi takdirde bir hata kodu döndürür.

## <a name="see-also"></a>Ayrıca Bkz.
- [IDiaEnumSegments](../../debugger/debug-interface-access/idiaenumsegments.md)
- [IDiaSegment](../../debugger/debug-interface-access/idiasegment.md)
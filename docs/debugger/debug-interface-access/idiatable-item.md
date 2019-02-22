---
title: Idiatable::Item | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
dev_langs:
- C++
helpviewer_keywords:
- IDiaTable::Item method
ms.assetid: eae11b26-4807-400c-be25-e85bbc0c6b20
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 1d8070acfa254ae26e017a0070a21884309bc4d7
ms.sourcegitcommit: d0425b6b7d4b99e17ca6ac0671282bc718f80910
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/21/2019
ms.locfileid: "56616345"
---
# <a name="idiatableitem"></a>IDiaTable::Item
Belirtilen giriş tablosundaki bir başvuru alır.

## <a name="syntax"></a>Sözdizimi

```C++
HRESULT Item ( 
   DWORD      index,
   IUnknown** element
);
```

#### <a name="parameters"></a>Parametreler
 `index`

[in] Tablo girişi için 0 aralığındaki dizinini `count`-1, burada `count` tarafından döndürülen [Idiatable::get_Count](../../debugger/debug-interface-access/idiatable-get-count.md)yöntemi.

 `element`

[out] Döndürür bir `IUnknown` belirtilen tablo girişi temsil eden nesne.

## <a name="return-value"></a>Dönüş Değeri
 Başarılı olursa döndürür `S_OK`; Aksi takdirde bir hata kodu döndürür.

## <a name="remarks"></a>Açıklamalar
 Bir tablo nesnelerinin bir koleksiyonunu temsil eder. Nesnelere bağlı olarak, öğenin parametresi uygun arabirimine çevirebilirsiniz. Örneğin, bir tablo içeriyorsa [Idiasegment](../../debugger/debug-interface-access/idiasegment.md) öğesi parametresi atanabilecek sonra nesneleri `IDiaSegment` arabirimi.

 Çağırmak için daha yaygın bir yaklaşımdır `QueryInterface` yönteminde [Idiatable](../../debugger/debug-interface-access/idiatable.md) uygun Numaralandırıcı arabirimi arabirim ve içindekiler erişmek için Numaralandırıcı belirli yöntemlerini kullanın. Bkz: [Idiaenumınjectedsources](../../debugger/debug-interface-access/idiaenuminjectedsources.md) örneği için arabirim.

## <a name="see-also"></a>Ayrıca Bkz.
- [IDiaTable](../../debugger/debug-interface-access/idiatable.md)
- [IDiaTable::get_Count](../../debugger/debug-interface-access/idiatable-get-count.md)
- [IDiaSegment](../../debugger/debug-interface-access/idiasegment.md)
- [IDiaEnumInjectedSources](../../debugger/debug-interface-access/idiaenuminjectedsources.md)
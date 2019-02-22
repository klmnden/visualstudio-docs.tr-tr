---
title: CvReleaseMarkerSeries işlevi | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
f1_keywords:
- cvmarkers/CvReleaseMarkerSeries
helpviewer_keywords:
- CvReleaseMarkerSeries method
ms.assetid: 3b4711ee-e534-411d-9128-f69cd7932a48
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: d100b7ff37ea5a3cd224fd420f14e4cb23061903
ms.sourcegitcommit: d0425b6b7d4b99e17ca6ac0671282bc718f80910
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/21/2019
ms.locfileid: "56630203"
---
# <a name="cvreleasemarkerseries-function"></a>CvReleaseMarkerSeries işlevi
İşaret serisi serbest bırakır. Aksi takdirde uygulama serbest çökebilir sonra işaret serisi nesnesi kullanmayın. İşaret serisi yayımlamayı hatası bellek sızıntısına neden olur.

## <a name="syntax"></a>Sözdizimi

```C
HRESULT CvReleaseMarkerSeries(
   _In_reads_bytes_(16) PCV_MARKERSERIES pMarkerSeries
);
```

#### <a name="parameters"></a>Parametreler
 `pMarkerSeries` Nesne değişkeni sağlayıcı adresi. Adresi boş olamaz, değişken herhangi bir değere sahip olabilir.

## <a name="return-value"></a>Dönüş Değeri
 S_OK işaret serisi başarıyla serbest bırakıldı veya hata kodu var. durumda tüm hatalar. Hata koşulu denetleyen için başarılı/başarısız makroları kullanın.

## <a name="requirements"></a>Gereksinimler
 **Başlık:** *cvmarkers.h*

## <a name="see-also"></a>Ayrıca bkz.
- [C++ Kitaplık Başvurusu](../profiling/cpp-library-reference.md)
---
title: CvCreateMarkerSeries işlevi | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
f1_keywords:
- cvmarkers/CvCreateMarkerSeriesA
- cvmarkers/CvCreateMarkerSeriesW
helpviewer_keywords:
- CvCreateMarkerSeriesA method
- CvCreateMarkerSeriesW method
ms.assetid: e280530b-137a-43a7-8643-aa514ab86ed7
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: eb3ef4d928aaac57f39a48e5be212c1148ef58eb
ms.sourcegitcommit: d0425b6b7d4b99e17ca6ac0671282bc718f80910
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/21/2019
ms.locfileid: "56630307"
---
# <a name="cvcreatemarkerseries-function"></a>CvCreateMarkerSeries işlevi
İşaret için belirli bir sağlayıcı oluşturur.

## <a name="syntax"></a>Sözdizimi

```C
_Check_return_ HRESULT CvCreateMarkerSeriesW(
    _In_ PCV_PROVIDER  pProvider,
    _In_ LPCWSTR pSeriesName,
    _Out_ PCV_MARKERSERIES* ppMarkerSeries);

_Check_return_ HRESULT CvCreateMarkerSeriesA(
    _In_ PCV_PROVIDER  pProvider,
    _In_ LPCSTR pSeriesName,
    _Out_ PCV_MARKERSERIES* ppMarkerSeries);
```

#### <a name="parameters"></a>Parametreler
 `pProvider` Cvınitprovider tarafından önceden başlatılan sağlayıcı nesnesi. NULL olamaz.

 `pSeriesName` İşaret seri adı. NULL olamaz, ancak boş dizeye izin verilir.

 `ppMarkerSeries` İşaret serisi bağlam depolayacak bir çıkış değişkeni adresi. NULL olamaz.

## <a name="return-value"></a>Dönüş değeri
 S_OK işaret serisi başarıyla oluşturulduğunda veya hata kodu var. durumda tüm hatalar. Hata koşulu denetleyen için başarılı/başarısız makroları kullanın.

## <a name="requirements"></a>Gereksinimler
 **Başlık:** *cvmarkers.h*

 **Unicode:** CvCreateMarkerSeriesW

 **ANSI:** CvCreateMarkerSeriesA

## <a name="see-also"></a>Ayrıca bkz.
- [C++ Kitaplık Başvurusu](../profiling/cpp-library-reference.md)
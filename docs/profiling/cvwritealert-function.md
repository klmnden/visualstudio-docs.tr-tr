---
title: CvWriteAlert işlevi | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
f1_keywords:
- cvmarkers/CvWriteAlertVA
- cvmarkers/CvWriteAlertVW
- cvmarkers/CvWriteAlertA
- cvmarkers/CvWriteAlertW
helpviewer_keywords:
- CvWriteAlertVW method
- CvWriteAlertA method
- CvWriteAlertVA method
- CvWriteAlertW method
ms.assetid: 937aa9d6-278a-4df3-bef7-151441df16d5
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 4b7cc2316168d14c6c996c4d55065771c85ffdfc
ms.sourcegitcommit: d0425b6b7d4b99e17ca6ac0671282bc718f80910
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/21/2019
ms.locfileid: "56596819"
---
# <a name="cvwritealert-function"></a>CvWriteAlert işlevi
Bir uyarı eşzamanlılık görselleştiricisi izleme dosyasına yazar.

## <a name="syntax"></a>Sözdizimi

```C
HRESULT CvWriteAlertW(
    _In_reads_bytes_(16) PCV_MARKERSERIES pMarkerSeries,
    _In_ PCWSTR pMessage,
    ...
    );

HRESULT CvWriteAlertA(
    _In_reads_bytes_(16) PCV_MARKERSERIES pMarkerSeries,
    _In_ PCSTR pMessage,
    ...
    );

HRESULT CvWriteAlertVW(
    _In_reads_bytes_(16) PCV_MARKERSERIES pMarkerSeries,
    _In_ PCWSTR pMessage,
    _In_ va_list argList);

HRESULT CvWriteAlertVA(
    _In_reads_bytes_(16) PCV_MARKERSERIES pMarkerSeries,
    _In_ PCSTR pMessage,
    _In_ va_list argList);
```

#### <a name="parameters"></a>Parametreler
 `argList` Bağımsız değişken listesi.

 `pMarkerSeries` Geçerli işaret serisi bağlamı. NULL olamaz.

 `pMessage` İleti biçimi dizesi. NULL olamaz.

## <a name="return-value"></a>Dönüş değeri
 İletinin başarılı bir şekilde yazıldığında S_OK. Hata kodu: var olan herhangi bir hata durumunda. Hata koşulu denetleyen için başarılı/başarısız makroları kullanın.

## <a name="requirements"></a>Gereksinimler
 **Başlık:** *cvmarkers.h*

 **Unicode:** CvWriteAlertW, CvWriteAlertVW

 **ANSI:** CvWriteAlertA, CvWriteAlertVA

## <a name="see-also"></a>Ayrıca bkz.
- [C++ Kitaplık Başvurusu](../profiling/cpp-library-reference.md)
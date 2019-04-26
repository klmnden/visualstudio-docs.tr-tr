---
title: Cvınitprovider işlevi | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
f1_keywords:
- cvmarkers/CvInitProvider
helpviewer_keywords:
- CvInitProvider method
ms.assetid: ba1863ad-e35f-4d34-a2f2-5e68957d1915
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: a97be63cd782397e984fd8dbce7da844efa07540
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62552673"
---
# <a name="cvinitprovider-function"></a>Cvınitprovider işlevi
İşaretleyici sağlayıcısını başlatır. Diğer eşzamanlılık görselleştiricisi SDK'si işlevinden önce çağrılmalıdır.

## <a name="syntax"></a>Sözdizimi

```C
HRESULT CvInitProvider(
   _In_ const GUID* pGuid,
   _Out_ PCV_PROVIDER* ppProvider
);
```

#### <a name="parameters"></a>Parametreler
 `pGuid` Sağlayıcı GUID'si. NULL olamaz.

 `ppProvider` Sağlayıcı içeriği depolayacak bir çıkış değişkeni adresi. NULL olamaz.

## <a name="return-value"></a>Dönüş değeri
 S_OK sağlayıcısı başarıyla başlatıldı veya hata kodu var. durumda tüm hatalar. Hata koşulu denetleyen için başarılı/başarısız makroları kullanın.

## <a name="requirements"></a>Gereksinimler
 **Başlık:** *cvmarkers.h*

## <a name="see-also"></a>Ayrıca bkz.
- [C++ Kitaplık Başvurusu](../profiling/cpp-library-reference.md)
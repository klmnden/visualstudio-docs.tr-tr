---
title: CvCreateDefaultMarkerSeriesOfDefaultProvider işlevi | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
f1_keywords:
- cvmarkers/CvCreateDefaultMarkerSeriesOfDefaultProvider
helpviewer_keywords:
- CvCreateDefaultMarkerSeriesOfDefaultProvider method
ms.assetid: 24eb80f8-8fca-4c47-93b5-bb1eb8ffdffd
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 036eba6fd1c25b475b703f49e1841c647d5fbd9a
ms.sourcegitcommit: 2193323efc608118e0ce6f6b2ff532f158245d56
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/25/2019
ms.locfileid: "54962176"
---
# <a name="cvcreatedefaultmarkerseriesofdefaultprovider-function"></a>CvCreateDefaultMarkerSeriesOfDefaultProvider işlevi
Varsayılan işaret varsayılan sağlayıcı dizi oluşturur.  
  
## <a name="syntax"></a>Sözdizimi  
  
```C  
HRESULT CvCreateDefaultMarkerSeriesOfDefaultProvider(  
   _Out_ PCV_PROVIDER* ppProvider,  
   _Out_ PCV_MARKERSERIES* ppMarkerSeries  
);  
```  
  
#### <a name="parameters"></a>Parametreler  
 `ppProvider`  
 Nesne değişkeni sağlayıcı adresi. Adresi boş olamaz, değişken herhangi bir değere sahip olabilir.  
  
 `ppMarkerSeries`  
 İşaret serisi nesne değişkeni adresi. Adresi boş olamaz, değişken herhangi bir değere sahip olabilir.  
  
## <a name="return-value"></a>Dönüş değeri  
 Hem sağlayıcı hem de işaret serisi başarıyla oluşturulmuş veya hata kodu var. durumda herhangi bir hata olduğunda S_OK. Hata koşulu denetleyen için başarılı/başarısız makroları kullanın.  
  
## <a name="requirements"></a>Gereksinimler  
 **Başlık:** *cvmarkers.h*  
  
## <a name="see-also"></a>Ayrıca bkz.  
 [C++ Kitaplık Başvurusu](../profiling/cpp-library-reference.md)
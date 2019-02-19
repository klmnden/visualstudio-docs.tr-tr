---
title: CvCreateDefaultMarkerSeriesOfDefaultProvider işlevi | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-debug
ms.topic: reference
f1_keywords:
- cvmarkers/CvCreateDefaultMarkerSeriesOfDefaultProvider
helpviewer_keywords:
- CvCreateDefaultMarkerSeriesOfDefaultProvider method
ms.assetid: 24eb80f8-8fca-4c47-93b5-bb1eb8ffdffd
caps.latest.revision: 7
author: MikeJo5000
ms.author: mikejo
manager: jillfra
ms.openlocfilehash: fb0ab16dcd7e42a496317f4e7589bafdbdaf83dc
ms.sourcegitcommit: a83c60bb00bf95e6bea037f0e1b9696c64deda3c
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/19/2019
ms.locfileid: "54770901"
---
# <a name="cvcreatedefaultmarkerseriesofdefaultprovider-function"></a>CvCreateDefaultMarkerSeriesOfDefaultProvider İşlevi
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Varsayılan işaret varsayılan sağlayıcı dizi oluşturur.  
  
## <a name="syntax"></a>Sözdizimi  
  
```  
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
  
## <a name="return-value"></a>Dönüş Değeri  
 Hem sağlayıcı hem de işaret serisi başarıyla oluşturulmuş veya hata kodu var. durumda herhangi bir hata olduğunda S_OK. Hata koşulu denetleyen için başarılı/başarısız makroları kullanın.  
  
## <a name="requirements"></a>Gereksinimler  
 **Başlık:** cvmarkers.h  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [C++ Kitaplık Başvurusu](../profiling/cpp-library-reference.md)

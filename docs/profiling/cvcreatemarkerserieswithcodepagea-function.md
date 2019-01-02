---
title: CvCreateMarkerSeriesWithCodePageA işlevi | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
f1_keywords:
- cvmakers/CvCreateMarkerSeriesWithCodePageA
helpviewer_keywords:
- CvCreateMarkerSeriesWithCodePageA method
ms.assetid: 3d7ed601-2222-4be9-a557-f217db008753
author: mikejo5000
ms.author: mikejo
manager: douge
ms.workload:
- multiple
ms.openlocfilehash: 55466cc96e4969f05bc34edfaf4a28564dba17ea
ms.sourcegitcommit: 37fb7075b0a65d2add3b137a5230767aa3266c74
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/02/2019
ms.locfileid: "53822495"
---
# <a name="cvcreatemarkerserieswithcodepagea-function"></a>CvCreateMarkerSeriesWithCodePageA işlevi
Belirtilen sağlayıcı ve belirtilen kod sayfası için işaretçisi oluşturur. Bu işlev, açıkça işaret API ANSI işlevleri tarafından yazılan metin için kod sayfası belirtmek için kullanılabilir. İzleme yakalanan ve daha sonra farklı yerel ayarlar/dilleri ile farklı makinelerde analiz durumda kod sayfası ayarlanması yararlı olabilir. Varsayılan olarak, kod sayfası GetACP() işlevi tarafından döndürülen kullanılır.  
  
## <a name="syntax"></a>Sözdizimi  
  
```C  
HRESULT CvCreateMarkerSeriesWithCodePageA(  
   _In_ PCV_PROVIDER pProvider,  
   _In_ LPCSTR pSeriesName,  
   _In_ UINT nTextCodePage,  
   _Out_ PCV_MARKERSERIES* ppMarkerSeries  
);  
```  
  
#### <a name="parameters"></a>Parametreler  
 `pProvider`  
 Cvınitprovider tarafından önceden başlatılan sağlayıcı nesnesi. NULL olamaz.  
  
 `pSeriesName`  
 İşaret seri adı. NULL olamaz, ancak boş dizeye izin verilir.  
  
 `nTextCodePage`  
 Geçerli kod sayfası.  
  
 `ppMarkerSeries`  
 İşaret serisi bağlam depolayacak bir çıkış değişkeni adresi. NULL olamaz.  
  
## <a name="return-value"></a>Dönüş değeri  
 S_OK işaret serisi başarıyla oluşturulduğunda veya hata kodu var. durumda tüm hatalar. Hata koşulu denetleyen için başarılı/başarısız makroları kullanın.  
  
## <a name="requirements"></a>Gereksinimler  
 **Başlık:** *cvmarkers.h*  
  
## <a name="see-also"></a>Ayrıca bkz.  
 [C++ Kitaplık Başvurusu](../profiling/cpp-library-reference.md)
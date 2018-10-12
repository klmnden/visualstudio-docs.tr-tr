---
title: CvCreateMarkerSeriesWithCodePageA işlevi | Microsoft Docs
ms.custom: ''
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.reviewer: ''
ms.suite: ''
ms.technology:
- vs-ide-debug
ms.tgt_pltfrm: ''
ms.topic: article
f1_keywords:
- cvmakers/CvCreateMarkerSeriesWithCodePageA
helpviewer_keywords:
- CvCreateMarkerSeriesWithCodePageA method
ms.assetid: 3d7ed601-2222-4be9-a557-f217db008753
caps.latest.revision: 8
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: fda15e064c4a8d14ebb2d145ba9f2fa5c050ce2e
ms.sourcegitcommit: 9ceaf69568d61023868ced59108ae4dd46f720ab
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/12/2018
ms.locfileid: "49239050"
---
# <a name="cvcreatemarkerserieswithcodepagea-function"></a>CvCreateMarkerSeriesWithCodePageA İşlevi
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Belirtilen sağlayıcı ve belirtilen kod sayfası için işaretçisi oluşturur. Bu işlev, açıkça işaret API ANSI işlevleri tarafından yazılan metin için kod sayfası belirtmek için kullanılabilir. İzleme yakalanan ve daha sonra farklı yerel ayarlar/dilleri ile farklı makinelerde analiz durumda kod sayfası ayarlanması yararlı olabilir. Varsayılan olarak, kod sayfası GetACP() işlevi tarafından döndürülen kullanılır.  
  
## <a name="syntax"></a>Sözdizimi  
  
```  
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
  
## <a name="return-value"></a>Dönüş Değeri  
 S_OK işaret serisi başarıyla oluşturulduğunda veya hata kodu var. durumda tüm hatalar. Hata koşulu denetleyen için başarılı/başarısız makroları kullanın.  
  
## <a name="requirements"></a>Gereksinimler  
 **Başlık:** cvmarkers.h  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [C++ Kitaplık Başvurusu](../profiling/cpp-library-reference.md)




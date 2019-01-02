---
title: CvLeaveSpan işlevi | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
f1_keywords:
- cvmarkers/CvLeaveSpan
helpviewer_keywords:
- CvLeaveSpan method
ms.assetid: 3bf65fdf-a471-4efd-ac7a-03e701bbae5d
author: mikejo5000
ms.author: mikejo
manager: douge
ms.workload:
- multiple
ms.openlocfilehash: 4de86d390b03eb38a449ada23f4189b9baca6152
ms.sourcegitcommit: 37fb7075b0a65d2add3b137a5230767aa3266c74
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/02/2019
ms.locfileid: "53967728"
---
# <a name="cvleavespan-function"></a>CvLeaveSpan işlevi
Aralığın sonunu işaretler.  
  
## <a name="syntax"></a>Sözdizimi  
  
```C  
HRESULT CvLeaveSpan(  
   _In_ PCV_SPAN pSpan  
);  
```  
  
#### <a name="parameters"></a>Parametreler  
 `pSpan`  
 CvEnterSpan * önceki çağrı tarafından döndürülen nesne yayılır. NULL olamaz.  
  
## <a name="return-value"></a>Dönüş Değeri  
 İletinin başarılı bir şekilde yazıldığında S_OK. Hata kodu: var olan herhangi bir hata durumunda. Hata koşulu denetleyen için başarılı/başarısız makroları kullanın.  
  
## <a name="requirements"></a>Gereksinimler  
 **Başlık:** *cvmarkers.h*  
  
## <a name="see-also"></a>Ayrıca bkz.  
 [C++ Kitaplık Başvurusu](../profiling/cpp-library-reference.md)
---
title: CvLeaveSpan işlevi | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-debug
ms.topic: reference
f1_keywords:
- cvmarkers/CvLeaveSpan
helpviewer_keywords:
- CvLeaveSpan method
ms.assetid: 3bf65fdf-a471-4efd-ac7a-03e701bbae5d
caps.latest.revision: 8
author: MikeJo5000
ms.author: mikejo
manager: jillfra
ms.openlocfilehash: d1f17de6df465408e9bec3b6db4e1620f0181fd9
ms.sourcegitcommit: 8b538eea125241e9d6d8b7297b72a66faa9a4a47
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54772371"
---
# <a name="cvleavespan-function"></a>CvLeaveSpan İşlevi
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Aralığın sonunu işaretler.  
  
## <a name="syntax"></a>Sözdizimi  
  
```  
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
 **Başlık:** cvmarkers.h  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [C++ Kitaplık Başvurusu](../profiling/cpp-library-reference.md)

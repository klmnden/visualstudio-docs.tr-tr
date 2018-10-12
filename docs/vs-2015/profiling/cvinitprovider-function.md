---
title: Cvınitprovider işlevi | Microsoft Docs
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
- cvmarkers/CvInitProvider
helpviewer_keywords:
- CvInitProvider method
ms.assetid: ba1863ad-e35f-4d34-a2f2-5e68957d1915
caps.latest.revision: 8
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: aa41b1cbbba6e88a86ae5af0c471d5f6627dcca2
ms.sourcegitcommit: 9ceaf69568d61023868ced59108ae4dd46f720ab
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/12/2018
ms.locfileid: "49276221"
---
# <a name="cvinitprovider-function"></a>CvInitProvider İşlevi
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

İşaretleyici sağlayıcısını başlatır. Önce başka bir eşzamanlılık görselleştiricisi SDK işlevlerinin çağrılması gerekir.  
  
## <a name="syntax"></a>Sözdizimi  
  
```  
HRESULT CvInitProvider(  
   _In_ const GUID* pGuid,  
   _Out_ PCV_PROVIDER* ppProvider  
);  
```  
  
#### <a name="parameters"></a>Parametreler  
 `pGuid`  
 Sağlayıcı GUID'si. NULL olamaz.  
  
 `ppProvider`  
 Sağlayıcı içeriği depolayacak bir çıkış değişkeni adresi. NULL olamaz.  
  
## <a name="return-value"></a>Dönüş Değeri  
 S_OK sağlayıcısı başarıyla başlatıldı veya hata kodu var. durumda tüm hatalar. Hata koşulu denetleyen için başarılı/başarısız makroları kullanın.  
  
## <a name="requirements"></a>Gereksinimler  
 **Başlık:** cvmarkers.h  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [C++ Kitaplık Başvurusu](../profiling/cpp-library-reference.md)




---
title: Cvınitprovider işlevi | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-debug
ms.topic: reference
f1_keywords:
- cvmarkers/CvInitProvider
helpviewer_keywords:
- CvInitProvider method
ms.assetid: ba1863ad-e35f-4d34-a2f2-5e68957d1915
caps.latest.revision: 8
author: MikeJo5000
ms.author: mikejo
manager: jillfra
ms.openlocfilehash: a5a8a9e70c85563e95037c754c59b6077ed21f28
ms.sourcegitcommit: 8b538eea125241e9d6d8b7297b72a66faa9a4a47
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54771875"
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

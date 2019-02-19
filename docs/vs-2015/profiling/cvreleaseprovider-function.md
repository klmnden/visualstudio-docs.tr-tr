---
title: CvReleaseProvider işlevi | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-debug
ms.topic: reference
f1_keywords:
- cvmarkers/CvReleaseProvider
helpviewer_keywords:
- CvReleaseProvider method
ms.assetid: 8d74379e-295d-452b-bd5f-0769df387d4f
caps.latest.revision: 8
author: MikeJo5000
ms.author: mikejo
manager: jillfra
ms.openlocfilehash: 7d5e611c2a964fcbb78a387a09989436e672ecd6
ms.sourcegitcommit: a83c60bb00bf95e6bea037f0e1b9696c64deda3c
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/19/2019
ms.locfileid: "54758312"
---
# <a name="cvreleaseprovider-function"></a>CvReleaseProvider İşlevi
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

İşaretleyici sağlayıcısını yayınlar. İşaretleyici sağlayıcısını serbest bu sağlayıcı dizi önceden oluşturulmuş işaret etkilemez. İşaret serisi CvReleaseMarkerSeries çağrı tarafından ayrı ayrı serbest bırakılması gerekir. Sağlayıcı yayımlamayı hatası bellek sızıntısına neden olur.  
  
## <a name="syntax"></a>Sözdizimi  
  
```  
HRESULT CvReleaseProvider(  
   _In_ PCV_PROVIDER pProvider  
);  
```  
  
#### <a name="parameters"></a>Parametreler  
 `pProvider`  
 Sağlayıcı bağlamı. NULL olamaz.  
  
## <a name="return-value"></a>Dönüş Değeri  
 S_OK sağlayıcısı başarıyla serbest bırakıldı veya hata kodu var. durumda tüm hatalar. Hata koşulu denetleyen için başarılı/başarısız makroları kullanın.  
  
## <a name="requirements"></a>Gereksinimler  
 **Başlık:** cvmarkers.h  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [C++ Kitaplık Başvurusu](../profiling/cpp-library-reference.md)

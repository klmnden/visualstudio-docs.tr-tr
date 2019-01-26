---
title: Cvısenabled işlevi | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
f1_keywords:
- cvmarkers/CvIsEnabledEx
- cvmarkers/CvIsEnabled
helpviewer_keywords:
- CvIsEnabled method
- CvIsEnabledEx method
ms.assetid: 2e4fea6d-758d-4150-8744-6102a1d58c1c
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 8af4da802ef0ad87831f2f67f47e8ffb66a969e7
ms.sourcegitcommit: 2193323efc608118e0ce6f6b2ff532f158245d56
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/25/2019
ms.locfileid: "54990049"
---
# <a name="cvisenabled-function"></a>Cvısenabled işlevi
Tüm oturum belirtilen ETW sağlayıcısı etkin olup olmadığını belirler.  
  
## <a name="syntax"></a>Sözdizimi  
  
```C  
HRESULT CvIsEnabled(  
   _In_ PCV_PROVIDER pProvider  
);  
HRESULT CvIsEnabledEx(  
   _In_ PCV_PROVIDER pProvider,  
   _In_ CV_IMPORTANCE level,  
   _In_ int category  
);  
```  
  
#### <a name="parameters"></a>Parametreler  
 `category`  
 Kategori.  
  
 `level`  
 Önem düzeyi.  
  
 `pProvider`  
 Geçerli sağlayıcı nesnesi. NULL olamaz.  
  
## <a name="return-value"></a>Dönüş değeri  
 Sağlayıcı etkinse S_OK. Sağlayıcı şu anda devre dışı bırakılırsa S_FALSE. Hata kodu: var olan herhangi bir hata durumunda. Hata koşulu denetleyen ve ardından S_OK/S_FALSE denetlemek için FAILED makrosunu kullanın.  
  
## <a name="requirements"></a>Gereksinimler  
 **Başlık:** *cvmarkers.h*  
  
## <a name="see-also"></a>Ayrıca bkz.  
 [C++ Kitaplık Başvurusu](../profiling/cpp-library-reference.md)
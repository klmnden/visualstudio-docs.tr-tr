---
title: DONT_SAVE_VSGLOG_TO_TEMP | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
ms.assetid: f27ab0e6-9575-4ca0-9901-37d3e5c3a2f5
author: mikejo5000
ms.author: mikejo
manager: douge
ms.workload:
- multiple
ms.openlocfilehash: d945f3ef7fe2c5aa2abb0bd2263bae693d517f7c
ms.sourcegitcommit: 37fb7075b0a65d2add3b137a5230767aa3266c74
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/02/2019
ms.locfileid: "53859165"
---
# <a name="dontsavevsglogtotemp"></a>DONT_SAVE_VSGLOG_TO_TEMP
Grafik günlük dosyası, kullanıcı için geçici dosyalar dizini kaydedilip kaydedilmediğini kendi varlığı tanımlar.  

## <a name="syntax"></a>Sözdizimi  

```C++  
#define DONT_SAVE_VSGLOG_TO_TEMP  
```  

## <a name="value"></a>Değer  
 Grafik günlük dosyası olup olmadığını belirler, kendi varlığı veya yokluğuna göre bir önişlemci sembolü kullanıcının geçici dosyalar dizinine kaydedilir. Bu simge tanımlanmadıysa sonra dosya adı tarafından tanımlanan `VSG_DEFAULT_RUN_FILENAME` yakalanan uygulamayı geçerli dizine göreli veya mutlak bir yol; Aksi takdirde, dosya adı tarafından tanımlanan `VSG_DEFAULT_RUN_FILENAME` ve kullanıcının geçici dosyalar dizini göreli olamaz mutlak bir yol.  

## <a name="remarks"></a>Açıklamalar  
 Kullanıcının ayrıcalıkları bağlı olarak, grafik günlük dosyasını rastgele bir konuma kaydedilmesi mümkün olmayabilir. Seçmek konumun kullanıcı tarafından yazılabilir olup emin değilseniz, grafik günlüklerini kullanıcının geçici dosyalar dizini veya bilinen iyi başka bir konuma kaydetmek tercih ettiğiniz öneririz.  

 Grafik günlük dosyası için geçici dosyalar dizini kaydedilmesini engellemek için gerekir tanımlanmış `DONT_SAVE_VSGLOG_TO_TEMP` dahil önce `vsgcapture.h`.  

## <a name="example"></a>Örnek  
 Bu örnek konak makinesi üzerinde mutlak bir yol için grafik günlük dosyasını kaydetmeyi nasıl gösterir.  

```cpp
// Define DONT_SAVE_VSGLOG_TO_TEMP and VSG_DEFAULT_RUN_FILENAME before including vsgcapture.h  
#define DONT_SAVE_VSGLOG_TO_TEMP  
#define VSG_DEFAULT_RUN_FILENAME L"C:\\Graphics Diagnostics Captures\\default.vsglog"  

#include <vsgcapture.h>  
```  

## <a name="see-also"></a>Ayrıca Bkz.  
 [VSG_DEFAULT_RUN_FILENAME](vsg-default-run-filename.md)

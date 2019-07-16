---
title: DONT_SAVE_VSGLOG_TO_TEMP | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-debug
ms.topic: conceptual
ms.assetid: f27ab0e6-9575-4ca0-9901-37d3e5c3a2f5
caps.latest.revision: 7
author: MikeJo5000
ms.author: mikejo
manager: jillfra
ms.openlocfilehash: 449c6c1ecdb0644b9b52b6ec12ce867dc34d66c4
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "68156099"
---
# <a name="dontsavevsglogtotemp"></a>DONT_SAVE_VSGLOG_TO_TEMP
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Grafik günlük dosyası, kullanıcı için geçici dosyalar dizini kaydedilip kaydedilmediğini kendi varlığı tanımlar.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp  
#define DONT_SAVE_VSGLOG_TO_TEMP  
```  
  
## <a name="value"></a>Değer  
 Grafik günlük dosyası olup olmadığını belirler, kendi varlığı veya yokluğuna göre bir önişlemci sembolü kullanıcının geçici dosyalar dizinine kaydedilir. Bu simge tanımlanmadıysa sonra dosya adı tarafından tanımlanan `VSG_DEFAULT_RUN_FILENAME` yakalanan uygulamayı geçerli dizine göreli veya mutlak bir yol; Aksi takdirde, dosya adı tarafından tanımlanan `VSG_DEFAULT_RUN_FILENAME` ve kullanıcının geçici dosyalar dizini göreli olamaz mutlak bir yol.  
  
## <a name="remarks"></a>Açıklamalar  
 Kullanıcının ayrıcalıkları bağlı olarak, grafik günlük dosyasını rastgele bir konuma kaydedilmesi mümkün olmayabilir. Seçmek konumun kullanıcı tarafından yazılabilir olup emin değilseniz, grafik günlüklerini kullanıcının geçici dosyalar dizini veya bilinen iyi başka bir konuma kaydetmek tercih ettiğiniz öneririz.  
  
 Grafik günlük dosyası için geçici dosyalar dizini kaydedilmesini engellemek için gerekir tanımlanmış `DONT_SAVE_VSGLOG_TO_TEMP` dahil önce `vsgcapture.h`.  
  
## <a name="example"></a>Örnek  
 Bu örnek konak makinesi üzerinde mutlak bir yol için grafik günlük dosyasını kaydetmeyi nasıl gösterir.  
  
```  
// Define DONT_SAVE_VSGLOG_TO_TEMP and VSG_DEFAULT_RUN_FILENAME before including vsgcapture.h  
#define DONT_SAVE_VSGLOG_TO_TEMP  
#define VSG_DEFAULT_RUN_FILENAME L"C:\\Graphics Diagnostics Captures\\default.vsglog"  
  
#include <vsgcapture.h>  
  
```  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [VSG_DEFAULT_RUN_FILENAME](../debugger/vsg-default-run-filename.md)

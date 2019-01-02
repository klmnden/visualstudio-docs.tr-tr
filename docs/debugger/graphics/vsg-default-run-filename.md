---
title: VSG_DEFAULT_RUN_FILENAME | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
ms.assetid: ea549d2f-c857-458c-93c7-bc5a2d11d15d
author: mikejo5000
ms.author: mikejo
manager: douge
ms.workload:
- multiple
ms.openlocfilehash: a05acfd07e8b67bf500864f00ead4d78f2da22ae
ms.sourcegitcommit: 37fb7075b0a65d2add3b137a5230767aa3266c74
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/02/2019
ms.locfileid: "53922566"
---
# <a name="vsgdefaultrunfilename"></a>VSG_DEFAULT_RUN_FILENAME
Grafik günlük dosyası varsayılan dosya adını tanımlar.  
  
## <a name="syntax"></a>Sözdizimi  
  
```C++  
#define VSG_DEFAULT_FILENAME filename  
```  
  
#### <a name="parameters"></a>Parametreler  
 `filename`  
 Grafik bilgilerini programla yakalandığında, varsayılan olarak grafik günlük dosyasına verilen dosya adı.  
  
## <a name="value"></a>Değer  
 Günlük dosyası grafik dosya adını temsil eden bir dize. Varsayılan olarak, L"default.vsglog".  
  
```C++  
#define VSG_DEFAULT_FILENAME L"default.vsglog"  
```  
  
## <a name="remarks"></a>Açıklamalar  
 Önişlemci sembolü `DONT_SAVE_VSGLOG_TO_TEMP` tanımlı, daha sonra dosya adı yakalanan uygulamayı geçerli dizine göreli veya mutlak bir yol; Aksi takdirde, bu kullanıcının geçici dosya dizinine göreli ve mutlak bir yol olamaz.  
  
 Dahil etmeden önce tanımlanan dosya adını değiştirmek için onu yeniden tanımlamalısınız `vsgcapture.h` programınızdaki.  
  
## <a name="example"></a>Örnek  
 Bu örnek yakalama dosya varsayılan dosya adını değiştirmek nasıl gösterir:  
  
```C++  
// Redefine the default capture filename before including vsgcapture.h  
#define VSG_DEFAULT_FILENAME L"capture.vsglog"  
  
#include <vsgcapture.h>  
```  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [DONT_SAVE_VSGLOG_TO_TEMP](dont-save-vsglog-to-temp.md)
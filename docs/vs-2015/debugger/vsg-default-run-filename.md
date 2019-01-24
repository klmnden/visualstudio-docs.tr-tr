---
title: VSG_DEFAULT_RUN_FILENAME | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-debug
ms.topic: conceptual
ms.assetid: ea549d2f-c857-458c-93c7-bc5a2d11d15d
caps.latest.revision: 7
author: MikeJo5000
ms.author: mikejo
manager: jillfra
ms.openlocfilehash: 2980d34028c58a6abadb2df21bf22c8d37cda6e0
ms.sourcegitcommit: 8b538eea125241e9d6d8b7297b72a66faa9a4a47
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54754158"
---
# <a name="vsgdefaultrunfilename"></a>VSG_DEFAULT_RUN_FILENAME
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Grafik günlük dosyası varsayılan dosya adını tanımlar.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp  
#define VSG_DEFAULT_FILENAME filename  
```  
  
#### <a name="parameters"></a>Parametreler  
 `filename`  
 Grafik bilgilerini programla yakalandığında, varsayılan olarak grafik günlük dosyasına verilen dosya adı.  
  
## <a name="value"></a>Değer  
 Günlük dosyası grafik dosya adını temsil eden bir dize. Varsayılan olarak, L"default.vsglog".  
  
```cpp  
#define VSG_DEFAULT_FILENAME L"default.vsglog"  
```  
  
## <a name="remarks"></a>Açıklamalar  
 Önişlemci sembolü `DONT_SAVE_VSGLOG_TO_TEMP` tanımlı, daha sonra dosya adı yakalanan uygulamayı geçerli dizine göreli veya mutlak bir yol; Aksi takdirde, bu kullanıcının geçici dosya dizinine göreli ve mutlak bir yol olamaz.  
  
 Dahil etmeden önce tanımlanan dosya adını değiştirmek için onu yeniden tanımlamalısınız `vsgcapture.h` programınızdaki.  
  
## <a name="example"></a>Örnek  
 Bu örnek yakalama dosya varsayılan dosya adını değiştirmek nasıl gösterir:  
  
```cpp  
// Redefine the default capture filename before including vsgcapture.h  
#define VSG_DEFAULT_FILENAME L"capture.vsglog"  
  
#include <vsgcapture.h>  
```  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [DONT_SAVE_VSGLOG_TO_TEMP](../debugger/dont-save-vsglog-to-temp.md)

---
title: VSG_DEFAULT_RUN_FILENAME | Microsoft Docs
ms.custom: ''
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.reviewer: ''
ms.suite: ''
ms.technology:
- vs-ide-debug
ms.tgt_pltfrm: ''
ms.topic: article
ms.assetid: ea549d2f-c857-458c-93c7-bc5a2d11d15d
caps.latest.revision: 7
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: 35f243cf021e5acbb169022ba8d9bc9a5ab4eacb
ms.sourcegitcommit: 9ceaf69568d61023868ced59108ae4dd46f720ab
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/12/2018
ms.locfileid: "49288580"
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




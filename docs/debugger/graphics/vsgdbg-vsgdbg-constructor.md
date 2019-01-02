---
title: VsgDbg::VsgDbg (oluşturucu) | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
ms.assetid: 670651e6-5e79-4845-b0c2-671beb7055a8
author: mikejo5000
ms.author: mikejo
manager: douge
ms.workload:
- multiple
ms.openlocfilehash: e282e63b81ecee4023934a235d4f524f8372311e
ms.sourcegitcommit: 37fb7075b0a65d2add3b137a5230767aa3266c74
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/02/2019
ms.locfileid: "53945580"
---
# <a name="vsgdbgvsgdbg-constructor"></a>VsgDbg::VsgDbg (Oluşturucu)
Örneği oluşturur `VsgDbg` sınıfı ile veya olmadan etkin şekilde Yakala ve belirtilen Boolean parametresini temel alan varsayılan olarak, grafik bilgilerini kaydetmek için grafik tanılama uygulama bileşeninin hazırlanıyor.  
  
## <a name="syntax"></a>Sözdizimi  
  
```C++  
VsgDbg(  
  bDefaultInit  
);  
```  
  
#### <a name="parameters"></a>Parametreler  
 `bDefaultInit`  
 `true` Grafik tanılama uygulama bileşeninin etkin bir şekilde yakalayıp grafik bilgilerini kaydetmek hazırlıklı olmanıza olduğunu belirtmek için; `false` uygulamayı etkin bir şekilde yakalayıp grafik bilgilerini şu anda kayıt için hazırlıklı olmalıdır değil olduğunu belirtmek için.  
  
## <a name="remarks"></a>Açıklamalar  
 Ne zaman Oluşturucu çağrıldığında ve `bDefaultInit` kümesine `true`, grafik günlük dosyasının dosya adı tarafından nasıl belirlenir `DONT_SAVE_VSGLOG_TO_TEMP` ve `VSG_DEFAULT_RUN_FILENAME` önişlemci sembolleri önce tanımlanan `vsgcapture.h` uygulamanızda dahildir.  
  
 Ne zaman Oluşturucu çağrıldığında `bDefaultInit` kümesine `false`, etkin bir şekilde yakalayıp çağırarak sonraki bir zamanda, grafik bilgilerini kaydetmek için grafik tanılama uygulama bileşeninin hazırlanabilir `Init` işlevi.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [VsgDbg:: ~ VsgDbg (yok edici)](vsgdbg-tilde-vsgdbg-destructor.md)   
 [Init](init.md)   
 [DONT_SAVE_VSGLOG_TO_TEMP](dont-save-vsglog-to-temp.md)   
 [VSG_DEFAULT_RUN_FILENAME](vsg-default-run-filename.md)
---
title: VsgDbg::VsgDbg (oluşturucu) | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
ms.assetid: 670651e6-5e79-4845-b0c2-671beb7055a8
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: b4c4c987bd0f44f6b8a4bad945d249aaf832fc57
ms.sourcegitcommit: 2193323efc608118e0ce6f6b2ff532f158245d56
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/25/2019
ms.locfileid: "55035282"
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
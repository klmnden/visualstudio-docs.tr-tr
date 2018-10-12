---
title: VsgDbg::VsgDbg (oluşturucu) | Microsoft Docs
ms.custom: ''
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.reviewer: ''
ms.suite: ''
ms.technology:
- vs-ide-debug
ms.tgt_pltfrm: ''
ms.topic: article
ms.assetid: 670651e6-5e79-4845-b0c2-671beb7055a8
caps.latest.revision: 7
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: 2a3188116e3b0316ccb6f3892bdd12d7e7ee2677
ms.sourcegitcommit: 9ceaf69568d61023868ced59108ae4dd46f720ab
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/12/2018
ms.locfileid: "49251816"
---
# <a name="vsgdbgvsgdbg-constructor"></a>VsgDbg::VsgDbg (Oluşturucu)
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Örneği oluşturur `VsgDbg` sınıfı ile veya olmadan etkin şekilde Yakala ve belirtilen Boolean parametresini temel alan varsayılan olarak, grafik bilgilerini kaydetmek için grafik tanılama uygulama bileşeninin hazırlanıyor.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp  
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
 [VsgDbg:: ~ VsgDbg (yok edici)](../debugger/vsgdbg-tilde-vsgdbg-destructor.md)   
 [Init](../debugger/init.md)   
 [DONT_SAVE_VSGLOG_TO_TEMP](../debugger/dont-save-vsglog-to-temp.md)   
 [VSG_DEFAULT_RUN_FILENAME](../debugger/vsg-default-run-filename.md)




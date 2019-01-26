---
title: Yerel çalışma zamanı denetimleri özelleştirme | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
f1_keywords:
- vs.debug.crt
dev_langs:
- CSharp
- VB
- FSharp
- C++
- JScript
helpviewer_keywords:
- runtime_checks pragma
- debugger, native run-time checks
- /RTC compiler option [C++], native run-time checks
- customizing CRT error checking
- native run-time checks, customizing
ms.assetid: 76a365fe-6439-49db-8603-34058b78e5a8
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- cplusplus
ms.openlocfilehash: 450c69ccffaa35b9dbe519782b28067e6f2beb8f
ms.sourcegitcommit: 2193323efc608118e0ce6f6b2ff532f158245d56
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/25/2019
ms.locfileid: "54954091"
---
# <a name="native-run-time-checks-customization"></a>Yerel Çalışma Zamanı Denetimlerini Özelleştirme
Derleme yaptığınızda **/RTC** (çalışma zamanı denetimleri) veya `runtime_checks` pragması, C çalışma zamanı kitaplığı, yerel çalışma zamanı denetimleri sağlar. Bazı durumlarda, çalışma zamanı denetimi özelleştirmek isteyebilirsiniz:  
  
- Bir dosya ya da varsayılan dışındaki hedef çalışma zamanı denetimi iletileri yönlendirmek için.  
  
- Hedef çalışma zamanı için bir çıktı belirtmek için üçüncü taraf hata ayıklayıcı altında iletileri denetleyin.  
  
- Çalışma zamanı denetimi iletileri yayın sürümü C çalışma zamanı kitaplığı ile derlenmiş bir programdan bildirmek için. Kitaplık sürümleri kullanmayın `_CrtDbgReportW` çalışma zamanı hatalarını raporlamak için. Bunun yerine, görüntüledikleri bir **Assert** her bir çalışma zamanı hata iletişim kutusu.  
  
  Çalışma zamanı hata denetimi özelleştirmek için şunları yapabilirsiniz:  
  
- Çalışma zamanı hata raporlama işlevi yazma. Daha fazla bilgi için [nasıl yapılır: Bir çalışma zamanı hata raporlama işlevi yazma](../debugger/how-to-write-a-run-time-error-reporting-function.md).  
  
- Hata iletisi hedef özelleştirin.  
  
- Sorgu çalıştırma hakkında bilgi için hataları kontrol edin.  
  
## <a name="customize-the-error-message-destination"></a>Hata iletisi hedef özelleştirme  
 Kullanırsanız `_CrtDbgReportW` hatalarını raporlamak için kullanabileceğiniz `_CrtSetReportMode` hata iletileri hedefini belirlemek için.  
  
 Özel bir raporlama işlevini kullanıyorsanız `_RTC_SetErrorType` bir hata rapor türü ile ilişkilendirilecek.  
  
## <a name="query-for-information-about-run-time-checks"></a>Sorgu için çalışma zamanı denetimleri hakkında bilgi  
 `_RTC_NumErrors` çalışma zamanı hata denetimleri tarafından algılanan hata türlerinin sayısını döndürür. Her hata kısa bir açıklamasını almak için 0'dan dönüş değeri olarak döngüye girer `_RTC_NumErrors`, yineleme değeri geçirme `_RTC_GetErrDesc` her döngüde. Daha fazla bilgi için [_RTC_NumErrors](/cpp/c-runtime-library/reference/rtc-numerrors) ve [_RTC_GetErrDesc](/cpp/c-runtime-library/reference/rtc-geterrdesc).  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Nasıl yapılır: Yerel çalışma zamanı denetimlerini kullanma](../debugger/how-to-use-native-run-time-checks.md)   
 [runtime_checks](/cpp/preprocessor/runtime-checks)   
 [_CrtDbgReport, _CrtDbgReportW](/cpp/c-runtime-library/reference/crtdbgreport-crtdbgreportw)
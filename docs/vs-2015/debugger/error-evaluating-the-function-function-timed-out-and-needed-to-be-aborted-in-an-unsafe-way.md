---
title: 'Hata: İşlev değerlendirme &#39;işlevi&#39; zaman aşımına uğradı ve güvenli bir şekilde iptal edilmesi gerekti | Microsoft Docs'
ms.date: 11/15/2016
ms.topic: reference
f1_keywords:
- vs.debug.error.unsafe_func_eval_abort
ms.assetid: 0a9f70ed-21ad-4a10-8535-b9c5885ad8f4
caps.latest.revision: 9
author: MikeJo5000
ms.author: mikejo
manager: jillfra
ms.openlocfilehash: 5d5a992751e31f21a7875091b4c8b1be9bd0bd0a
ms.sourcegitcommit: 8b538eea125241e9d6d8b7297b72a66faa9a4a47
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54790558"
---
# <a name="error-evaluating-the-function-39function39-timed-out-and-needed-to-be-aborted-in-an-unsafe-way"></a>Hata: İşlev değerlendirme &#39;işlevi&#39; zaman aşımına uğradı ve güvenli bir şekilde iptal edilmesi gerekti
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Tüm ileti metni: 'Function' işlevinin değerlendirilmesi zaman aşımına uğradı ve güvenli bir şekilde iptal edilmesi gerekti. Bu hedef işlemi bozmuş olabilir. 

.NET nesnelerinin durumunu incelemek daha kolay hale getirmek için ek kod (genellikle özellik alıcı yöntemlere ve ToString işlevleri) çalıştırmak için hataları ayıklanan işlem otomatik olarak hata ayıklayıcı zorlar. Çoğu tüm senaryolarda, bu işlevler hızla tamamlayın ve çok daha kolay hata ayıklama yapın. Ancak, hata ayıklayıcı korumalı alanda uygulama çalışmaz. Sonuç olarak, özellik alıcısı veya yanıt vermemeye başlıyor yerel bir işleve çağrı ToString yöntemini kurtarılamayabilir uzun zaman aşımları için neden olabilir. Bu hata iletisiyle karşılaşırsanız, bu durum oluştu.
 
Bu sorun için yaygın nedenlerinden biri hata ayıklayıcı bir özellik değerlendirdiğinde, yalnızca yürütmek için denetlenen iş parçacığı olanak sağlamasıdır. Bu nedenle özelliği içinde hata ayıklanan uygulamayı çalıştırmak için diğer iş parçacıkları üzerinde bekleyen ve .NET çalışma zamanı kesme mümkün olmayan bir şekilde bekliyorsa, bu sorunu gerçekleşir.
 
## <a name="to-correct-this-error"></a>Bu hatayı düzeltmek için
 
Bu sorun için üç olası çözümü vardır.
 
### <a name="solution-1-prevent-the-debugger-from-calling-the-getter-property-or-tostring-method"></a>Çözüm #1: Hata ayıklayıcısı özellik alıcı veya ToString yöntemini çağırmasını engellemek
 
Hata iletisi, hata ayıklayıcı ulaşmaya çalıştık işlevin adını bildirir. Bu işlev değiştirebilir, özellik alıcısı veya ToString yöntemini çağırma, hata ayıklayıcı engelleyebilirsiniz. Aşağıdakilerden birini deneyin:
 
* Yöntem başka türde bir özellik alıcısı yanı sıra kodu değiştirin veya ToString yöntemi ve sorunu kaybolur.
    -veya-
* (ToString için) DebuggerDisplay özniteliği türüne tanımlayın ve ToString dışında bir şey değerlendirmek hata ayıklayıcı olabilir.
    -veya-
* (Özellik alıcısı için) PUT `[System.Diagnostics.DebuggerBrowsable(DebuggerBrowsableState.Never)]` özelliği özniteliği. Bu API Uyumluluk nedenleriyle bir özellik kalması gereken bir yöntem varsa yararlı olabilir, ancak gerçekten bir yöntemi olması gerekir.
 
### <a name="solution-2-have-the-target-code-ask-the-debugger-to-abort-the-evaluation"></a>Çözüm #2: Değerlendirme iptal etmek için hata ayıklayıcı isteyin hedef kodu
 
Hata iletisi, hata ayıklayıcı ulaşmaya çalıştık işlevin adını bildirir. ToString yöntemi ve özellik alıcısı bazen düzgün çalışması başarısız sorunu olduğu, özellikle durumlarda kod kodu çalıştırmak için başka bir iş parçacığı gerekir ve ardından uygulama işlevi çağırabilir `System.Diagnostics.Debugger.NotifyOfCrossThreadDependency` işlevi iptal etmek için hata ayıklayıcı istemek için Değerlendirme. Bu çözüm ile açıkça bu işlevler değerlendirmek yine de mümkündür, ancak NotifyOfCrossThreadDependency çağrısı yapıldığında yürütmeyi durdurur varsayılan davranıştır.
 
### <a name="solution-3-disable-all-implicit-evaluation"></a>Çözüm #3: Tüm örtülü değerlendirme devre dışı bırak
 
Önceki çözümler sorunu yoksa, Git *Araçları* / *seçenekleri*, ayarı kaldırın *hata ayıklama*  /   *Genel* / *özellik değerlendirmesini ve diğer örtük işlev çağrılarını etkinleştir*. Bu, çoğu örtük İşlev değerlendirmesi devre dışı bırakır ve sorun çözülebilir.

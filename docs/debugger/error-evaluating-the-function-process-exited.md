---
title: 'Hata: Hedef işlem şu kodla sonlandı &#39;kod&#39; işlevi değerlendirilirken &#39;işlevi&#39; | Microsoft Docs'
ms.date: 4/06/2018
ms.topic: troubleshooting
f1_keywords:
- vs.debug.error.process_exit_during_func_eval
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 75d82b6011a0dfa7f2c388e7d5f39a9ebabcd663
ms.sourcegitcommit: b0d8e61745f67bd1f7ecf7fe080a0fe73ac6a181
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/22/2019
ms.locfileid: "56698176"
---
# <a name="error-the-target-process-exited-with-code-39code39-while-evaluating-the-function-39function39"></a>Hata: Hedef işlem şu kodla sonlandı &#39;kod&#39; işlevi değerlendirilirken &#39;işlevi&#39;

Tüm ileti metni: Hedef işlem, ' % s'function 'işlevini değerlendirirken 'code' koduyla çıkıldı.

.NET nesnelerinin durumunu incelemek kolaylaştırmak için hata ayıklayıcı ek kodu çalıştırmak için hataları ayıklanan işlem otomatik olarak zorlayacak (genellikle özellik alıcı yöntemlere ve `ToString` işlevler). Çoğu senaryoda, bu işlevlerin başarıyla tamamlanması veya hata ayıklayıcı tarafından yakalanan özel durumlar. Ancak, bunlar çekirdek sınırlarını geçen kullanıcı ileti Pompalama gerektirir veya kurtarılamaz olarak kabul edilir, özel durumlar yakalanamaz bazı durumlar vardır. Bir sonuç, özellik alıcısı veya kod yürüten ToString yöntemi bu da açıkça sonlandırır işlemi (örneğin, çağrıları `ExitProcess()`) veya yakalanamaz işlenmeyen bir özel durum oluşturur (örneğin, `StackOverflowException`) sona erer hataları ayıklanan işlem ve hata ayıklama oturumunu. Bu hata iletisiyle karşılaşırsanız, bu durum oluştu.

Bu sorun için yaygın nedenlerinden biri, hata ayıklayıcı kendisini çağıran bir özelliği değerlendirirken, bu bir yığın taşması özel durumu sonuçlanabilir ' dir. Yığın taşması özel durumuna geri alınamaz ve hedef işlem sonlandırılır.

## <a name="to-correct-this-error"></a>Bu hatayı düzeltmek için

Bu sorunun iki olası çözümü vardır.

### <a name="solution-1-prevent-the-debugger-from-calling-the-getter-property-or-tostring-method"></a>Çözüm #1: Hata ayıklayıcısı özellik alıcı veya ToString yöntemini çağırmasını engellemek 

Hata iletisi, hata ayıklayıcı ulaşmaya çalıştık işlevin adını bildirir. İşlev adı ile bu işlevi yeniden değerlendirmeyi deneyebilirsiniz **hemen** değerlendirme hata ayıklamak için penceresi. Hata ayıklama mümkün gelen değerlendirirken **hemen** penceresi olduğundan, örtük değerlendirmeleri farklı olarak **Yereller/değişkenler/Watch** windows hata ayıklayıcı, işlenmemiş özel durumlarda keser.

Bu işlev değiştirebilir, özellik Get yordamı çağırma hata ayıklayıcı engelleyebilir veya `ToString` yöntemi. Aşağıdakilerden birini deneyin:

* Yöntem başka türde bir özellik alıcısı yanı sıra kodu değiştirin veya ToString yöntemi ve sorunu kaybolur.
    -veya-
* (İçin `ToString`) tanımla bir `DebuggerDisplay` öznitelik türü ve hata ayıklayıcı dışında bir şey değerlendirmek olabilir `ToString`.
    -veya-
* (Özellik alıcısı için) PUT `[System.Diagnostics.DebuggerBrowsable(DebuggerBrowsableState.Never)]` özelliği özniteliği. Bu API Uyumluluk nedenleriyle bir özellik kalması için gereken bir yöntem varsa yararlı olabilir, ancak gerçekten bir yöntemi olması gerekir.

Bu yöntem değişiklik yapamazsınız, alternatif bir yönerge hedef işlem kurtulmayı ve değerlendirmeyi yeniden deneme mümkün olabilir.

### <a name="solution-2-disable-all-implicit-evaluation"></a>Çözüm #2: Tüm örtülü değerlendirme devre dışı bırak

Önceki çözümler sorunu yoksa, Git **Araçları** > **seçenekleri**, ayarı kaldırın **hata ayıklama**  >   **Genel** > **özellik değerlendirmesini ve diğer örtük işlev çağrılarını etkinleştir**. Bu, çoğu örtük İşlev değerlendirmesi devre dışı bırakır ve sorun çözülebilir.

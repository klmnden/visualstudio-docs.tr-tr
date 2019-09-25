---
title: Yerel kodda hata ayıklama | Microsoft Docs
ms.date: 04/11/2017
ms.topic: conceptual
f1_keywords:
- vs.debug
dev_langs:
- CSharp
- VB
- FSharp
- C++
helpviewer_keywords:
- debugging native code
- debugging [C++], native code
- debugging [Visual Studio], native code
- native code, debugging
ms.assetid: d94eee90-7e0d-4cac-88c1-9831030daa5e
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- cplusplus
ms.openlocfilehash: 8115d16b64096af343adb918ba4855d9655d4df0
ms.sourcegitcommit: ea182703e922c74725045afc251bcebac305068a
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/24/2019
ms.locfileid: "71211151"
---
# <a name="debugging-native-code"></a>Yerel Kodda Hata Ayıklama
Bu bölümde, yerel uygulamalar için bazı yaygın hata ayıklama sorunları ve teknikleri ele alınmaktadır. Bu bölümde ele alınan teknikler, üst düzey tekniklerdir. Visual Studio hata ayıklayıcısını kullanmanın mekanizması için bkz. [ilk olarak hata ayıklayıcıya](../debugger/debugger-feature-tour.md)bakın.

## <a name="in-this-section"></a>Bu Bölümde
 [Nasıl yapılır: En iyi duruma](../debugger/how-to-debug-optimized-code.md) getirilmiş kod hata ayıklama için en iyi duruma getirilmiş kodda hata ayıklama ipuçları, hata ayıklama ve sürüm yapılandırmalarının varsayılan iyileştirme ayarları ve yalnızca İyileştirilmiş Kodda görünür (hata ayıklama yapı yapılandırmasında iyileştirmesi açılıyor).

 [DebugBreak ve __debugbreak](../debugger/debugbreak-and-debugbreak.md) Win32 `DebugBreak` işlevini açıklar ve Platform SDK 'sında başvuru konusuna bir bağlantı sağlar. Ayrıca, `__debugbreak` iç öğesini açıklar.

 [C/C++ ](../debugger/c-cpp-assertions.md) onaylar onay deyimlerini, bunların nasıl çalıştığını, bunları kullanmanın avantajlarını (mantık hatalarını yakalama, bir işlemin sonuçlarını ve hata koşullarını test etmeyi), ile `_DEBUG`etkileşimini ve onaylama türlerini tartışır sürümünde [!INCLUDE[vsprvs](../code-quality/includes/vsprvs_md.md)]desteklenir.

 [Nasıl yapılır: Satır içi derleme kodunda](../debugger/how-to-debug-inline-assembly-code.md) hata ayıklama kodu, kayıt içeriğini görüntülemek ve bu pencereler hakkındaki konuların bağlantılarını sağlamak üzere derleme yönergelerini ve Yazmaçları penceresini görüntülemek için ayrıştırma penceresini kullanmayla ilgili kısa yönergeler sağlar.

 [MFC hata ayıklama teknikleri](../debugger/mfc-debugging-techniques.md) MFC programları için hata ayıklama tekniklerine bağlantı sağlar: afxDebugBreak, Izleme makrosu, MFC 'de bellek sızıntılarını algılama, MFC onayları ve MFC hata ayıklama derlemeleri boyutunu azaltma.

 [CRT hata ayıklama teknikleri](../debugger/crt-debugging-techniques.md) CRT hata ayıklama kitaplığı, raporlama makroları, malloc ve _malloc_dbg arasındaki farklılıklar, hata ayıklama kanca işlevleri ve CRT hata ayıklama yığını gibi C çalışma zamanı kitaplığı için hata ayıklama tekniklerine bağlantı sağlar.

 [Yerel kod SSS hatalarını ayıklama](../debugger/debugging-native-code-faqs.md) Görsel C++ programlarda hata ayıklama hakkında sık sorulan soruların yanıtlarını sağlar

 [Com ve ActiveX hata ayıklaması](../debugger/com-and-activex-debugging.md) Com ve ActiveX hata ayıklaması için kullanabileceğiniz araçlar da dahil olmak üzere COM ve ActiveX uygulamalarının hatalarını ayıklama hakkında bilgi sağlar.

 [Nasıl yapılır: Eklenen kodun](../debugger/how-to-debug-injected-code.md) hatalarını ayıklama öznitelikleri kullanan hata ayıklama kodu hakkında rehberlik sağlar. Kaynak ek açıklamanın nasıl kullanılacağı, eklenen kodun nasıl görüntüleneceği ve geçerli yürütme noktasındaki ayrıştırılmış kodu nasıl görüntüleneceği hakkında yönergeler içerir.

 [İzlenecek yol: Paralel uygulamada](../debugger/walkthrough-debugging-a-parallel-application.md) hata ayıklama paralel bir uygulamada hata ayıklamak için paralel **Görevler** ve **Paralel Yığınlar** araç pencerelerinin nasıl kullanılacağını açıklar.

## <a name="related-sections"></a>İlgili Bölümler
 [Görsel C++ proje türleri](../debugger/debugging-preparation-visual-cpp-project-types.md) , görsel C++ proje şablonları tarafından oluşturulan yerel proje türlerinde hata ayıklamanın nasıl yapılacağını betimleyen konuların bağlantılarını sağlar.

 [DLL projelerinde hata ayıklama](../debugger/debugging-dll-projects.md) Yerel ve yönetilen DLL 'Lerde hata ayıklama hakkında bilgi sağlar.

 [Hata ayıklayıcıya ilk bakış](../debugger/debugger-feature-tour.md) Hata ayıklama belgelerinin daha büyük bölümlerine bağlantılar sağlar. Bilgiler hata ayıklayıcıdaki yenilikleri, ayarlar ve hazırlık, kesme noktaları, özel durumları işleme, düzenleme ve devam etme, yönetilen kod hatalarını ayıklama, yerel kodda hata ayıklama, SQL hata ayıklama ve Kullanıcı arabirimi başvurularına dahildir.

## <a name="see-also"></a>Ayrıca Bkz.

- [Hata Ayıklayıcısı Güvenliği](../debugger/debugger-security.md)
- [Visual Studio’da hata ayıklama](../debugger/index.yml)
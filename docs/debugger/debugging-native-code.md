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
ms.openlocfilehash: 5a7cf0b150c45037941010bf7e611f4bc21252c7
ms.sourcegitcommit: f7c401a376ce410336846835332a693e6159c551
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/14/2019
ms.locfileid: "57870421"
---
# <a name="debugging-native-code"></a>Yerel Kodda Hata Ayıklama
Bu bölüm, bazı yaygın hata ayıklama sorunları ve yerel uygulamalar için teknikleri kapsar. Bu bölümde yer alan teknikleri, üst düzey tekniklerle aynıdır. Visual Studio hata ayıklayıcısını kullanarak mekanizması için bkz: [hata ayıklayıcıya ilk bakış](../debugger/debugger-feature-tour.md)).

## <a name="in-this-section"></a>Bu Bölümde
 [Nasıl yapılır: Optimize edilmiş kodda hata ayıklama](../debugger/how-to-debug-optimized-code.md) verir ipuçları en iyi duruma getirilmiş kodu, özellikle hata ayıklama için neden hata ayıklama, programınızın hata ayıklama ve yayın yapılandırmaları için varsayılan iyileştirme ayarlarını iyileştirilmemiş bir sürümü ve bulma, yalnızca hatalar için ipuçları (hata ayıklama yapısı yapılandırması iyileştirme özelliğini) en iyi duruma getirilmiş kodda görünür.

 [DebugBreak ve __debugbreak](../debugger/debugbreak-and-debugbreak.md) Win32 açıklar `DebugBreak` işlev ve Platform SDK'sında, başvuru konularına bağlantı sağlar. Ayrıca açıklar `__debugbreak` iç.

 [C/C++ onaylamaları](../debugger/c-cpp-assertions.md) onaylama deyimleri, nasıl çalıştıklarını, (bir işleminin sonuçlarını denetleme ve hata koşulları test çalýþýrçalýþma yakalama mantık hataları,), bunları kullanmanın avantajları anlatılmaktadır kendi etkileşim `_DEBUG`ve türleri desteklenen bir onayları [!INCLUDE[vsprvs](../code-quality/includes/vsprvs_md.md)].

 [Nasıl yapılır: Satır içi derleme kodunda hata ayıklama](../debugger/how-to-debug-inline-assembly-code.md) kısa yönergeleri görüntülemek için derleme yönergeleri ve yazmaçlar penceresini görüntülemek için ayrıştırma penceresini kullanarak içeriği kaydedin ve bu windows ile ilgili konulara bağlantılar sağlar.

 [MFC hata ayıklama teknikleri](../debugger/mfc-debugging-techniques.md) teknikleri dahil olmak üzere, MFC programları için hata ayıklama için bağlantılar: afxDebugBreak, bellek algılama TRACE makrosu, MFC, MFC onaylar sızıntıları ve MFC hata ayıklama boyutunu küçültmeyi oluşturur.

 [CRT hata ayıklama teknikleri](../debugger/crt-debugging-techniques.md) CRT hata ayıklama kitaplığı, raporlama için makroları kullanma dahil olmak üzere C çalışma zamanı kitaplığı hata ayıklama tekniklerine için bağlantılar, malloc ve hata ayıklama kanca işlevlerini ve CRT hata ayıklama yığın yazma _malloc_dbg, farklar.

 [Yerel kod hata ayıklaması SSS](../debugger/debugging-native-code-faqs.md) Visual C++ programlarında hata ayıklama hakkında sık sorulan soruların yanıtlarını sağlar

 [COM ve ActiveX hata ayıklaması](../debugger/com-and-activex-debugging.md) COM için kullanabileceğiniz araçlar dahil olmak üzere, COM ve ActiveX uygulamalarında hata ayıklama ve ActiveX hata ayıklaması hakkında bilgi sağlar.

 [Nasıl yapılır: Eklenen kodda hata ayıklama](../debugger/how-to-debug-injected-code.md) öznitelikleri kullanan kodu hata ayıklama hakkında rehberlik sağlar. Kaynak ek açıklama üzerinde devre dışı bırakma, eklenen kodu görüntüleme ve geçerli yürütme noktasına ayrıştırılmış kodu görüntüleme yönergeleri içerir.

 [İzlenecek yol: Paralel uygulamada hata ayıklama](../debugger/walkthrough-debugging-a-parallel-application.md) nasıl kullanılacağını açıklar **Paralel Görevler** ve **Paralel Yığınlar** paralel uygulamada hata ayıklamak için windows aracı.

## <a name="related-sections"></a>İlgili Bölümler
 [Visual C++ proje türleri](../debugger/debugging-preparation-visual-cpp-project-types.md) hata ayıklama Visual C++ proje şablonları tarafından oluşturulan yerel proje türleri açıklayan konulara bağlantılar sağlar.

 [DLL projelerinde hata ayıklama](../debugger/debugging-dll-projects.md) yerel ve yönetilen DLL'lerin hata ayıklama hakkında bilgi sağlar.

 [Hata ayıklayıcıya ilk bakış](../debugger/debugger-feature-tour.md) hata ayıklama belgesinin en geniş bölümlerine bağlantılar sağlar. Bilgileri içeren hata ayıklayıcı, ayarlar ve hazırlık, kesme noktaları, özel durumların işlenmesi yenilikler Düzenle ve devam et, yönetilen kodda hata ayıklama, yerel kodda hata ayıklama, SQL ve kullanıcı arabirimi başvuruları hata ayıklama.

## <a name="see-also"></a>Ayrıca Bkz.

- [Hata Ayıklayıcısı Güvenliği](../debugger/debugger-security.md)
- [Visual Studio’da hata ayıklama](../debugger/index.md)
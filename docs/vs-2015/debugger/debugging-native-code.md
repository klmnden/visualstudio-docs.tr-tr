---
title: Yerel kodda hata ayıklama | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-debug
ms.topic: conceptual
f1_keywords:
- vs.debug
dev_langs:
- FSharp
- VB
- CSharp
- C++
- C++
helpviewer_keywords:
- debugging native code
- debugging [C++], native code
- debugging [Visual Studio], native code
- native code, debugging
ms.assetid: d94eee90-7e0d-4cac-88c1-9831030daa5e
caps.latest.revision: 24
author: MikeJo5000
ms.author: mikejo
manager: jillfra
ms.openlocfilehash: 61ee852f75737d85604fda106b15e61dc3634899
ms.sourcegitcommit: 8b538eea125241e9d6d8b7297b72a66faa9a4a47
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54773595"
---
# <a name="debugging-native-code"></a>Yerel Kodda Hata Ayıklama
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Bu bölüm, bazı yaygın hata ayıklama sorunları ve yerel uygulamalar için teknikleri kapsar. Bu bölümde yer alan teknikleri, üst düzey tekniklerle aynıdır. Visual Studio hata ayıklayıcısını kullanarak mekanizması için bkz: [hata ayıklayıcı yol haritası](../debugger/debugger-basics.md).  
  
## <a name="in-this-section"></a>Bu Bölümde  
 [Nasıl yapılır: İyileştirilmiş Kodda Hata Ayıklama](../debugger/how-to-debug-optimized-code.md)  
 Hata ayıklama, program, hata ayıklama ve yayın yapılandırmaları için varsayılan iyileştirme ayarlarını ve yalnızca en iyi duruma getirilmiş kod (açma görünen hataları bulmaya yönelik ipuçları iyileştirilmemiş bir sürümü neden hata ayıklama ipuçları sağlar, özellikle en iyileştirilmiş kodda iyileştirme hata ayıklama yapısı yapılandırması).  
  
 [DebugBreak ve __debugbreak](../debugger/debugbreak-and-debugbreak.md)  
 Win32 açıklar `DebugBreak` işlev ve Platform SDK'sında, başvuru konularına bağlantı sağlar. Ayrıca açıklar `__debugbreak` iç.  
  
 [C/C++ Onaylamaları](../debugger/c-cpp-assertions.md)  
 Onaylama deyimleri, nasıl çalıştıklarını, (bir işleminin sonuçlarını denetleme ve hata koşulları test çalýþýrçalýþma yakalama mantık hataları,), bunları kullanmanın avantajları anlatılmaktadır kendi etkileşim `_DEBUG`, desteklenen bir onayları türleri [!INCLUDE[vsprvs](../includes/vsprvs-md.md)].  
  
 [Nasıl yapılır: Satır İçi Derleme Kodunda Hata Ayıklama](../debugger/how-to-debug-inline-assembly-code.md)  
 YAZMAÇ içerikleri görüntülemek için derleme yönergeleri ve yazmaçlar penceresini görüntülemek için Ayrıştırılmış kod penceresini kullanma hakkında kısa yönerge sağlar ve bu windows ile ilgili konulara bağlantılar sağlar.  
  
 [MFC Hata Ayıklama Teknikleri](../debugger/mfc-debugging-techniques.md)  
 Teknikleri dahil olmak üzere, MFC programları için hata ayıklama için bağlantılar: afxDebugBreak, bellek algılama TRACE makrosu, MFC, MFC onaylar sızıntıları ve MFC hata ayıklama boyutunu küçültmeyi oluşturur.  
  
 [CRT Hata Ayıklama Teknikleri](../debugger/crt-debugging-techniques.md)  
 Bağlantıları, CRT hata ayıklama kitaplığı, raporlama, farklılıklardan malloc ve _malloc_dbg, yazma için makroları kullanma dahil olmak üzere C çalışma zamanı kitaplığı hata ayıklama tekniklerine hata ayıklama kanca işlevlerini ve CRT hata ayıklama yığını.  
  
 [Yerel Kodda Hata Ayıklama SSS](../debugger/debugging-native-code-faqs.md)  
 Visual C++ programlarında hata ayıklama hakkında sık sorulan soruların yanıtlarını sağlar  
  
 [COM ve ActiveX Hata Ayıklaması](../debugger/com-and-activex-debugging.md)  
 COM için kullanabileceğiniz araçları da dahil olmak üzere, COM ve ActiveX uygulamalarında hata ayıklama ve ActiveX hata ayıklaması hakkında bilgi sağlar.  
  
 [Nasıl yapılır: Yerel DLL'lerde Hata Ayıklama](../debugger/how-to-debug-native-dlls.md)  
 DLL dosyaları için yerel kod hata ayıklamayı kurma açıklanmaktadır.  
  
 [Nasıl yapılır: Eklenen Kodda Hata Ayıklama](../debugger/how-to-debug-injected-code.md)  
 Öznitelikleri kullanan kod hata ayıklamayı konusunda rehberlik yapmaktadır. Kaynak ek açıklama üzerinde devre dışı bırakma, eklenen kodu görüntüleme ve geçerli yürütme noktasına ayrıştırılmış kodu görüntüleme yönergeleri içerir.  
  
 [İzlenecek yol: Paralel Uygulamada Hata Ayıklama](../debugger/walkthrough-debugging-a-parallel-application.md)  
 Nasıl kullanılacağını açıklar **Paralel Görevler** ve **Paralel Yığınlar** paralel uygulamada hata ayıklamak için windows aracı.  
  
## <a name="related-sections"></a>İlgili Bölümler  
 [Visual C++ Proje Türleri](../debugger/debugging-preparation-visual-cpp-project-types.md)  
 Hata ayıklama Visual C++ proje şablonları tarafından oluşturulan yerel proje türleri açıklayan konulara bağlantılar sağlar.  
  
 [Visual Studio’da hata ayıklama](../debugger/debugging-in-visual-studio.md)  
 Hata ayıklama belgesinin en geniş bölümlerine bağlantılar sağlar. Bilgileri içeren hata ayıklayıcı, ayarlar ve hazırlık, kesme noktaları, özel durumların işlenmesi yenilikler Düzenle ve devam et, yönetilen kodda hata ayıklama, yerel kodda hata ayıklama, SQL ve kullanıcı arabirimi başvuruları hata ayıklama.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Hata ayıklayıcısı güvenliği](../debugger/debugger-security.md)   
 [Visual Studio’da hata ayıklama](../debugger/debugging-in-visual-studio.md)

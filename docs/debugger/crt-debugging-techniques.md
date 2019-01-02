---
title: CRT hata ayıklama tekniklerine | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
f1_keywords:
- c.runtime.debugging
dev_langs:
- CSharp
- VB
- FSharp
- C++
helpviewer_keywords:
- debugging [CRT]
- CRT, debugging
- debugging [C++], CRT debug support
ms.assetid: 9be561f6-14a8-44ff-925d-d911d5b8e6ff
author: mikejo5000
ms.author: mikejo
manager: douge
ms.workload:
- multiple
ms.openlocfilehash: 99edc41e86d492e8a38341917de1a5d7543dc93d
ms.sourcegitcommit: 37fb7075b0a65d2add3b137a5230767aa3266c74
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/02/2019
ms.locfileid: "53889117"
---
# <a name="crt-debugging-techniques"></a>CRT Hata Ayıklama Teknikleri
C çalışma zamanı kitaplığı kullanan bir programı hata ayıklaması yapıyorsanız, bu hata ayıklama teknikleri yararlı olabilir.  
  
## <a name="in-this-section"></a>Bu Bölümde  
 [CRT Hata Ayıklama Kitaplığı Kullanımı](../debugger/crt-debug-library-use.md)  
 C çalışma zamanı kitaplığı tarafından sağlanan hata ayıklama desteğini açıklar ve araçlara erişmek için yönergeler sağlar.  
  
 [Raporlama Makroları](../debugger/macros-for-reporting.md)  
 Hakkında bilgi sağlar **_RPTn** ve **_RPTFn** makroları (CRTDBG içinde tanımlanır. Kullanımını değiştirin H) `printf` hata ayıklama için deyimleri.  
  
 [Öbek Atama İşlevleri Hata Ayıklama Sürümleri](../debugger/debug-versions-of-heap-allocation-functions.md)  
 Yığın ayırma işlevleri dahil olmak üzere, özel hata ayıklama sürümlerini açıklar: CRT çağrıları, açıkça çağırma avantajları nasıl eşlendiğini nasıl önleneceğini dönüştürme, istemci bloklar ayırmaları ayrı türlerini ve tanımlamayarak _ sonuçlarını izleme HATA AYIKLAMA.  
  
 [CRT Hata Ayıklama Öbeği Ayrıntıları](../debugger/crt-debug-heap-details.md)  
 Bellek yönetimi ve hata ayıklama yığın, blok türlerine bağlantılar kullanarak hata ayıklama öbek, öbek durumu raporlama işlevleri ve yığın ayırma isteklerini izleme hata ayıklama yığınında sağlar.  
  
 [Hata Ayıklama Kanca İşlevi Yazma](../debugger/debug-hook-function-writing.md)  
 İstemci engelleme listeleri bağlantılar, İşlevler, atama kanca işlevleri, atama kancaları ve CRT bellek ayırmaları ve kanca işlevlerini raporlama bağlayın.  
  
 [CRT Kitaplığını Kullanarak Bellek Sızıntılarını Bulma](../debugger/finding-memory-leaks-using-the-crt-library.md)  
 Algılama ve hata ayıklayıcı ve C çalışma zamanı kitaplığını kullanarak bellek sızıntılarını ayırma teknikleri kapsar.  
  
## <a name="related-sections"></a>İlgili Bölümler  
 [Yerel Kodda Hata Ayıklama](../debugger/debugging-native-code.md)  
 Bazı yaygın hata ayıklama sorunları ve C ve C++ uygulamaları için teknikleri açıklar.  
  
 [Hata Ayıklayıcısı Güvenliği](../debugger/debugger-security.md)  
 Daha güvenli hata ayıklama için öneriler sağlar.
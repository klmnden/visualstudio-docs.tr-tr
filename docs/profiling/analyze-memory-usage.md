---
title: Bellek kullanımını analiz etme
ms.custom: seodec18
ms.date: 01/02/2018
ms.topic: conceptual
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 4f06685be91926e4168c5e4592514469f94da47d
ms.sourcegitcommit: 2193323efc608118e0ce6f6b2ff532f158245d56
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/25/2019
ms.locfileid: "54932616"
---
# <a name="analyze-memory-usage"></a>Bellek kullanımını analiz etme
Hata ayıklayıcıyla tümleştirilmiş kullanın **bellek kullanımı** Tanılama aracını bellek sızıntılarını ve verimsiz bellek kullanımını bulun. Bir veya daha fazla atmanız bellek kullanımı aracı sağlar *anlık görüntüleri* yönetilen ve yerel bellek yığın. .NET, ASP.NET, yerel veya karma mod (.NET ve yerel) uygulamaları, anlık toplayabilirsiniz.  
  
-   Nesne türlerinin bellek kullanımı üzerindeki göreli etkisini anlamak ve uygulamanızda belleği verimsiz kullanan kodu bulmak için tek bir anlık görüntüyü anailz edebilirsiniz.  
  
-   Zaman içinde bellek kullanımı neden (fark) iki anlık görüntüsünü uygulama kodunuzda alanlar bulmak için de karşılaştırabilirsiniz.  

Ayrıntılı yönergeler için bkz. [bellek kullanımını analiz etme](../profiling/memory-usage.md) öğretici.  Şu anda .NET Core uygulaması için bellek kullanımını ölçmek için hata ayıklayıcısı ekli aracını kullanmanız gerekir. Diğer yönetilen ve yerel uygulamalar için veya bilginiz olmaksızın hata ayıklayıcısı ekli aracını kullanabilirsiniz.

Windows 7 ve daha sonra hata ayıklayıcı olmadan profil oluşturma araçları kullanabilirsiniz. Windows 8 ve üzeri, hata ayıklayıcısı ile profil oluşturma araçları çalıştırmak için gereklidir (**tanılama araçları** pencere).
  
## <a name="blogs-and-videos"></a>Bloglar ve videolar  

| | |
|---------|---------|
| ![video kamera simgesini film](../install/media/video-icon.png "bir video izleyin") | [Bir video izleyin](https://mva.microsoft.com/en-US/training-courses-embed/getting-started-with-visual-studio-2017-17798/Profiling-with-Diagnostics-Tools-in-Visual-Studio-2017-daHnzMD6D_9211787171) bellek kullanımı ve Visual Studio 2017'de CPU kullanımını analiz etme gösteren tanılama araçlarını kullanma. |

 [Hata ayıklama sırasında CPU ve bellek çözümleme](https://blogs.msdn.microsoft.com/visualstudio/2016/02/15/analyze-cpu-memory-while-debugging/)  
  
 [Visual C++ blogu: Visual C++ 2015'te bellek profili oluşturma](https://blogs.msdn.microsoft.com/vcblog/2015/10/21/memory-profiling-in-visual-c-2015/)  

## <a name="see-also"></a>Ayrıca bkz.
 [Visual Studio profil oluşturma](../profiling/index.md)  
 [Araçlar profil oluşturmaya ilk bakış](../profiling/profiling-feature-tour.md)
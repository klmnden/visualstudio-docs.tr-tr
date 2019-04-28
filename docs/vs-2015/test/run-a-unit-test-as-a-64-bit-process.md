---
title: Bir 64 bit işlem olarak birim testi çalıştırma | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-test
ms.topic: conceptual
helpviewer_keywords:
- unit tests, creating
- unit tests, running
ms.assetid: d23a9ee7-58e3-4e8b-a38c-b2207ea73fea
caps.latest.revision: 27
ms.author: gewarren
manager: jillfra
ms.openlocfilehash: 6b8dd75f7d293ee4e7dc412b2ff8f1983d936e3a
ms.sourcegitcommit: 47eeeeadd84c879636e9d48747b615de69384356
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "63446267"
---
# <a name="run-a-unit-test-as-a-64-bit-process"></a>64 bitlik bir işlem olarak birim testi çalıştırma
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Bir 64 bit makineniz varsa, birim testleri çalıştırma ve 64-bit işlem olarak kod kapsamı bilgileri yakalayın.  
  
## <a name="running-a-unit-test-as-a-64-bit-process"></a>Bir 64 bit işlem olarak birim testi çalıştırma  
  
#### <a name="to-run-a-unit-test-as-a-64-bit-process"></a>Bir 64 bit işlem olarak birim testi çalıştırmak için  
  
1. Kod veya testleri 32-bit/x86 derlendi ancak artık bunları 64 bit işlem olarak çalıştırmak istediğiniz, olarak yeniden derleyin **herhangi bir CPU**, ya da isteğe bağlı olarak **64-bit**.  
  
    > [!TIP]
    > Maksimum esneklik için test projelerinizi derlemelisiniz **herhangi bir CPU** yapılandırma. Ardından, 32 ve 64 bit aracıların çalıştırabilirsiniz. İle test projelerini derlemek için herhangi bir avantaj sağlamaz **64-bit** yapılandırma.  
  
2. Visual Studio menüsünden **Test**, ardından **ayarları**ve ardından **İşlemci mimarisi**. Seçin **x64** testleri 64 bit işlem olarak çalıştırılacak.  
  
     \- veya -  
  
     Belirtin `<TargetPlatform>x64</TargetPlatform>` .runsettings dosyasında. Bu yöntemin avantajı, farklı dosyalarında ayar gruplarını belirtin ve farklı ayarlar arasında hızlıca geçiş olmasıdır. Ayrıca, ayarları çözümleri arasında kopyalayabilirsiniz. Daha fazla bilgi için [bir .runsettings dosyasını kullanarak birim testlerini yapılandırma](../test/configure-unit-tests-by-using-a-dot-runsettings-file.md).  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Test Gezgini ile birim testleri çalıştırma](../test/run-unit-tests-with-test-explorer.md)   
 [Kodunuza birim testi](../test/unit-test-your-code.md)   
 [Visual Studio testleri için test ayarlarını belirtme](http://msdn.microsoft.com/library/0c15317e-80c6-4317-aed3-82b8e15e3901)

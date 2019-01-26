---
title: Visual Basic'de Durdur deyimleri | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
dev_langs:
- CSharp
- VB
- FSharp
- C++
helpviewer_keywords:
- End statements
- breakpoints, Stop statements
- debugging managed code, Stop statements vs breakpoints
- Stop statements, about Stop statements
- debugging [Visual Basic], Stop statements vs. breakpoints
ms.assetid: 4ad3fe5c-3dfb-4913-b2eb-a0b635751c18
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 3ea8f2b9fc9b6cc2694db94e156f1a182fb98e29
ms.sourcegitcommit: 2193323efc608118e0ce6f6b2ff532f158245d56
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/25/2019
ms.locfileid: "55011604"
---
# <a name="stop-statements-in-visual-basic"></a>Visual Basic'de Durdur Deyimleri
Visual Basic Stop deyimi, bir kesme noktası ayarlamak için programlı bir alternatif sunar. Hata ayıklayıcı Stop deyimi karşılaştığında (kesme moduna girer) programın yürütülmesini keser. C# programcıları System.Diagnostics.Debugger.Break yapılan bir çağrı kullanılarak aynı etkiyi elde edebilirsiniz.  
  
 Ayarlar veya kaynak kodu düzenleyerek bir Stop deyimi kaldırın. Ayarlayamıyor veya bir kesme noktası gibi hata ayıklayıcı komutlarını kullanarak Stop deyimleri temizleyin.  
  
 Bir End deyimi Stop deyimi değişkenleri sıfırlamak veya desteklemez, tasarım moduna dönmek. Uygulamayı çalıştırmaya devam etmek için hata ayıklama menüsünden devam seçebilirsiniz.  
  
 Stop deyimi, bir Visual Basic uygulama hata ayıklayıcının dışında çalıştırmak, Just-ın-Time, hata ayıklayıcı başlatılır, hata ayıklama etkin. Just-ın-Time, hata ayıklama etkin değil, Stop deyimi yürütmeyi sonlandırma bir End deyimi değilmiş gibi davranır. Visual Basic uygulamasında yayın sürümünden tüm Stop deyimleri kaldırmak için hiçbir QueryUnload ya da kaldırma olayı oluşur. Daha fazla bilgi için [tam zamanında hata ayıklama](../debugger/just-in-time-debugging-in-visual-studio.md).  
  
 Stop deyimleri kaldırmanın ihtiyacını önlemek için koşullu derleme kullanabilirsiniz:  
  
```cpp
#If DEBUG Then  
   Stop  
#Else  
   ' Don't stop  
#End If  
```  
  
 Başka bir alternatif bir onay deyimi yerine Stop deyimi kullanmaktır. Belirtilen koşul karşılanmamıştır ve bir yayım sürümünü derlediğinizde otomatik olarak kaldırılır Debug.Assert deyimi yürütmeyi keser. Daha fazla bilgi için [yönetilen koddaki onaylar](../debugger/assertions-in-managed-code.md). Hata ayıklama sürümü her zaman yürütmeyi keser bir onay deyimi istiyorsanız, bunu yapabilirsiniz:  
  
```csharp
Debug.Assert(false)  
```  
  
 Henüz başka bir alternatif Debug.Fail yöntemi kullanmaktır:  
  
```csharp
Debug.Fail("a clever output string goes here")  
```  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Hata ayıklayıcısı güvenliği](../debugger/debugger-security.md)   
 [C#, F#ve Visual Basic proje türleri](../debugger/debugging-preparation-csharp-f-hash-and-visual-basic-project-types.md)   
 [Yönetilen Kodda Hata Ayıklama](../debugger/debugging-managed-code.md)

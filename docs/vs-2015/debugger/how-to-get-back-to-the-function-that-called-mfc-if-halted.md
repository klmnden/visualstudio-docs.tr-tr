---
title: "Nasıl yapılır: Geri durdurulduysa MFC'yi çağıran işleve geri dönme | Microsoft Docs"
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-debug
ms.topic: conceptual
f1_keywords:
- vs.debug.mfc
dev_langs:
- FSharp
- VB
- CSharp
- C++
- C++
helpviewer_keywords:
- functions [C++], debugging
- function calls, returning to calling function
- debugging [MFC], returning to calling function
- debugging [MFC], functions
- Break command
- programs, halting
- functions [debugger]
ms.assetid: d254a5a9-afbd-4923-9d7a-7422d824cabf
caps.latest.revision: 21
author: MikeJo5000
ms.author: mikejo
manager: jillfra
ms.openlocfilehash: c19cbf6e892ba8b35f2b92ad9b86aa0b74a64810
ms.sourcegitcommit: 08fc78516f1107b83f46e2401888df4868bb1e40
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/15/2019
ms.locfileid: "65685877"
---
# <a name="how-to-get-back-to-the-function-that-called-mfc-if-halted"></a>Nasıl yapılır: Geri durdurulduysa MFC'yi çağıran işleve geri dönme
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

[NOT]
> Gördüğünüz iletişim kutuları ve menü komutları, etkin ayarlarınıza ve ürün sürümüne bağlı olarak Yardım menüsünde açıklanana göre farklılık gösterebilir. Ayarlarınızı değiştirmek için Araçlar menüsünden içeri ve dışarı aktarma ayarları seçin. Daha fazla bilgi için [Visual Studio'da geliştirme ayarlarını özelleştirme](https://msdn.microsoft.com/22c4debb-4e31-47a8-8f19-16f328d7dcd3).  
  
 Kullandıysanız **sonu** komutunu **hata ayıklama** programı durdurmak için menü MFC'de sonuçlandı ve sorunu kodunuzda olduğundan eminseniz işlevinize geri gitmek için çağrı yığını penceresini kullanabilirsiniz. Daha fazla bilgi için [nasıl yapılır: Çağrı yığını penceresini kullanma](../debugger/how-to-use-the-call-stack-window.md).  
  
 Bazen, kodunuzun içinde ileti pompası kesilebilir. Bu durumda, çağrı yığınındaki kullanıcı kodu yok. Bu sorunu önlemek için kesme noktaları (büyük olasılıkla ile koşullar ve isabet sayıları) yerine kullanabileceğiniz **sonu** komutu. Daha fazla bilgi için [kesme noktaları ve izleme noktaları](https://msdn.microsoft.com/fe4eedc1-71aa-4928-962f-0912c334d583)).  
  
### <a name="to-navigate-to-the-function-from-which-mfc-was-called"></a>MFC çağrıldı işleve gidin  
  
- Kullanım **çağrı yığını** penceresi.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Yerel kod hata ayıklaması SSS](../debugger/debugging-native-code-faqs.md)   
 [Yerel Kodda Hata Ayıklama](../debugger/debugging-native-code.md)

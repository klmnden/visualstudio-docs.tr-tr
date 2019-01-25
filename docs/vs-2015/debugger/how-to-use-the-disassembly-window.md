---
title: 'Nasıl yapılır: Ayrıştırılmış kod penceresini kullanma | Microsoft Docs'
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-debug
ms.topic: conceptual
f1_keywords:
- vs.debug.disassembly
dev_langs:
- FSharp
- VB
- CSharp
- C++
- JScript
- VB
- CSharp
- C++
helpviewer_keywords:
- assembly language, debugging inline assembly code
- breakpoints, Disassembly window
- Disassembly window
- machine code
ms.assetid: eaf84dd0-c82d-481b-af51-690b74e7794c
caps.latest.revision: 34
author: MikeJo5000
ms.author: mikejo
manager: jillfra
ms.openlocfilehash: 2bd0fe7ca8b2a1f21ebcb6c3434348df9d2e66e5
ms.sourcegitcommit: 8b538eea125241e9d6d8b7297b72a66faa9a4a47
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54803331"
---
# <a name="how-to-use-the-disassembly-window"></a>Nasıl yapılır: Ayrıştırılmış kod penceresini kullanma
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Bu özellik yalnızca adres seviyesinde hata ayıklamayı etkinse kullanılabilir **seçenekleri** iletişim kutusu, **hata ayıklama** düğümü. Betik veya SQL hata ayıklama için kullanılabilir değil.  
  
 **Ayrıştırılmış kodu** penceresi için derleyici tarafından oluşturulan talimatlara karşılık gelen derleme kodlarını gösterir. Yönetilen kod hata ayıklaması yapıyorsanız bu derleme yönergeleri, Visual Studio derleyici tarafından oluşturulan değil Microsoft Ara dilini (MSIL) Just-ın-Time (JIT) derleyici tarafından oluşturulan yerel koda karşılık gelir.  
  
 Derleme yönergeleri yanı sıra **ayrıştırılmış kodu** penceresi, aşağıdaki isteğe bağlı bilgileri gösterebilir:  
  
- Her yönerge bulunduğu bellek adresi. Yerel uygulamalar için bu gerçek bellek adresidir. Visual Basic, C# veya yönetilen kod için işlevin başlangıcına uzaklık var.  
  
- Bütünleştirilmiş kodu türetildiği kaynak kodu.  
  
- Kod bayt — bayt temsillerini gerçek makine ya da MSIL yönergeleri.  
  
- Sembol adları için bellek adresleri.  
  
- Kaynak koduna karşılık gelen satır numaraları.  
  
  Derleme dili talimatlarını yönerge adları ve değişkenler, kayıtlar ve sabitleri temsil eden simgeler kısaltmalar anımsatıcıları, oluşur. Her makine dil yönergesi, genellikle bir veya daha fazla değişkenleri, kayıtları veya sabitler ve ardından, bir derleme dili anımsatıcı temsil edilir.  
  
  Assembly dili okuyun ve ayrıştırma penceresi tam olarak yararlanmak istiyorsanız, derleme dili programlama hakkında iyi kitap başvurun. Assembly dili programlama ne biz Ayrıştırılmış kod penceresini kısa giriş bölümünde ele kapsamı dışındadır.  
  
  Bütünleştirilmiş kodu, yoğun işlemci kayıtları veya yönetilen kod kullandığından, ortak dil çalışma zamanı kaydeder, genellikle birlikte ayrıştırma penceresinde, kayıt incelemenize olanak tanır yazmaçlar penceresi ile kullanmak faydalı içeriği.  
  
  Büyük olasılıkla hiçbir zaman isteğine sahip veya kendi ham, sayısal bir form yerine derleme dili yönergeleri makine kodu görüntülemeniz gerekir. Ancak, bunu yapmak istiyorsanız, bu amaç için bellek penceresini kullanma veya kod bayt ayrıştırma penceresinde kısayol menüsünden seçin.  
  
> [!NOTE]
>  Gördüğünüz iletişim kutuları ve menü komutları, etkin ayarlarınıza ve ürün sürümüne bağlı olarak Yardım menüsünde açıklanana göre farklılık gösterebilir. Ayarlarınızı değiştirmek için seçin **içeri ve dışarı aktarma ayarları** üzerinde **Araçları** menüsü. Daha fazla bilgi için [Visual Studio'da geliştirme ayarlarını özelleştirme](http://msdn.microsoft.com/22c4debb-4e31-47a8-8f19-16f328d7dcd3).  
  
### <a name="to-display-the-disassembly-window"></a>Ayrıştırılmış kod penceresini görüntülemek için  
  
-   Üzerinde **hata ayıklama** menüsünde seçin **Windows**, tıklatıp **ayrıştırılmış kodu**.  
  
     Hata ayıklayıcı, çalışan veya kesme modunda olması gerekir.  
  
### <a name="to-turn-optional-information-on-or-off"></a>İsteğe bağlı bilgiler açmak veya kapatmak için  
  
-   Sağ **ayrıştırılmış kodu** penceresinde ayarlayın ve kısayol menüsünde istenen seçenekleri temizleyin.  
  
     Sol kenar boşluğundaki bir sarı ok geçerli yürütme noktasını konumu işaretler. Yerel kod için CPU'nun program sayacı bu karşılık gelir. Bu konum, programınızda yürütülecek sonraki yönergeyi gösterir.  
  
     Daha fazla bilgi için [sayfalama yukarı veya aşağı bellekte](../debugger/how-to-page-up-or-down-in-memory.md).  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Hata ayıklayıcıda verileri görüntüleme](../debugger/viewing-data-in-the-debugger.md)   
 [Nasıl yapılır: Yazmaçlar Penceresi Hakkında](../debugger/how-to-use-the-registers-window.md)

---
title: 'Nasıl Yapılır: Spy ++ başlangıç | Microsoft Docs'
ms.custom: ''
ms.date: 12/16/2018
ms.technology: vs-ide-debug
ms.topic: conceptual
helpviewer_keywords:
- Spy++, starting
ms.assetid: 1d36813a-dc2a-4fda-9b3d-a38928a62ced
author: mikejo5000
ms.author: mikejo
manager: douge
ms.workload:
- multiple
ms.openlocfilehash: 5143c34f0c344fecec82a5d08b2e7fb9b95ac1bc
ms.sourcegitcommit: a205ff1b389fba1803acd32c54df7feb0ef7a203
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 12/20/2018
ms.locfileid: "53646873"
---
# <a name="how-to-start-spy"></a>Nasıl Yapılır: Spy++'ı başlatma

Spy ++ Visual Studio'dan veya bir komut isteminde başlatabilirsiniz.  
  
 Başladığınızda Spy ++'ta, değişiklik bilgisayara select izni istemek için bir ileti görüntülenirse **Evet**.  
  
> [!NOTE]
>  Spy ++ yalnızca bir örneği çalıştırabilirsiniz. Yalnızca ikinci bir örneğini başlatmayı denerseniz, odağı almak o sırada çalıştırılan örneğinden neden olur.

## <a name="prerequisites"></a>Önkoşullar

Spy ++ aşağıdaki bileşenleri gerektirir. Seçerek bu bileşenlerin Visual Studio Yükleyicisi'nden seçebilirsiniz **tek tek bileşenler** sekmesini seçip ardından aşağıdaki bileşenleri.

* Hata ayıklama ve test altında seçin **C++ profil oluşturma araçları**
* Geliştirme etkinlikleri altında seçin **Visual Studio C++ temel özellikler**

Herhangi bir değişiklik yaptıysanız, bu bileşenleri yüklemek için istemleri izleyin.
  
## <a name="start-spy-from-visual-studio"></a>Spy ++ Visual Studio'dan Başlat
  
Üzerinde **Araçları** menüsünde **Spy ++**.  
  
Başladıktan sonra Spy ++ birbirinden bağımsız olarak çalıştığından, Visual Studio'yu kapatabilirsiniz.  
  
> [!NOTE]
>  İletileri Spy ++ ile oturum açışınızda, işletim sisteminin daha yavaş çalışmasına neden olabilir.  
  
## <a name="start-spy-at-a-command-prompt"></a>Spy ++ bir komut isteminden başlatmak  
  
1.  Bir komut istemi penceresinde dizinleri spyxx.exe içeren klasöre değiştirin. Genellikle, bu klasörün yolu... \\ *Visual Studio yükleme klasörü*\Common7\Tools\\.  
  
2.  Girin **spyxx.exe**. 
  
## <a name="see-also"></a>Ayrıca bkz.  
 [Spy ++ kullanma](../debugger/using-spy-increment.md)   
 [Spy ++ görünümleri](../debugger/spy-increment-views.md)   
 [Spy++ Başvurusu](../debugger/spy-increment-reference.md)
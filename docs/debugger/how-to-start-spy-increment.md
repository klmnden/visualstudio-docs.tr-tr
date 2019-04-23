---
title: 'Nasıl yapılır: Spy ++ başlangıç | Microsoft Docs'
ms.date: 12/16/2018
ms.topic: conceptual
helpviewer_keywords:
- Spy++, starting
ms.assetid: 1d36813a-dc2a-4fda-9b3d-a38928a62ced
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 85e253491a4cb3713b5920c9abd09f9396298319
ms.sourcegitcommit: 1fc6ee928733e61a1f42782f832ead9f7946d00c
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/22/2019
ms.locfileid: "60099149"
---
# <a name="how-to-start-spy"></a>Nasıl yapılır: Spy++'ı başlatma

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

1. Bir komut istemi penceresinde dizinleri spyxx.exe içeren klasöre değiştirin. Genellikle, bu klasörün yolu... \\ *Visual Studio yükleme klasörü*\Common7\Tools\\.

2. Enter **spyxx.exe**.

## <a name="see-also"></a>Ayrıca bkz.
- [Spy++ kullanma](../debugger/using-spy-increment.md)
- [Spy++ Görünümleri](../debugger/spy-increment-views.md)
- [Spy++ Başvurusu](../debugger/spy-increment-reference.md)
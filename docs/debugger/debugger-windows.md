---
title: Hata ayıklayıcı penceresini kullanarak verileri İnceleme | Microsoft Docs
ms.custom: seodec18
ms.date: 04/25/2018
ms.topic: conceptual
ms.assetid: 4c6fe8f1-b015-4989-bb31-72ebac390026
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: e14f1864452edd00237164e14af74330e3c209f7
ms.sourcegitcommit: 91c7f1b525e0c22d938bc4080ba4ceac2483474f
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/12/2019
ms.locfileid: "67033009"
---
# <a name="inspect-data-using-debugger-windows-in-visual-studio"></a>Visual Studio hata ayıklayıcı pencerelerinde kullanarak verileri İnceleme

Programınızın hata ayıklama sırasında çoğu hata ayıklayıcı penceresini açabilirsiniz. Hata ayıklayıcı pencereleri listesini görmek için bir kesme noktası ayarlayın ve hata ayıklamaya başlayın. Kesme noktası ve yürütme durakları ulaştığınızda tıklayın **hata ayıklama > Windows**.

||||
|-|-|-|
|**Pencere**|**Kısayol tuşu**|**Konusuna bakın**|
|Kesme noktaları|CTRL+ALT+B|[Kesme noktaları kullanma](../debugger/using-breakpoints.md)|
|Özel durum ayarları|CTRL + ALT + E|[Özel durumları hata ayıklayıcısı ile yönetme](../debugger/managing-exceptions-with-the-debugger.md)|
|Çıkış|CTRL + ALT + O|[Çıktı Penceresi](../ide/reference/output-window.md)|
|İzleme|CTRL + ALT + W, (1, 2, 3, 4)|[İzleme ve Hızlı İzleme Pencereleri](../debugger/watch-and-quickwatch-windows.md)|
|QuickWatch|SHIFT + F9|[İzleme ve Hızlı İzleme Pencereleri](../debugger/watch-and-quickwatch-windows.md)|
|İfade ve değişkenler|CTRL+ALT+V, A|[Otomatikler ve Yereller Pencereleri](../debugger/autos-and-locals-windows.md)|
|Yerel öğeler|CTRL+ALT+V, L|[Otomatikler ve Yereller Pencereleri](../debugger/autos-and-locals-windows.md)|
|Çağrı yığınları|CTRL+ALT+C|[Nasıl yapılır: Çağrı Yığını Penceresini Kullanma](../debugger/how-to-use-the-call-stack-window.md)|
|Hemen|CTRL+ALT+I|[Komut Penceresi](../ide/reference/immediate-window.md)|
|Paralel Yığınlar|CTRL: + SHIFT + D, S|[Paralel Yığınlar Penceresini Kullanma](../debugger/using-the-parallel-stacks-window.md)|
|Paralel izleme|CTRL: + SHIFT + D, (1, 2, 3, 4)|[Alma çok iş parçacıklı uygulamalarda hata ayıklama başlatıldı](../debugger/get-started-debugging-multithreaded-apps.md)|
|İş Parçacıkları|CTRL + ALT + H|[İş parçacıkları penceresini kullanarak hata ayıklama](../debugger/how-to-use-the-threads-window.md)|
|Modüller|CTRL+ALT+U|[Nasıl yapılır: Modüller Penceresini Kullanma](../debugger/how-to-use-the-modules-window.md)|
|GPU iş parçacıkları|-|[Nasıl yapılır: GPU İş Parçacıkları Penceresini Kullanma](../debugger/how-to-use-the-gpu-threads-window.md)|
|Görevler|CTR:+SHIFT+D, K|[Görevleri Penceresini Kullanma](../debugger/using-the-tasks-window.md)|
|Python etkileşimli hata ayıklama|SHIFT+ALT+I|[Python etkileşimli REPL](../python/python-interactive-repl-in-visual-studio.md)|
|JavaScript Konsolu|CTRL+ALT+V, C|[Hızlı Başlangıç: JavaScript hatalarını ayıklama](../debugger/quickstart-debug-javascript-using-the-console.md)|
|DOM Gezgini|CTRL+ALT+V, D|[DOM Gezgini'ni kullanarak düzen hatalarını ayıklama](/visualstudio/debugger/quickstart-debug-html-and-css)|
|Canlı görsel ağaç|-|[Hata ayıklama sırasında XAML özelliklerini denetleme](../debugger/inspect-xaml-properties-while-debugging.md)|
|Canlı özellik Gezgini|-|[Hata ayıklama sırasında XAML özelliklerini denetleme](../debugger/inspect-xaml-properties-while-debugging.md)|
|İşlemler|CTRL+ALT+Z|[İş Parçacıklarında ve İşlemlerde Hata Ayıklama](../debugger/debug-threads-and-processes.md)|
|Bellek|CTRL + ALT + M, (1, 2, 3, 4)|[Bellek Pencereleri](../debugger/memory-windows.md)|
|Ayrıştırılmış kodu|CTRL + ALT + D|[Nasıl yapılır: Ayrıştırılmış Kod Penceresini Kullanma](../debugger/how-to-use-the-disassembly-window.md)|
|Kaydeder|CTRL+ALT+G|[Nasıl yapılır: Yazmaçlar Penceresi Hakkında](../debugger/how-to-use-the-registers-window.md)|

## <a name="see-also"></a>Ayrıca Bkz.

[Hata ayıklayıcıya ilk bakış](../debugger/debugger-feature-tour.md)
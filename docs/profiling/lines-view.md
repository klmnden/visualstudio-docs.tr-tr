---
title: Satırlar görünümü | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
f1_keywords:
- vs.performance.view.lines
helpviewer_keywords:
- profiling tools reports, Line view
- profiling tools, Line view
- Lines view
ms.assetid: 71ec0781-6031-4e17-af09-f50226018437
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 905979e0bc563e7525f1385a484e9b44b523a1f9
ms.sourcegitcommit: d0425b6b7d4b99e17ca6ac0671282bc718f80910
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/21/2019
ms.locfileid: "56613992"
---
# <a name="lines-view"></a>Satırlar Görünümü
Satırlar görünümü, toplanan örnekleme yöntemini kullanarak profil oluşturucu verileri için kullanılabilir. Görünüm araçları kullanılarak toplanan veriler için kullanılabilir değil.

 Satırlar görünümü, profil verileri örnekleme için örnek toplanan doğrudan yürütülmekte olan bir işlev bildiriminde tanımlar. .NET bellek verileri için bellek tahsis deyimleri satırlar görünümü tanımlar.

 Bir kaynak dosyasında bir deyimi kaynak dosyasında bir satırdan daha kapsayabilir ve tek bir satır birden fazla deyim içerebilir.

 Bir deyimi aşağıdaki tarafından tanımlanır:

-   Function deyimi içeren kaynak dosyası.

-   Deyimi içeren işlev.

-   Deyim başladığı kaynak satırı.

-   Deyim başladığı kaynak satırı karakter.

-   Kaynak satırı başlangıçtan deyimini sonlandırır.

-   Deyim erdiği kaynak satırı karakter.

## <a name="see-also"></a>Ayrıca bkz.
- [Satırlar Görünümü](../profiling/lines-view-sampling-data.md)
- [Satırlar görünümü - örnekleme](../profiling/lines-view-dotnet-memory-sampling-data.md)
- [Satırlar Görünümü](../profiling/lines-view-contention-data.md)
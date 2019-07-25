---
title: PerfView ile ETL izlemesi toplama
ms.date: 06/27/2019
ms.topic: conceptual
helpviewer_keywords:
- perfview
- ETL Trace
author: mikeblome
ms.author: mblome
manager: jillfra
dev_langs:
- CSharp
- VB
- CPP
ms.workload:
- multiple
ms.description: Use perfview.exe to collect ETL traces for troubleshooting issues with Visual Studio
ms.openlocfilehash: 6b1f61888fa642ed544c6da7d1cf77c43b52b2d9
ms.sourcegitcommit: 85d66dc9fea3fa49018263064876b15aeb6f9584
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/24/2019
ms.locfileid: "68461547"
---
# <a name="collect-an-etl-trace-with-perfview"></a>PerfView ile ETL izlemesi toplama

PerfView, Visual Studio ile ilgili bazı sorunların giderilmesi için yararlı olabilecek, [Windows Için olay izleme](/windows/desktop/ETW/event-tracing-portal) 'ye dayalı ETL (olay izleme günlüğü) dosyaları oluşturan bir araçtır. Bazen bir sorun rapor ettiğinizde, ürün ekibi ek bilgi toplamak için PerfView çalıştırmanızı isteyebilir.

## <a name="install-perfview"></a>PerfView 'ı yükler

PerfView 'ı [Microsoft Indirme merkezi](http://www.microsoft.com/download/details.aspx?id=28567)' nden indirin.

## <a name="run-perfview"></a>PerfView çalıştırma

1. Windows Gezgini 'nde **PerfView. exe** ' ye sağ tıklayın ve **yönetici olarak çalıştır** ' ı seçin.
1. Topla menüsünde **topla** ' yı seçin.
1. **Zip**, **birleştirme**ve **threadtime**'ı denetleyin.
1. **DAIRESEL MB** ile 1000 arasında bir artış yapın.
1. Birden çok kez toplanmanız durumunda ETL izlemelerini belirtilen bir klasöre ve veri dosyasına kaydetmek için **geçerli dizini** değiştirin.
1. Veri kaydetmeye başlamak için **koleksiyonu Başlat** düğmesini seçin.
1. Verileri kaydetmeyi durdurmak için **koleksiyonu durdur** düğmesini seçin. Tercih görünümü. etl. zip dosyası belirtilen dizine kaydedilecek.

PerfView yalnızca kendi arabelleğine sığan en son verileri saklayabilir. Bu nedenle, Visual Studio Donmadan veya yavaşlamaya başladıktan sonra toplamayı en kısa sürede durdurmayı deneyin. Bir sorunla karşılaşmadan 30 saniyeden uzun süre toplanmayın.

Daha fazla bilgi için bkz. [Channel9 üzerinde PerfView öğreticisi](http://channel9.msdn.com/Series/PerfView-Tutorial/PerfView-Tutorial-1-Collecting-data-with-the-Run-command).

---
title: Bir ETL izleme PerfView ile Topla
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
ms.openlocfilehash: baae89b7bf45a4848c571f75e37c6cc0d203d459
ms.sourcegitcommit: 6f7a740750b2cd17ea2275c3d046caebc9782917
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/02/2019
ms.locfileid: "67518237"
---
# <a name="collect-an-etl-trace-with-perfview"></a>Bir ETL izleme PerfView ile Topla

PerfView göre ETL (olay izleme günlüğü) dosyaları oluşturan bir araçtır [olay izleme için Windows](/windows/desktop/ETW/event-tracing-portal) , bazı tür kapalı Visual Studio ile ilgili sorunları gidermeye yararlı olabilir. Bazen ne zaman sorun bildir, ürün ekibi, ek bilgi toplamak için PerfView çalıştırmanızı isteyebilir.

## <a name="install-perfview"></a>PerfView yükleyin

PerfView'nden indirin [Microsoft İndirme Merkezi](http://www.microsoft.com/download/details.aspx?id=28567).

## <a name="run-perfview"></a>PerfView çalıştırın

1. Sağ **PerfView.exe** Windows Gezgini'nde seçin **yönetici olarak çalıştır** Yöneticisi
1. Toplama menüsünde **Topla**
1. Denetleme **Zip**, **birleştirme**, ve **İşParçacığıSüresi**.
1. Artırmak **döngüsel MB** 1000.
1. Değişiklik **geçerli dizini** birden çok kez toplamak için kullanacaksanız, belirtilen klasör ve veri dosyası için ETL izlemeleri kaydetmek için.
1. Veri kaydını başlatmak için **toplamaya Başla** düğmesi.
1. Veri kaydı durdurmak için seçin **toplamasını Durdur** düğmesi. Belirtilen dizindeki PrefView.etl.zip dosyası kaydedilir.

PerfView kendi arabelleğe uygun en son veriyi depolayabilirsiniz. Bu nedenle, Visual Studio dondurma veya yavaşlamasına başladıktan sonra toplama olabildiğince çabuk durdurmayı deneyin. Bir sorun isabet sonra birden fazla 30 saniye için toplamayın.

Daha fazla bilgi için [channel9 Öğreticisi PerfView](http://channel9.msdn.com/Series/PerfView-Tutorial/PerfView-Tutorial-1-Collecting-data-with-the-Run-command).

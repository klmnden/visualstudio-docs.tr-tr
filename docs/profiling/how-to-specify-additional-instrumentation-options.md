---
title: 'Nasıl yapılır: Ek izleme seçeneklerini belirtme | Microsoft Docs'
ms.date: 11/04/2016
ms.topic: conceptual
f1_keywords:
- vs.performance.property.advanced
helpviewer_keywords:
- instrumentation, options
- profiling tools, session options
- performance sessions, options
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: c95add435824663e798d226e0be11ddbe06b8aba
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62539146"
---
# <a name="how-to-specify-additional-instrumentation-options"></a>Nasıl yapılır: Ek izleme seçeneklerini belirtme

İkili dosyaları Visual Studio IDE kullanarak veya komut satırı araçlarını kullanarak izleyebilirsiniz. IDE içinde bir ikili izleme, ek izleme seçeneklerini belirterek izleme sırasında toplanan verilerin hacmini denetleyebilirsiniz [Vsınstr](../profiling/vsinstr.md) aracı. Bu seçenekler, oturum veya hedef düzeyinde kullanılabilir. Örneğin, dahil etmek veya izleme işlemi sırasında belirli işlevleri hariç tutmak için hedef düzeyinde ek izleme seçeneği kullanın.

> [!IMPORTANT]
> Eklenen her araştırma biraz özgün programın davranışını değiştirir. Bu değişikliği yükü analiz zamanında neden olur. Bu ek yükü yaklaşık çıkarılır olsa da, yine de çok iş parçacıklı uygulamalar üzerinde ince zamanlama etkileri vardır. [Vsınstr](../profiling/vsinstr.md) aracı profil oluşturma sırasında seçenekleri Yardım denetim veri koleksiyonu.

## <a name="to-specify-additional-instrumentation-option"></a>Ek izleme seçeneği belirlemek için

1. İçinde **performans Gezgini**seçin **performans oturumu** ve ardından sağ tıklayıp **özellikleri**.

2. İçinde **özellikler sayfaları**, tıklayın **Gelişmiş** özellikleri.

3. Tür seçenekleri **ek izleme seçeneklerini** kutusu.

     Örneğin, /CONTROL:THREAD profil oluşturma düzeyini belirtmek için kullanın. Seçeneklerinin tam listesi için bkz: [Vsınstr](../profiling/vsinstr.md).

4. **Tamam**'ı tıklatın.

## <a name="see-also"></a>Ayrıca bkz.

[Performans oturumlarını yapılandırma](../profiling/configuring-performance-sessions.md)
[komut satırından profil](../profiling/using-the-profiling-tools-from-the-command-line.md)
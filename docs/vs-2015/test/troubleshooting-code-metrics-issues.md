---
title: Kod ölçümleri sorunlarını giderme | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-test
ms.topic: troubleshooting
ms.assetid: f2fdb995-4888-4246-85dc-7bacadd45968
caps.latest.revision: 6
author: gewarren
ms.author: gewarren
manager: jillfra
ms.openlocfilehash: 5a02dbc4840729d5004b0815175f626fc8760711
ms.sourcegitcommit: 59e5758036223ee866f3de5e3c0ab2b6dbae97b6
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/23/2019
ms.locfileid: "68416971"
---
# <a name="troubleshooting-code-metrics-issues"></a>Kod Ölçümleri Sorunlarını Giderme
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Kod ölçümleri topladığınızda aşağıdaki sorunlardan bazılarını yaşayabilirsiniz:

- [Visual Studio 2010 kod karmaşıklığı hesaplamalarında yapılan değişiklikler](#Changes_in_Visual_Studio_2010_code_complexity_calculations)

## <a name="Changes_in_Visual_Studio_2010_code_complexity_calculations"></a>Visual Studio 2010 kod karmaşıklığı hesaplamalarında yapılan değişiklikler

Aynı işlev için, içinde [!INCLUDE[vs_dev10_long](../includes/vs-dev10-long-md.md)] hesaplanan kod karmaşıklığı ölçümü aşağıdaki durumlar [!INCLUDE[vs_current_short](../includes/vs-current-short-md.md)] için önceki sürümleri tarafından hesaplanan ölçüden farklı olabilir:

- İşlev bir veya daha fazla catch bloğu içeriyor. Önceki sürümlerinde [!INCLUDE[vs_current_short](../includes/vs-current-short-md.md)], catch blokları hesaplamaya eklenmedi. ' [!INCLUDE[vs_dev10_long](../includes/vs-dev10-long-md.md)]De, her bir catch bloğunun karmaşıklığı işlevin karmaşıklığına eklenir.

- İşlev, bir anahtar (VB 'de Case, Select Case) ifadesini içerir. Ve önceki sürümler [!INCLUDE[vs_dev10_long](../includes/vs-dev10-long-md.md)] arasındaki derleyici farklılıkları, daha fazla dönüş durumu içeren bazı Switch deyimleri için farklı MSIL kodu oluşturabilir.

## <a name="see-also"></a>Ayrıca bkz.

- [Yönetilen Kodun Ölçüm Karmaşıklığı ve Bakımı](../code-quality/measuring-complexity-and-maintainability-of-managed-code.md)

---
title: Visual Studio yavaşsa performansı
titleSuffix: ''
ms.date: 04/11/2018
ms.topic: conceptual
helpviewer_keywords:
- performance [Visual Studio]
author: gewarren
ms.author: gewarren
manager: jillfra
f1_keywords:
- vs.performancecenter
ms.workload:
- multiple
ms.openlocfilehash: bdc605b614fab5b11c2efc8466480ebf49a1fee7
ms.sourcegitcommit: 53aa5a413717a1b62ca56a5983b6a50f7f0663b3
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/17/2019
ms.locfileid: "59648030"
---
# <a name="optimize-visual-studio-performance"></a>Visual Studio performansını iyileştirme

Bu makalede, Visual Studio'nun yavaş çalıştığından bulursanız denemek için bazı öneriler sağlar. Ayrıca bir göz atabilirsiniz [Visual Studio performans ipuçları ve püf noktaları](../ide/visual-studio-performance-tips-and-tricks.md) performansı konusunda daha fazla öneri için.

## <a name="upgrade-visual-studio"></a>Visual Studio yükseltme

Visual Studio 2015 kullanıyorsanız, indirme [Visual Studio 2017](https://visualstudio.microsoft.com/vs/older-downloads/?utm_medium=microsoft&utm_source=docs.microsoft.com&utm_campaign=vs+2017+download) veya [Visual Studio 2019](https://visualstudio.microsoft.com/downloads/?utm_medium=microsoft&utm_source=docs.microsoft.com&utm_campaign=inline+link&utm_content=download+vs2019) ücretsiz geliştirilmiş performansını denetlemek için. Çözümler iki Visual Studio 2015'te daha hızlı bir şekilde diğer alanlarda performans geliştirmeleri ile üç kez çok yükleyin. Herhangi bir şey tarafından denediğiniz kaybetmemesi için visual Studio 2017 ve Visual Studio 2019 yan yana Visual Studio 2015 ile uyumludur.

::: moniker range="vs-2017"

Visual Studio 2017 zaten kullanıyorsanız, 15.6 veya sonraki sürümü çalıştırdığından emin olun. Veri çözümleri için iki veya üç kez sürüm 15.6 daha hızlı yükleneceğiyle olduğunu gösterir. İndirdiği [burada](https://visualstudio.microsoft.com/vs/older-downloads/?utm_medium=microsoft&utm_source=docs.microsoft.com&utm_campaign=vs+2017+download).

::: moniker-end

## <a name="extensions-and-tool-windows"></a>Uzantılar ve araç pencereleri

Visual Studio yavaşlamasıdır yüklü uzantılar olabilir. Performansı artırmak için uzantıları yönetme hakkında daha fazla yardım için bkz: [performansını artırmak için uzantı ayarları değiştir](../ide/optimize-visual-studio-startup-time.md#extensions).

Benzer şekilde, Visual Studio yavaşlamasıdır araç pencereleri olabilir. Araç pencereleri yönetme hakkında daha fazla yardım için bkz: [performansını artırmak için araç penceresi ayarlarını değiştir](../ide/optimize-visual-studio-startup-time.md#tool-windows).

## <a name="hardware"></a>Donanım

Donanım yükseltme hakkında düşünüyorsanız, ek RAM veya daha hızlı bir CPU performans üzerindeki etkisini daha fazla katı hal sürücüsü (SSD) sahiptir.

Bir SSD eklerseniz, en iyi performans için bir sabit disk sürücüsü (HDD) aksine bu sürücüyü Windows yükleyin. Visual Studio çözümünüzü sürücü konumunu kadar önemli görünmüyor.

Ayrıca, çözümünüze bir USB sürücüsünden çalıştırmayın. HDD veya SSD kopyalayın.

## <a name="help-us-improve"></a>Geliştirmemize yardımcı olun

Geri bildiriminiz geliştirmemize yardımcı olur. Kullanım **sorun bildir** özelliğini "kaydı bir izleme" ve bize gönderin. Geri bildirim simgesini seçin **hızlı başlatma**, ya da seçin **yardımcı** > **geri bildirim gönder** > **sorunbildir** menü çubuğundan. Daha fazla bilgi için [Visual Studio ile ilgili bir sorun bildirme](../ide/how-to-report-a-problem-with-visual-studio.md).

## <a name="see-also"></a>Ayrıca bkz.

- [Performans İpuçları ve püf noktaları](../ide/visual-studio-performance-tips-and-tricks.md)
- [Visual Studio blogu - Visual Studio 2017 sürüm 15.6 ile daha hızlı yük çözümleri](https://devblogs.microsoft.com/visualstudio/load-solutions-faster-with-visual-studio-2017-version-15-6/)
---
title: Başlatma süresi geliştirin
ms.date: 11/15/2017
ms.topic: conceptual
helpviewer_keywords:
- startup time [Visual Studio]
- optimizing performance [Visual Studio]
- speed up start time [Visual Studio]
ms.assetid: d1508121-8499-4084-8eb5-fa89fa7b17d3
author: gewarren
ms.author: gewarren
manager: jillfra
f1_keywords:
- vs.performancecenter
ms.workload:
- multiple
ms.openlocfilehash: 60302646abbf36034756f38183d7be7f0d28c1ca
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62812527"
---
# <a name="optimize-visual-studio-startup-time"></a>Visual Studio Başlangıç süresini iyileştirme

Visual Studio, olabildiğince çabuk ve mümkün olduğunca verimli bir şekilde başlamak için tasarlanmıştır. Ancak, bazı Visual Studio uzantıları ve araç pencerelerini yüklü olduğunda başlangıç zamanını olumsuz etkileyebilir. Yavaş uzantıları davranışını denetleyen ve aracı windows **Visual Studio performansını Yönet** iletişim kutusu. Performansı artırma ile ilgili daha fazla genel ipuçları için bkz: [Visual Studio performans ipuçları ve püf noktaları](../ide/visual-studio-performance-tips-and-tricks.md).

## <a name="startup-behavior"></a>Başlangıç davranışı

Başlangıç zamanı genişletme önlemek için Visual Studio uzantılarını kullanarak yükleyen bir _isteğe bağlı_ yaklaşım. Bu davranış uzantıları hemen sonra Visual Studio başlatılır, ancak gerektiğinde olarak açmayın anlamına gelir. Ayrıca, önceki bir Visual Studio oturumu açık sol araç pencereleri başlangıç zamanını yavaşlatabileceği için Visual Studio Başlangıç süresini etkileyen önlemek için daha akıllı bir şekilde araç pencereleri açılır.

Visual Studio yavaş başlatma algılarsa, yavaşlama neden olan uzantı veya araç penceresinin için uyarı bir açılır ileti görüntülenir. İleti bir sayfaya bağlantı verilmektedir **Visual Studio performansını Yönet** iletişim kutusu. Bu iletişim kutusunu seçerek de erişebilirsiniz **yardımcı** > **Visual Studio performansını Yönet** menü çubuğundan.

![Açılan okuma - Visual Studio performansını Yönet ' uzantısının... ettik Visual Studio'yu yavaşlatıyor '](../ide/media/vside_perfdialog_popup.png)

İletişim kutusunun başlangıç performansı etkileyen uzantıları ve araçları windows listeler. Başlangıç performansı artırmak için uzantı ve araç penceresi ayarlarını değiştirebilirsiniz.

## <a name="a-nameextensions-to-change-extension-settings-to-improve-startup-solution-load-and-typing-performance"></a><a name="extensions" />Başlangıç, çözüm yükü ve performans yazarak geliştirmek için uzantı ayarları değiştirmek için

1. Açık **Visual Studio performansını Yönet** iletişim kutusunu **yardımcı** > **Visual Studio performansını Yönet** menü çubuğundan.

    Bir uzantı yüklenirken, çözümü Visual Studio Başlangıç yavaşlatıyor veya yazarak, görünen uzantıyı **Visual Studio performansını Yönet** iletişim kutusunun altında **uzantıları**  >   **Başlangıç** (veya **çözüm yükü** veya **yazarak**).

    ![Visual Studio performansını - uzantıları görünümü yönetme](../ide/media/vside_perfdialog_extensions.png)

2. Devre dışı bırakın ve ardından istediğiniz uzantıyı seçin **devre dışı** düğmesi.

Her zaman uzantı için gelecekteki oturumları kullanarak yeniden etkinleştirebilirsiniz **Uzantı Yöneticisi** veya **Visual Studio performansını Yönet** iletişim kutusu.

## <a name="a-nametool-windows-to-change-tool-window-settings-to-improve-startup-time"></a><a name="tool-windows" />Başlangıç süresini kısaltmak için araç penceresi ayarlarını değiştirmek için

1. Açık **Visual Studio performansını Yönet** iletişim kutusunu **yardımcı** > **Visual Studio performansını Yönet** menü çubuğundan.

    Araç penceresi Visual Studio Başlangıç yavaşlatıyor araç penceresi görünür **Visual Studio performansını Yönet** iletişim kutusunun altında **aracı Windows** > **başlatma**.

2. Davranışını değiştirmek istediğiniz araç penceresi seçin.

3. Aşağıdaki üç seçenekten birini seçin:

   - **Varsayılan davranışı kullanın:** Araç penceresi için varsayılan davranış. Bu seçenek tutma başlangıç performansı artırmak değildir.

   - **Başlangıçta pencere gösterme:** Visual Studio'da açtığınızda önceki bir oturum açma sol olsa bile her zaman belirtilen araç penceresi kapatılır. İhtiyacınız olduğunda, araç penceresi uygun menüsünden açabilirsiniz.

   - **Başlangıçta pencereyi otomatik gizle:** Araç penceresini önceki bir oturumda açık bırakıldı, başlangıçta aracını pencerenin grubu araç penceresi başlatma önlemek için bu seçeneği daraltır. Araç penceresi genellikle kullanıyorsanız bu seçeneği iyi bir seçimdir. Araç penceresi hala kullanılabilir ancak Visual Studio Başlangıç süresini artık olumsuz etkiler.

     ![Visual Studio performansını Yönet - araç pencerelerini görüntüleyin](../ide/media/vside_perfdialog_toolwindows.png)

> [!NOTE]
> Visual Studio 2017'in önceki bazı sürümlerinde denilen bir özelliği olan **basit çözüm yükü**. Geçerli sürümlerinde kodu yükleme önceden kıyasla çok daha hızlı, basit çözüm yükü olmadan bile içeren büyük çözümler yönetilen.

## <a name="see-also"></a>Ayrıca bkz.

- [Visual Studio performansını iyileştirme](../ide/optimize-visual-studio-performance.md)
- [Visual Studio performans ipuçları ve püf noktaları](../ide/visual-studio-performance-tips-and-tricks.md)
- [Visual Studio blogu - Visual Studio 2017 sürüm 15.6 ile daha hızlı yük çözümleri](https://devblogs.microsoft.com/visualstudio/load-solutions-faster-with-visual-studio-2017-version-15-6/)
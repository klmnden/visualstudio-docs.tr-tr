---
title: Hızlı Eylemler, ampuller ve tornavidalar
ms.date: 03/28/2018
ms.topic: conceptual
author: gewarren
ms.author: gewarren
manager: jillfra
dev_langs:
- CSharp
- VB
ms.workload:
- multiple
ms.openlocfilehash: 1a08e54025ac0826b88a3d3fcee299beef245d13
ms.sourcegitcommit: f7c401a376ce410336846835332a693e6159c551
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/14/2019
ms.locfileid: "57867043"
---
# <a name="quick-actions"></a>Hızlı Eylemler

Hızlı Eylemler, kolayca yeniden düzenleme sağlar, oluşturmak veya aksi halde kodu tek eylemle değiştirin. Hızlı eylemler için kullanılabilir C#, [C++](/cpp/ide/writing-and-refactoring-code-cpp)ve Visual Basic kod dosyalarında. Bazı eylemler bir dile özgü olan ve diğer tüm diller için geçerlidir.

Hızlı eylemler için kullanılabilir:

- Bir kod düzeltmesini uygulayın bir [Çözümleyicisi kod](../code-quality/roslyn-analyzers-overview.md) kuralı ihlali

- [Bastır](../code-quality/use-roslyn-analyzers.md#suppress-violations) kod Çözümleyicisi Kuralı ihlali

- Geçerli bir yeniden düzenleme (örneğin, [satır içi geçici değişken](../ide/reference/inline-temporary-variable.md))

- Kod oluşturma (örneğin, [bir yerel değişken ekleme](../ide/reference/introduce-local-variable.md))

> [!NOTE]
> Bu konu, Windows üzerinde Visual Studio için geçerlidir. Mac için Visual Studio için bkz: [yeniden düzenleme (Mac için Visual Studio)](/visualstudio/mac/refactoring).

Ampul kullanarak hızlı Eylemler uygulanabilir ![ampul](media/light-bulb-icon.png) veya tornavida ![tornavida simgesi](media/screwdriver-icon.png) simgeleri veya basarak **Ctrl** + **.** imlecinizi bir eylem kullanılabilir kod satırına olduğunda. Gördüğünüz hata ampul ![hata ampul simgesini](media/error-light-bulb-icon.png) hata belirten bir kırmızı dalgalı çizgi yoktur ve Visual Studio, bu hata için bir düzeltme sahiptir.

Herhangi bir dilde üçüncü taraflara özel tanılama ve öneriler, örneğin bir SDK'ın bir parçası olarak sağlayabilir ve Visual Studio ampuller bu kurallara göre görünür.

## <a name="icons"></a>Simgeler

Hızlı eylem kullanılabilir olduğunda görüntülenen simge, kullanılabilir düzeltme veya yeniden düzenleme tür gittiğinin belirtisini verir. *Tornavida* ![tornavida simgesi](media/screwdriver-icon.png) simgesi gösterir yalnızca kodunu değiştirmek kullanılabilir eylemleri vardır, ancak bunları mutlaka kullanmamalısınız. *Sarı bir ampul* ![ampul](media/light-bulb-icon.png) simgesi gösterir kullanılabilir eylemler, *gereken* kodunuzu geliştirmek için yapın. *Hata ampul* ![hata ampul simgesini](media/error-light-bulb-icon.png) simgesi gösterir, kodunuzdaki bir hatayı düzeltir bir eylem yoktur.

## <a name="to-see-a-light-bulb-or-screwdriver"></a>Ampul veya tornavida görmek için

Bir düzeltme kullanılabilir haldeyse, ampuller görünür:

- Bir hatanın konumda fare geldiğinizde

   ![Ampul fare vurgulama ile](../ide/media/vs2015_lightbulb_hover.png)

- Giriş işaretini (imleç) ilgili kod satırının içine taşıdığınızda düzenleyicinin sol kenar boşluğunda

Ayrıca basabilirsiniz **Ctrl**+**.** Hızlı Eylemler ve yeniden düzenlemeler kullanılabilir bir listesini görmek için herhangi bir yerde bir satıra.

Olası düzeltmeleri görmek için her iki yanındaki aşağı oku ampul seçin veya **olası düzeltmeleri göster** bağlantı. Kullanılabilir hızlı eylemler listesi görüntülenir.

![Genişletilmiş ampul](../ide/media/vs2015_lightbulb_hover_expanded.png)

## <a name="see-also"></a>Ayrıca bkz.

- [Visual Studio'da kod üretimi](../ide/code-generation-in-visual-studio.md)
- [Yaygın Hızlı Eylemler](../ide/common-quick-actions.md)
- [Kod stilleri ve hızlı Eylemler](../ide/code-styles-and-quick-actions.md)
- [Yazma ve yeniden düzenleme kod (C++)](/cpp/ide/writing-and-refactoring-code-cpp)
- [Yeniden düzenleme (Mac için Visual Studio)](/visualstudio/mac/refactoring)
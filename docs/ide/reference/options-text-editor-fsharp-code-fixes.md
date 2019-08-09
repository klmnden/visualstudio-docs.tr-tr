---
title: Seçenekler, metin düzenleyici, F#kod düzeltmeleri
ms.date: 01/16/2019
ms.topic: reference
f1_keywords:
- VS.ToolsOptionsPages.Text_Editor.F%2523.Code_Fixes
author: gewarren
ms.author: gewarren
manager: jillfra
ms.workload:
- dotnet
ms.openlocfilehash: a73991702455fab54baf868499634e1a4f5bbf48
ms.sourcegitcommit: 2da366ba9ad124366f6502927ecc720985fc2f9e
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/09/2019
ms.locfileid: "68870754"
---
# <a name="options-text-editor--f--code-fixes"></a>Seçenekler: Metin düzenleyici > F# > kod düzeltmeleri

Kod hatalarını ve teklif çözümlerini belirlemenize yardımcı olabilecek ayarları belirtmek için kod düzeltmeleri seçenekleri sayfasını kullanın. Bu seçenekler sayfasına erişmek için **Araçlar** > **Seçenekler**' i ve ardından **metin düzenleyici** > **F#**  > **kod düzeltmeleri**' ni seçin.

## <a name="code-fixes"></a>Kod Düzeltmeleri

- **Adları basitleştirme (gereksiz niteleyicileri Kaldır)**

  Bu onay kutusu işaretliyse, nitelikler gerekli olmadığında (sık kullanılan ad alanının bir üyesi gibi) tam nitelikli adlar basitleştirilir.

- **Açık deyimleri her zaman en üst düzeyde yerleştir**

  Bu onay kutusu işaretliyse ve koda bir `open` ifade yazarsanız, en üst düzeye konur.

- **Kullanılmayan açık deyimleri kaldır**

  Bu onay kutusu işaretliyse, belgeler kullanılmamış `open` deyimler için analiz edilir ve tüm kullanılmayan `open` deyimleri kaldırma eylemi içeren hızlı bir [eylem](../quick-actions.md) ampul görüntülenir.

- **Kullanılmayan değerler için düzeltmeleri çözümle ve önerme**

  Bu onay kutusu işaretliyse araç, kodda kullanılmayan bir değeri tanır. Daha sonra, kullanılmayan değerin üzerine geldiğinizde, bu değeri kullanabilmeniz için gereken yolları önerir.

## <a name="see-also"></a>Ayrıca bkz.

- [Genel, Ortam, Seçenekler İletişim Kutusu](../../ide/reference/general-environment-options-dialog-box.md)
- [CodeLens ile kod değişikliklerini ve diğer geçmişi bulma](../../ide/find-code-changes-and-other-history-with-codelens.md)

---
title: Yöntem imzası yeniden düzenleyin
ms.date: 01/26/2018
ms.topic: reference
author: gewarren
ms.author: gewarren
manager: jillfra
f1_keywords:
- vs.csharp.refactoring.remove
- vs.csharp.refactoring.reorder
dev_langs:
- CSharp
- VB
ms.workload:
- dotnet
ms.openlocfilehash: 89af8235f897858094058981df52d6a3fec8a7d6
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62791161"
---
# <a name="change-a-method-signature-refactoring"></a>Bir yöntem imzası yeniden düzenleme değiştirme

Bu yeniden düzenleme için geçerlidir:

- C#

- Visual Basic

**Ne:** Bir yöntemin parametre sırasını değiştirmek veya kaldırmak izin verir.

**ne zaman:** Taşıma veya bir çeşitli yerlerde kullanılmakta olan bir yöntem parametresi kaldırmak istediğiniz.

**Neden:** El ile kaldırın ve parametreleri yeniden Sırala ve ardından bu yönteme tüm çağrılarını bulun ve bunları tek tek değiştirmek, ancak hatalarına neden.  Bu yeniden düzenleme aracı görevi otomatik olarak gerçekleştirir.

## <a name="how-to"></a>Nasıl Yapılır Konuları

1. Vurgulama veya değiştirmek için yöntemi veya kendi kullanımlarından adını metin imleci yerleştirin:

   - C# İÇİN:

       ![Vurgulanmış kodu C#](media/changesignature-highlight-cs.png)

   - VB İÇİN:

       ![Vurgulanan kod Visual Basic](media/changesignature-highlight-vb.png)

2. Ardından, aşağıdakilerden birini yapın:

   - **Klavye**
      - Tuşuna **Ctrl + R**, ardından **Ctrl + V**.  (Bağlı olarak hangi profilinde seçtiğiniz klavye kısayolu farklı olabileceğini unutmayın.)
      - Tuşuna **Ctrl**+**.** Tetikleyici için **hızlı Eylemler ve yeniden düzenlemeler** menü ve select **değişiklik imzası** gelen önizleme penceresi açılır.
   - **Fare**
      - Seçin **Düzenle > Yeniden Düzenle > parametreleri Kaldır**.
      - Seçin **Düzenle > Yeniden Düzenle > parametreleri yeniden Sırala**.
      - Kod sağ tıklayın, **hızlı Eylemler ve yeniden düzenlemeler** menü ve select **değişiklik imzası** gelen önizleme penceresi açılır.

3. İçinde **değişiklik imzası** , açılan iletişim yöntem imzası değiştirmek için sağ tarafındaki düğmeleri kullanabilirsiniz:

   ![Değişiklik imzası iletişim](media/changesignature-dialog-cs.png)

   | Düğme | Açıklama
   | ------ | ---
   | **Yukarı/Aşağı** | Seçili parametreyi listede yukarı ve Aşağı Taşı
   | **Kaldır** | Seçili parametreyi listeden kaldırın
   | **Geri yükleme** | Seçildiğinde, çizilmiş parametre listesine geri yükleme

   > [!TIP]
   > Kullanım **başvuru değişikliklerini önizle** onay kutusu [sonucu görmek](../../ide/preview-changes.md) kendisine gerçekleştirmeden önce.

4. İşlemi tamamladığınızda, basın **Tamam** değişiklik yapmak için düğme.

   - C# İÇİN:

      ![İmza sonucu Değiştir-C#](media/changesignature-result-cs.png)

   - Visual Basic:

      ![İmza sonucu - Visual Basic değiştirme](media/changesignature-result-vb.png)

## <a name="see-also"></a>Ayrıca bkz.

- [Yeniden Düzenleme](../refactoring-in-visual-studio.md)
- [Değişiklikleri Önizleme](../../ide/preview-changes.md)
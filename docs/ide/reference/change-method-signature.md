---
title: Metot imzasını değiştirme
description: Yöntemin parametrelerinin sırasını kaldırın veya değiştirin. Yöntemine sağ tıklayın, hızlı eylemler ve yeniden düzenlemeler ' ı seçin ve Imzayı Değiştir ' i seçin.
ms.date: 01/26/2018
ms.topic: reference
author: mikadumont
ms.author: midumont
manager: jillfra
f1_keywords:
- vs.csharp.refactoring.remove
- vs.csharp.refactoring.reorder
dev_langs:
- CSharp
- VB
ms.workload:
- dotnet
ms.openlocfilehash: 97c03c798732b5d722b2dc49f3ec7ffa490b4f06
ms.sourcegitcommit: 3e74ec49a54e5c3da7631f4466128cdf4384af6b
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/01/2019
ms.locfileid: "68711256"
---
# <a name="change-a-method-signature-refactoring"></a>Bir yöntem imzası yeniden düzenleme değiştirme

Bu yeniden düzenleme için geçerlidir:

- C#

- Visual Basic

**Yazdırılacak** Bir yöntemin parametrelerinin sırasını kaldırmanıza veya değiştirmenize olanak sağlar.

**Oluşturulurken** Şu anda çeşitli konumlarda kullanılmakta olan bir yöntem parametresini taşımak veya kaldırmak istiyorsunuz.

**Kaydol** Parametreleri el ile kaldırıp yeniden sıralayın ve sonra bu yönteme yapılan tüm çağrıları bulabilir ve bunları tek tek değiştirebilir ancak bu hatalara yol açabilir.  Bu yeniden düzenleme aracı görevi otomatik olarak gerçekleştirir.

## <a name="how-to"></a>Nasıl Yapılır Konuları

1. Vurgulama veya değiştirmek için yöntemi veya kendi kullanımlarından adını metin imleci yerleştirin:

   - C# İÇİN:

       ![Vurgulanmış kodu C#](media/changesignature-highlight-cs.png)

   - VB İÇİN:

       ![Vurgulanan kod Visual Basic](media/changesignature-highlight-vb.png)

2. Ardından, aşağıdakilerden birini yapın:

   - **Klavye**
      - Tuşuna **Ctrl + R**, ardından **Ctrl + V**.  (Bağlı olarak hangi profilinde seçtiğiniz klavye kısayolu farklı olabileceğini unutmayın.)
      - Tuşuna **Ctrl**+ **.** Tetikleyici için **hızlı Eylemler ve yeniden düzenlemeler** menü ve select **değişiklik imzası** gelen önizleme penceresi açılır.
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
---
title: Bir özellik için bir alanı yeniden düzenleyin
ms.date: 01/26/2018
ms.prod: visual-studio-dev15
ms.topic: reference
author: gewarren
ms.author: gewarren
manager: douge
f1_keywords:
- vs.csharp.refactoring.encapsulatefield
dev_langs:
- CSharp
- VB
ms.workload:
- dotnet
ms.openlocfilehash: cc2d4e7d7210cc374358c6f5d296f5f99035907a
ms.sourcegitcommit: 37fb7075b0a65d2add3b137a5230767aa3266c74
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/02/2019
ms.locfileid: "53822267"
---
# <a name="encapsulate-a-field-refactoring"></a>Yeniden düzenleme alanı kapsülle

Bu yeniden düzenleme için geçerlidir:

- C#

- Visual Basic

**Ne:** Bir alan bir özellikte açın ve yeni oluşturulan özelliği kullanmak için bu alanın tüm kullanımları güncelleştirme olanak sağlar.

**ne zaman:** Bir alan bir özellikte taşıyın ve bu alanın tüm başvurularını güncelleştirmek istiyorsunuz.

**Neden:** Bir alan diğer sınıflar erişim vermek istediğiniz, ancak söz konusu sınıfın doğrudan erişimine sahip olmasını istemezsiniz.  Bir özellik alanı sarmalama tarafından örneğin atanan değerin doğrulamak için kod yazabilirsiniz.

## <a name="how-to"></a>Nasıl Yapılır Konuları

1. Vurgulama veya yalıtılacak alanın adını metin imleci yerleştirin:

   - C# İÇİN:

       ![Vurgulanan kodu:C#](media/encapsulate-highlight-cs.png)

   - Visual Basic:

       ![Vurgulanmış kodu - Visual Basic](media/encapsulate-highlight-vb.png)

2. Ardından, aşağıdakilerden birini yapın:

   - **Klavye**
      - Tuşuna **Ctrl + R**, ardından **Ctrl + E**.  (Bağlı olarak hangi profilinde seçtiğiniz klavye kısayolu farklı olabileceğini unutmayın.)
      - Tuşuna **Ctrl**+**.** Tetikleyici için **hızlı Eylemler ve yeniden düzenlemeler** menüsü ya da seçin **kapsülleme alanı** girişi önizleme penceresi açılır.
   - **Fare**
      - Seçin **Düzenle > yeniden düzenleyin > alanı Yalıt**.
      - Kod sağ tıklayın, **hızlı Eylemler ve yeniden düzenlemeler** menüsü ya da seçin **kapsülleme alanı** girişi önizleme penceresi açılır.

   Seçim | Açıklama
   --------- | -----------
   **Alanı kapsülle (ve özellik kullan)** | Alan özelliğine sahip kapsüller ve oluşturulan özellik kullanılacak alanın tüm kullanımları güncelleştirir
   **Alanı kapsülle (ancak yine de alan kullan)** | Alan özelliğine sahip saklar, ancak alanın tüm kullanımları dokunulmadan kalır

   Özelliği oluşturulur ve seçtiyseniz alanına yapılan başvurular güncelleştirilir.

   > [!TIP]
   > Kullanım **değişiklik önizlemesi** bağlantıyı açılan pencerede [sonucu görmek için](../../ide/preview-changes.md) kendisine gerçekleştirmeden önce.

   - C# İÇİN:

      ![Özellik sonucu kapsülleyen-C#](media/encapsulate-result-cs.png)

   - Visual Basic:

      ![Özellik sonucu - Visual Basic yalıtma](media/encapsulate-result-vb.png)

## <a name="see-also"></a>Ayrıca bkz.

- [Yeniden Düzenleme](../refactoring-in-visual-studio.md)
- [Değişiklikleri Önizleme](../../ide/preview-changes.md)
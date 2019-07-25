---
title: Bir yöntemi
description: Kodu seçip CTRL + R, CTRL + M yazarak kodun bir parçasını kendi yöntemine dönüştürün.
ms.date: 01/26/2018
ms.topic: reference
author: gewarren
ms.author: gewarren
manager: jillfra
f1_keywords:
- vs.csharp.refactoring.extractmethod
dev_langs:
- CSharp
- VB
ms.workload:
- dotnet
ms.openlocfilehash: a764fd0d95696866e914ec76a560a49d641acb47
ms.sourcegitcommit: 0f5f7955076238742f2071d286ad8e896f3a6cad
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/25/2019
ms.locfileid: "68483665"
---
# <a name="extract-a-method-refactoring"></a>Ayıklama yöntemi yeniden düzenleme

Bu yeniden düzenleme için geçerlidir:

- C#

- Visual Basic

**Yazdırılacak** Kodun bir parçasını kendi yöntemine açmanızı sağlar.

**Oluşturulurken** Başka bir yöntemden çağrılması gereken, bazı bir yöntemde var olan kodun bir parçası var.

**Kaydol** Bu kodu kopyalayabilir/yapıştırabilir, ancak çoğaltmaya yol açabilir. Bu parça halinde diğer herhangi bir yöntemle serbestçe çağrılabilir kendi yöntemi yeniden düzenleme daha iyi bir çözümdür.

## <a name="how-to"></a>Nasıl Yapılır Konuları

1. Ayıklanacak kod vurgular:

   - C# İÇİN:

       ![Vurgulanan kod-C#](media/extractmethod-highlight-cs.png)

   - Visual Basic:

       ![Vurgulanmış kodu - Visual Basic](media/extractmethod-highlight-vb.png)

2. Ardından, aşağıdakilerden birini yapın:

   - **Klavye**
      - Tuşuna **Ctrl + R**, ardından **Ctrl + M**. (Bağlı olarak hangi profilinde seçtiğiniz klavye kısayolu farklı olabileceğini unutmayın.)
      - Tuşuna **Ctrl**+ **.** Tetikleyici için **hızlı Eylemler ve yeniden düzenlemeler** menü ve select **yöntemi ayıklama** gelen önizleme penceresi açılır.
   - **Fare**
      - Seçin **Düzenle > yeniden düzenleyin > yöntemi Ayıkla**.
      - Kod sağ tıklayıp **yeniden düzenleyin > Ayıkla > yöntemi ayıklama**.
      - Kod sağ tıklayın, **hızlı Eylemler ve yeniden düzenlemeler** menü ve select **yöntemi ayıklama** gelen önizleme penceresi açılır.

   Yöntem hemen oluşturulur. Buradan, yeni bir ad yazarak artık yöntemi adlandırabilirsiniz.

   > [!TIP]
   > Ayrıca açıklamalar ve diğer dizeleri bu yeni adı kullanacak şekilde güncelleştirebilirsiniz yanı [değişiklik önizlemesi](../../ide/preview-changes.md) önce kaydetme, içinde onay kutularını kullanarak **Yeniden Adlandır** en üstünde açılan kutusunda IDE'nizi sağında.

   - C# İÇİN:

      ![Metodu yeniden adlandır-C#](media/extractmethod-rename-cs.png)

   - Visual Basic:

      ![Yöntemi - Visual Basic yeniden adlandır](media/extractmethod-rename-vb.png)

3. Değişiklik ile tamamladığınızda seçin **Uygula** düğme veya basın **Enter** ve değişiklikler uygulanır.

## <a name="see-also"></a>Ayrıca bkz.

- [Yeniden Düzenleme](../refactoring-in-visual-studio.md)
- [Değişiklikleri Önizleme](../../ide/preview-changes.md)
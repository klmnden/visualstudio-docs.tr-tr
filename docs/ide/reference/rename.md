---
title: Yeniden Adlandır yeniden düzenleyin
ms.date: 01/26/2018
ms.prod: visual-studio-dev15
ms.topic: reference
author: gewarren
ms.author: gewarren
manager: jillfra
f1_keywords:
- vs.csharp.refactoring.rename
dev_langs:
- CSharp
- VB
ms.workload:
- dotnet
ms.openlocfilehash: b0058a71205f707ee8ea3050e3a926571dec4ca3
ms.sourcegitcommit: 2193323efc608118e0ce6f6b2ff532f158245d56
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/25/2019
ms.locfileid: "54917191"
---
# <a name="rename-a-code-symbol-refactoring"></a>Bir kod sembol yeniden düzenlemeyi yeniden adlandırma

Bu yeniden düzenleme için geçerlidir:

- C#

- Visual Basic

**Ne:** Alanlar, yerel değişkenler, yöntemleri, ad alanları, özellikler ve türler gibi kod simgeleri tanımlayıcıları yeniden adlandır olanak tanır.

**ne zaman:** Güvenli bir şekilde bir şey tüm örneklerini bulun ve yeni adı kopyala/yapıştır gerekmeden yeniden adlandırmak istediğiniz.

**Neden:** Kopyalayıp yeni bir ad, bir projenin tamamı yapıştırarak musunuz büyük olasılıkla hatalara neden. Bu yeniden düzenleme aracı doğru yeniden adlandırma eylemi gerçekleştirir.

## <a name="how-to"></a>Nasıl Yapılır Konuları

1. Vurgulama veya yeniden adlandırılacak öğe metin imleci yerleştirin:

   - C# İÇİN:

       ![Vurgulanan kodu:C#](media/rename-highlight-cs.png)

   - Visual Basic:

       ![Vurgulanmış kodu - Visual Basic](media/rename-highlight-vb.png)

2. Ardından, aşağıdakilerden birini yapın:

   - **Klavye**
      - Tuşuna **Ctrl + R**, ardından **Ctrl + R**. (Bağlı olarak hangi profilinde seçtiğiniz klavye kısayolu farklı olabileceğini unutmayın.)
   - **Fare**
      - Seçin **Düzenle > yeniden düzenleyin > Yeniden Adlandır**.
      - Kod sağ tıklayıp **Yeniden Adlandır**.

3. Yeni bir ad yazarak öğeyi yeniden adlandırın.

   - C# İÇİN:

      ![Animasyon yeniden adlandır-C#](media/rename-animated-cs.gif)

   - Visual Basic:

      ![Rename - VB](media/rename-rename-vb.png)

   > [!TIP]
   > Ayrıca açıklamalar ve diğer dizeleri bu yeni adı kullanacak şekilde güncelleştirebilirsiniz yanı [değişiklikleri Önizleme](../../ide/preview-changes.md) önce kaydetme, içinde onay kutularını kullanarak **Yeniden Adlandır** en üstünde açılan kutusunda düzenleyiciniz sağında.

4. Değişiklik ile tamamladığınızda seçin **Uygula** düğme veya basın **Enter** ve değişiklikler uygulanır.

> [!NOTE]
> Bir çakışma neden zaten var olan bir ad kullanırsanız **Yeniden Adlandır** kutusunun sizi uyaracaktır.
>
> ![Yeniden adlandırma çakışması](media/rename-conflict-cs.png)

## <a name="see-also"></a>Ayrıca bkz.

- [Yeniden Düzenleme](../refactoring-in-visual-studio.md)
- [Değişiklikleri Önizleme](../../ide/preview-changes.md)

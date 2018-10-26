---
title: Visual Studio'da bir yöntemi
ms.date: 01/26/2018
ms.prod: visual-studio-dev15
ms.technology: vs-ide-general
ms.topic: reference
author: gewarren
ms.author: gewarren
manager: douge
f1_keywords:
- vs.csharp.refactoring.extractmethod
dev_langs:
- CSharp
- VB
ms.workload:
- dotnet
ms.openlocfilehash: 049b3caebc884ea22bd2928e9e4ff10e9921fd1d
ms.sourcegitcommit: 240c8b34e80952d00e90c52dcb1a077b9aff47f6
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/23/2018
ms.locfileid: "49930602"
---
# <a name="extract-a-method-refactoring"></a>Ayıklama yöntemi yeniden düzenleme

Bu yeniden düzenleme için geçerlidir:

- C#

- Visual Basic

**Ne:** kendi yönteme kodun bir parçasını kapatmanızı sağlar.

**Ne zaman:** başka bir yöntemden çağrılması gereken bazı yöntemi mevcut kodun bir parçasını sahip.

**Neden:** , Kopyala/kod Yapıştır, ancak çoğaltma için neden. Bu parça halinde diğer herhangi bir yöntemle serbestçe çağrılabilir kendi yöntemi yeniden düzenleme daha iyi bir çözümdür.

## <a name="how-to"></a>Nasıl Yapılır Konuları

1. Ayıklanacak kod vurgular:

   - C# İÇİN:

       ![Vurgulanan kod-C#](media/extractmethod-highlight-cs.png)

   - Visual Basic:

       ![Vurgulanmış kodu - Visual Basic](media/extractmethod-highlight-vb.png)

2. Ardından, aşağıdakilerden birini yapın:

   - **Klavye**
      - Tuşuna **Ctrl + R**, ardından **Ctrl + M**. (Bağlı olarak hangi profilinde seçtiğiniz klavye kısayolu farklı olabileceğini unutmayın.)
      - Tuşuna **Ctrl**+**.** Tetikleyici için **hızlı Eylemler ve yeniden düzenlemeler** menü ve select **yöntemi ayıklama** gelen önizleme penceresi açılır.
   - **Fare**
      - Seçin **Düzenle > yeniden düzenleyin > yöntemi Ayıkla**.
      - Kod sağ tıklayıp **yeniden düzenleyin > Ayıkla > yöntemi ayıklama**.
      - Kod sağ tıklayın, **hızlı Eylemler ve yeniden düzenlemeler** menü ve select **yöntemi ayıklama** gelen önizleme penceresi açılır.

   Yöntem hemen oluşturulur. Buradan, yeni bir ad yazarak artık yöntemi adlandırabilirsiniz.

   > [!TIP]
   > Ayrıca açıklamalar ve diğer dizeleri bu yeni adı kullanacak şekilde güncelleştirebilirsiniz yanı [değişiklik önizlemesi](../../ide/preview-changes.md) önce kaydetme, içinde onay kutularını kullanarak **Yeniden Adlandır** üst kısmında görünür kutusunu IDE'nizi sağında.

   - C# İÇİN:

      ![Metodu yeniden adlandır-C#](media/extractmethod-rename-cs.png)

   - Visual Basic:

      ![Yöntemi - Visual Basic yeniden adlandır](media/extractmethod-rename-vb.png)

3. Değişiklik ile tamamladığınızda seçin **Uygula** düğme veya basın **Enter** ve değişiklikler uygulanır.

## <a name="see-also"></a>Ayrıca bkz.

- [Yeniden Düzenleme](../refactoring-in-visual-studio.md)
- [Değişiklikleri Önizleme](../../ide/preview-changes.md)
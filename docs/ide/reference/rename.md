---
title: Yeniden Adlandır yeniden düzenleyin
ms.date: 01/26/2018
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
ms.openlocfilehash: d1b4ff448f04ff6f683fac06cbc0b31797edf587
ms.sourcegitcommit: 88f576ac32af31613c1a10c1548275e1ce029f4f
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/23/2019
ms.locfileid: "71186587"
---
# <a name="rename-a-code-symbol-refactoring"></a>Bir kod sembol yeniden düzenlemeyi yeniden adlandırma

Bu yeniden düzenleme için geçerlidir:

- C#

- Visual Basic

**Yazdırılacak** Alanlar, yerel değişkenler, Yöntemler, ad alanları, Özellikler ve türler gibi kod sembolleri için tanımlayıcıları yeniden adlandırmanızı sağlar.

**Oluşturulurken** Tüm örnekleri bulmak zorunda kalmadan bir şeyi güvenle yeniden adlandırmak ve yeni adı kopyalayıp yapıştırmak istiyorsunuz.

**Kaydol** Yeni adı bir projenin tamamına kopyalamak ve yapıştırmak muhtemelen hatalara neden olabilir. Bu yeniden düzenleme aracı doğru yeniden adlandırma eylemi gerçekleştirir.

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

## <a name="remarks"></a>Açıklamalar

- Visual Studio 2019 sürüm 16,3 ' den başlayarak, içindeki dosyanın adıyla eşleşen bir türü yeniden adlandırdığınızda, dosyayı aynı anda yeniden adlandırmanızı sağlayan bir onay kutusu görüntülenir. Bu seçenek, bir sınıfı, arabirimi veya numaralandırmayı yeniden adlandırdığınızda görüntülenir. Bu seçenek, birden çok tanım içeren kısmi türler için desteklenmez.

   ![Animasyonu dosyayla yeniden adlandırma-C#](media/rename-with-file-animated-cs.gif)
   
- Bir çakışma neden zaten var olan bir ad kullanırsanız **Yeniden Adlandır** kutusunun sizi uyaracaktır.

   ![Yeniden adlandırma çakışması](media/rename-conflict-cs.png)

- Bir sembolü yeniden adlandırmaya yönelik başka bir yol da düzenleyicide adını değiştirkullanmaktır. Ardından, imleç sembol adında, **CTRL**+tuşuna basın **.** ya da görünen ampul simgesi menüsünü genişlettikten sonra **eski adı > > \<yeni ad olarak \<yeniden adlandır**' ı seçin.

## <a name="see-also"></a>Ayrıca bkz.

- [Yeniden Düzenleme](../refactoring-in-visual-studio.md)
- [Değişiklikleri Önizleme](../../ide/preview-changes.md)

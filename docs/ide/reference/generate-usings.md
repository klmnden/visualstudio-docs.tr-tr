---
title: Using deyimleri oluşturma
ms.date: 02/19/2019
ms.topic: reference
author: kendrahavens
ms.author: kehavens
manager: jillfra
dev_langs:
- CSharp
ms.workload:
- dotnet
ms.openlocfilehash: 9124054dec08fde94ec98ca9e3ebdfb6e48d7384
ms.sourcegitcommit: 614d5b99576ea27a41957cd94062dc95cbd29c1c
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/10/2019
ms.locfileid: "65531626"
---
# <a name="generate-usings-in-visual-studio"></a>Visual Studio'da kullanımları oluşturun

Bu kod oluşturma için geçerlidir:

- C#

**Ne:** Gerekli içeri aktarmaları hemen eklemenize olanak sağlayan veya [using deyimlerini](/dotnet/csharp/language-reference/keywords/using-statement) kopyalama yapıştırılmış kod için.

**ne zaman:** Projenizi veya diğer kaynaklardan farklı yerlerde kodu kopyalayın ve yeni koda yapıştırın için yaygın bir uygulamadır. Bu hızlı eylem eksik kopyalama yapıştırılmış kod deyimlerini içeri aktarır ve ardından bunları eklemek ister bulur.

**Neden:** Hızlı eylem gerekli içeri aktarmaları otomatik olarak eklediğinden, el ile kopyalamanız gerekmez `using` kodunuzu gereken deyimleri.

## <a name="generate-usings-refactoring"></a>Using deyimlerini yeniden düzenleme oluştur

1. Bir dosyadan kodu kopyalayın ve gerekli dahil olmak üzere olmadan yeni bir tane yapıştırın `using` deyimleri. Ortaya çıkan hata eksik ekleyen bir kod düzeltme ile birlikte sunulduğu `using` deyimleri.

    > [!NOTE]
    > Bu önerisine etkinleştirmek gereken **Araçlar > Seçenekler > Metin Düzenleyicisi > C# > Gelişmiş > yönergeleri kullanarak**.

2. CTRL + seçin. açmak için **hızlı Eylemler ve yeniden düzenlemeler** menüsü.

    ![Using deyimleri oluşturma](media/generate-using-codefix.png)

3. Seçin **kullanarak \<başvurunuz\>;** eksik başvuru eklenemiyor.

    ![Using deyimlerini sonucu oluştur](media/generate-using-result.png)

## <a name="see-also"></a>Ayrıca bkz.

- [Kod oluşturma](../code-generation-in-visual-studio.md)
- [Değişiklikleri Önizleme](../../ide/preview-changes.md)
- [.NET geliştiricileri için ipuçları](../csharp-developer-productivity.md)

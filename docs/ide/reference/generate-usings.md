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
helpviewer_keywords:
- add missing usings
ms.openlocfilehash: d971bcdaca4efdf587c7e441f1b0b28d21388dee
ms.sourcegitcommit: 59e5758036223ee866f3de5e3c0ab2b6dbae97b6
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/23/2019
ms.locfileid: "68416471"
---
# <a name="add-missing-usings-in-visual-studio"></a>Visual Studio 'da eksik using 'leri ekleme

Bu kod oluşturma için geçerlidir:

- C#

**Yazdırılacak** Kopya ve yapıştırılan kod için gerekli içeri aktarmaları veya [using deyimlerini](/dotnet/csharp/language-reference/keywords/using-statement) hemen eklemenizi sağlar.

**Oluşturulurken** Projenizde veya diğer kaynaklardaki farklı yerlerden kod kopyalamak ve yeni koda yapıştırmak yaygın bir uygulamadır. Bu hızlı eylem, kopya ve yapıştırılan kod için eksik Imports deyimlerini bulur ve sonra bunları eklemenizi ister.

**Kaydol** Hızlı eylem gerekli içeri aktarmaları otomatik olarak eklediğinden, kodunuzun ihtiyaç duyduğu `using` deyimleri el ile kopyalamanız gerekmez.

## <a name="add-missing-usings-refactoring"></a>Eksik using 'leri yeniden düzenleme Ekle

1. Kodu bir dosyadan kopyalayın ve gerekli `using` deyimleri dahil etmeden yeni bir dosyaya yapıştırın. Ortaya çıkan hata, eksik `using` deyimleri ekleyen bir kod düzeltmesine eşlik eder.

    > [!NOTE]
    > **Araçlar > seçenekler > metin düzenleyicisi > C# yönergeleri kullanarak Gelişmiş > >** bu öneriyi etkinleştirmeniz gerekir.

2. CTRL + seçeneğini belirleyin. **Hızlı Eylemler ve yeniden düzenlemeler** menüsünü açmak için.

    ![Using deyimleri oluşturma](media/generate-using-codefix.png)

3. Eksik başvuruyu eklemek için **başvurunuz \<\>** ' ı kullanmayı seçin.

    ![Kullanımlar sonucu oluştur](media/generate-using-result.png)

## <a name="see-also"></a>Ayrıca bkz.

- [Kod oluşturma](../code-generation-in-visual-studio.md)
- [Değişiklikleri Önizleme](../../ide/preview-changes.md)
- [.NET geliştiricileri için ipuçları](../csharp-developer-productivity.md)

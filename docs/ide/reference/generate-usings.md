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
ms.openlocfilehash: afd4b758332d9357dc20dd84e726d72da4d2db74
ms.sourcegitcommit: 3201da3499051768ab59f492699a9049cbc5c3c6
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/22/2019
ms.locfileid: "58355195"
---
# <a name="generate-usings-in-visual-studio"></a>Visual Studio'da kullanımları oluşturun

Bu kod oluşturma için geçerlidir:

- C#

**Ne:** Gerekli içeri aktarmaları hemen eklemenize olanak sağlayan veya [using deyimlerini](/dotnet/csharp/language-reference/keywords/using-statement) kopyalama yapıştırılmış kod.

**ne zaman:** Kopyalayıp farklı yerlerde kod projenizi veya diğer kod kaynakları yapıştırmak için yaygın bir uygulamadır. Bu hızlı eylem eksik Imports kopyalama yapıştırılmış kod analiz eder ve ardından bunları eklemek isteyip istemediğinizi sorar.

**Neden:** Gerekli içeri aktarmaları otomatik olarak ekleyerek, kullanıcının gerekli el ile kopyalamanız gerekmez `using` deyimleri.

## <a name="generate-usings-refactoring"></a>Using deyimlerini yeniden düzenleme oluştur

1. Gerekli dahil olmak üzere farklı bir dosyadaki kodu yapıştırın `using` deyimleri. Hata artık eksik ekleyen bir kod düzeltme ile eşlik `using` deyimleri.

    > [!NOTE] 
    > Bu öneri, açık olması gerekiyor **Araçlar > Seçenekler > Metin Düzenleyicisi > C# > Gelişmiş > yönergeleri kullanarak**.

2. Tuşuna **Ctrl**+**.** açmak için **hızlı Eylemler ve yeniden düzenlemeler** menüsü. 

    ![Using deyimleri oluşturma](media/generate-using-codefix.png)

3. Seçin **kullanarak \<başvurunuz\>;** eksik başvuru eklenemiyor.

    ![Using deyimlerini sonucu oluştur](media/generate-using-result.png)

## <a name="see-also"></a>Ayrıca bkz.

- [Kod Oluşturma](../code-generation-in-visual-studio.md)
- [Değişiklikleri Önizleme](../../ide/preview-changes.md)
- [.NET Geliştiricileri için İpuçları](../../ide/visual-studio-2017-for-dotnet-developers.md)

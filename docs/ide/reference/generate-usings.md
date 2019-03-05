---
title: Using deyimlerini oluşturmak
ms.date: 02/19/2019
ms.topic: reference
author: kendrahavens
ms.author: kendrahavens
manager: jillfra
dev_langs:
- CSharp
ms.workload:
- dotnet
ms.openlocfilehash: 9fd34b40bdd1167eca7fa1dff8ab60bcc787b7c7
ms.sourcegitcommit: 11337745c1aaef450fd33e150664656d45fe5bc5
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/04/2019
ms.locfileid: "57325296"
---
# <a name="generate-usings-in-visual-studio"></a>Visual Studio'da kullanımları oluşturun

Bu kod oluşturma için geçerlidir:

- C#

**Ne:** **Ne:** Gerekli içeri aktarmaları hemen eklemenize olanak sağlayan veya [using deyimlerini](/dotnet/csharp/language-reference/keywords/using-statement) kopyalama yapıştırılmış kod.

**ne zaman:** Kopyalayıp farklı yerlerde kod projenizi veya diğer kod kaynakları yapıştırmak için yaygın bir uygulamadır. Bu hızlı eylem eksik Imports kopyalama yapıştırılmış kod analiz eder ve ardından bunları eklemek isteyip istemediğinizi sorar.

**Neden:** Gerekli içeri aktarmaları otomatik olarak ekleyerek, kullanıcının gerekli el ile kopyalamanız gerekmez `using` deyimleri.

## <a name="generate-usings-refactoring"></a>Using deyimlerini yeniden düzenleme oluştur

1. Gerekli dahil olmak üzere farklı bir dosyadaki kodu yapıştırın `using` deyimleri. Hata artık eksik ekleyen bir kod düzeltme ile eşlik `using` deyimleri.

    > [!NOTE] 
    > Bu öneri, açık olması gerekiyor **Araçlar > Seçenekler > Metin Düzenleyicisi > C# > Gelişmiş > yönergeleri kullanarak**.

2. Tuşuna **Ctrl**+**.** açmak için **hızlı Eylemler ve yeniden düzenlemeler** menüsü. 

    ![Using deyimlerini oluşturmak](media/generate-using-codefix.png)

3. Seçin **kullanarak \<başvurunuz\>;** eksik başvuru eklenemiyor.

    ![Using deyimlerini sonucu oluştur](media/generate-using-result.png)

## <a name="see-also"></a>Ayrıca bkz.

- [Kod Oluşturma](../code-generation-in-visual-studio.md)
- [Değişiklikleri Önizleme](../../ide/preview-changes.md)
- [.NET Geliştiricileri için İpuçları](../../ide/visual-studio-2017-for-dotnet-developers.md)
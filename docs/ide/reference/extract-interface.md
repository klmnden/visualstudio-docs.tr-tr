---
title: Bir arabirimi yeniden düzenleme ayıklayın
ms.date: 01/26/2018
ms.topic: reference
author: gewarren
ms.author: gewarren
manager: jillfra
f1_keywords:
- vs.csharp.refactoring.extractinterface
dev_langs:
- CSharp
- VB
ms.workload:
- dotnet
ms.openlocfilehash: f0036bb9bf8ef6d0c09fddc2b8ac0a4977c3674c
ms.sourcegitcommit: 11337745c1aaef450fd33e150664656d45fe5bc5
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/04/2019
ms.locfileid: "57323442"
---
# <a name="extract-an-interface-refactoring"></a>Bir arabirimi yeniden düzenleme ayıklayın

Bu yeniden düzenleme için geçerlidir:

- C#

- Visual Basic

**Ne:** Varolan bir sınıf, yapı veya arabirim üyelerini kullanarak bir arabirim oluşturmanıza olanak sağlar.

**ne zaman:** Bir sınıf, yapı veya diğer sınıflar, yapılar veya arabirimleri tarafından devralınır arabirim üyeleri var.

**Neden:** Arabirimleri, nesne yönelimli tasarım harika yapılarıdır. Sınıflar için tüm Eat, içecek, uyku gibi yaygın yöntemleri olabilir çeşitli hayvanlar (Dog, Kedi, Bird) sahip olduğunuzu düşünelim. IAnimal gibi bir arabirim kullanarak köpek Cat ve Bird ortak bir "SIGNATURE" Bu yöntemlere ait olmasını çalıştırmasına olanak tanır.

## <a name="extract-an-interface-refactoring"></a>Bir arabirimi yeniden düzenleme ayıklayın

1. İmlecinizi, sınıf adını yerleştirin.

   - C#:

       ![Vurgulanan kodu:C#](media/extractinterface-highlight-cs.png)

   - Visual Basic:

       ![Vurgulanmış kodu - Visual Basic](media/extractinterface-highlight-vb.png)

2. Ardından, aşağıdaki işlemlerden birini yapın:

   - **Klavye**
      - Tuşuna **Ctrl + R**, ardından **Ctrl + ı**. (Klavye kısayolu hangi profilini temel alan farklı olabilir, seçtiğiniz.)
      - Tuşuna **Ctrl**+**.** Tetikleyici için **hızlı Eylemler ve yeniden düzenlemeler** menü ve select **Arabirimi Ayıkla** gelen önizleme penceresi açılır.
   - **Fare**
      - Seçin **Düzenle > yeniden düzenleyin > Arabirimi Ayıkla**.
      - Select sınıf adına sağ tıklayın **hızlı Eylemler ve yeniden düzenlemeler** menü ve select **Arabirimi Ayıkla** gelen önizleme penceresi açılır.

3. İçinde **Arabirimi Ayıkla** , açılan iletişim kutusunda sorulan bilgileri girin:

   ![Ayıklama Arabirimi](media/extractinterface-dialog-same-file.png)


   | Alan | Açıklama |
   | - | - |
   | **Yeni arabirimin adı** | Oluşturulacak arabirimin adı. T adı varsayılan*ClassName*burada *ClassName* Yukarıda seçilen sınıf adıdır. |
   | **Yeni dosya adı** | Arabirim içeren oluşturulan dosyanın adı. Arabirim adı ile bu ad t varsayılacaktır gibi*ClassName*burada *ClassName* Yukarıda seçilen sınıf adıdır. Seçeneğini de seçebilirsiniz **geçerli dosyaya eklemek**. |
   | **Form arabirimi için genel üyeleri seçin** | Ayıklama arabirimi öğelerdir. İstediğiniz kadar çok seçebilirsiniz. |


4. Seçin **Tamam**.

   Belirtilen adı dosyasında arabirimi oluşturulur. Buna ek olarak, seçtiğiniz sınıfı bu arabirimi uygular.

   - C# İÇİN:

      ![Sonuçta elde edilen sınıfı - C# ](media/extractinterface-class-cs.png) ![elde edilen Interface -C#](media/extractinterface-interface-cs.png)

   - Visual Basic:

      ![Sonuçta elde edilen sınıfı - Visual Basic](media/extractinterface-class-vb.png) ![elde edilen Interface - Visual Basic](media/extractinterface-interface-vb.png)

## <a name="see-also"></a>Ayrıca bkz.

- [Yeniden Düzenleme](../refactoring-in-visual-studio.md)
- [.NET Geliştiricileri için İpuçları](../../ide/visual-studio-2017-for-dotnet-developers.md)
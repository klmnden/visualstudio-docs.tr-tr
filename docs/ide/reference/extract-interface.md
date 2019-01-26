---
title: Bir arabirimi yeniden düzenleme ayıklayın
ms.date: 01/26/2018
ms.prod: visual-studio-dev15
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
ms.openlocfilehash: fe61ca799b6df00acc34a0579398d612c142c2c2
ms.sourcegitcommit: 2193323efc608118e0ce6f6b2ff532f158245d56
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/25/2019
ms.locfileid: "55028479"
---
# <a name="extract-an-interface-refactoring"></a>Bir arabirimi yeniden düzenleme ayıklayın

Bu yeniden düzenleme için geçerlidir:

- C#

- Visual Basic

**Ne:** Varolan bir sınıf, yapı veya arabirim üyelerini kullanarak bir arabirim oluşturmanıza olanak sağlar.

**ne zaman:** Sahip olduğunuz çeşitli sınıflar, yapılar veya arabirimleri yöntemleriyle ortak ve diğer sınıflar, yapılar veya arabirimleri tarafından kullanılan yapılamadı.

**Neden:** Arabirimleri, nesne yönelimli tasarım harika yapılarıdır. Sınıflar için tüm Eat, içecek, uyku gibi yaygın yöntemleri olabilir çeşitli hayvanlar (Dog, Kedi, Bird) sahip olduğunuzu düşünelim. IAnimal gibi bir arabirim kullanarak köpek Cat ve Bird ortak bir "SIGNATURE" Bu yöntemlere ait olmasını çalıştırmasına olanak tanır.

## <a name="how-to"></a>Nasıl Yapılır Konuları

1. Eylemi gerçekleştirmek için sınıfın adını vurgulayın veya yalnızca metin imleç sınıf adını yere yerleştirin.

   - C# İÇİN:

       ![Vurgulanan kodu:C#](media/extractinterface-highlight-cs.png)

   - Visual Basic:

       ![Vurgulanmış kodu - Visual Basic](media/extractinterface-highlight-vb.png)

2. Ardından, aşağıdakilerden birini yapın:

   - **Klavye**
      - Tuşuna **Ctrl + R**, ardından **Ctrl + ı**. (Bağlı olarak hangi profilinde seçtiğiniz klavye kısayolu farklı olabileceğini unutmayın.)
      - Tuşuna **Ctrl**+**.** Tetikleyici için **hızlı Eylemler ve yeniden düzenlemeler** menü ve select **Arabirimi Ayıkla** gelen önizleme penceresi açılır.
   - **Fare**
      - Seçin **Düzenle > yeniden düzenleyin > Arabirimi Ayıkla**.
      - Select sınıf adına sağ tıklayın **hızlı Eylemler ve yeniden düzenlemeler** menü ve select **Arabirimi Ayıkla** gelen önizleme penceresi açılır.

3. İçinde **Arabirimi Ayıkla** , açılan iletişim kutusunda sorulan bilgileri girin:

   ![Ayıklama Arabirimi](media/extractinterface-dialog-cs.png)


   | Alan | Açıklama |
   | - | - |
   | **Yeni arabirimin adı** | Oluşturulacak arabirimin adı. Bu t varsayılan*ClassName*burada *ClassName* Yukarıda seçilen sınıf adıdır. |
   | **Yeni dosya adı** | Arabirimi içerecektir üretilecek dosyanın adı. Arabirim adı ile bu t varsayılan olarak*ClassName*burada *ClassName* Yukarıda seçilen sınıf adıdır. |
   | **Form arabirimi için genel üyeleri seçin** | Ayıklama arabirimi öğelerdir. İstediğiniz kadar çok seçebilirsiniz. |


4. Seçin **Tamam**.

   Belirtilen adı dosyasında arabirimi oluşturulur. Buna ek olarak, seçtiğiniz sınıfı bu arabirimi uygular.

   - C# İÇİN:

      ![Sonuçta elde edilen sınıfı - C# ](media/extractinterface-class-cs.png) ![elde edilen Interface -C#](media/extractinterface-interface-cs.png)

   - Visual Basic:

      ![Sonuçta elde edilen sınıfı - Visual Basic](media/extractinterface-class-vb.png) ![elde edilen Interface - Visual Basic](media/extractinterface-interface-vb.png)

## <a name="see-also"></a>Ayrıca bkz.

- [Yeniden Düzenleme](../refactoring-in-visual-studio.md)
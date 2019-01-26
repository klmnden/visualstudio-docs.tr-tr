---
title: Bir yerel değişken ekleme
ms.date: 01/26/2018
ms.prod: visual-studio-dev15
ms.topic: reference
author: gewarren
ms.author: gewarren
manager: jillfra
ms.workload:
- dotnet
ms.openlocfilehash: 2fcd6032879dc8e218aa782d27a34250982fb7c3
ms.sourcegitcommit: 2193323efc608118e0ce6f6b2ff532f158245d56
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/25/2019
ms.locfileid: "54961955"
---
# <a name="introduce-a-local-variable-in-visual-studio"></a>Visual Studio'da bir yerel değişken ekleme

Bu kod oluşturma için geçerlidir:

- C#

- Visual Basic

**Ne:** Var olan bir ifade değiştirmek için bir yerel değişken hemen oluşturmanıza olanak sağlar.

**ne zaman:** Yerel bir değişkende olsaydı kolayca daha sonra yeniden kullanılabilen kodlarla kodu var.

**Neden:** Kopyalayın ve sonra işlemi gerçekleştirmek, sonucu yerel bir değişkende depolar ve yerel bir değişken boyunca kullanmanız daha iyi ancak kodu çeşitli konumlarda kullanmak için birden çok kez yapıştırın.

## <a name="how-to"></a>Nasıl Yapılır Konuları

1. Yeni bir yerel değişkene atamak istediğiniz ifade vurgulayın.

   - C# İÇİN:

       ![Vurgulanmış kodu C#](media/local-highlight-cs.png)

   - Visual Basic:

       ![Vurgulanmış kodu VB](media/local-highlight-vb.png)

2. Ardından, aşağıdakilerden birini yapın:

   - **Klavye**
      - Tuşuna **Ctrl**+**.** Tetikleyici için **hızlı Eylemler ve yeniden düzenlemeler** menüsü.
   - **Fare**
      - Sağ tıklayıp **hızlı Eylemler ve yeniden düzenlemeler** menüsü.
      - &nbsp; ![Ampul](media/bulb-cs.png) kırmızı dalgalı çizgi içeren satırda metin imleci ise sol kenar boşluğunda görünür simge.

   ![Yerel Önizleme Ekle](media/local-preview-cs.png)

3. Seçin **(tüm örnekleri için) bir yerel değişken Ekle '*ifade*'** aşağı açılan menüden.

   > [!TIP]
   > Kullanım **değişiklik önizlemesi** Önizleme pencerenin alt kısmındaki bağlantı [tüm değişiklikleri görmek için](../../ide/preview-changes.md) , oluşturulacak, seçim yapmadan önce.

   Yerel değişken, kullanımdan çıkarılan türü ile oluşturulur. Yeni yerel değişkeni, yeni bir ad verin.

   - C# İÇİN:

       ![C# arabirimi sonucu uygulayın](media/local-result-cs.png)

   - Visual Basic:

       ![Uygulama arabirimi sonucu VB](media/local-result-vb.png)

   > [!NOTE]
   > Kullanabileceğiniz **.. .all oluşumlarını...**  menü seçeneğini seçili ifadesi, yalnızca özellikle vurgulanmış bir her örneğini değiştirin.

## <a name="see-also"></a>Ayrıca bkz.

- [Kod Oluşturma](../code-generation-in-visual-studio.md)
- [Değişiklikleri Önizleme](../../ide/preview-changes.md)
---
title: Bir yerel değişken ekleme
ms.date: 01/26/2018
ms.topic: reference
author: gewarren
ms.author: gewarren
manager: jillfra
ms.workload:
- dotnet
ms.openlocfilehash: 5564752fcecfe2d7a1b2d0bf7632a9cebe3d9353
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62541044"
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
      - &nbsp; ![Tornavida](media/screwdriver.png) Sol kenar boşluğunda vurgulanan ifadesiyle satırındaki metin imleci ise görüntülenen simge.

   ![Yerel Önizleme Ekle](media/local-preview-cs.png)

3. Seçin **'expression' (tüm örnekleri) için yerel tanıt** aşağı açılan menüden.

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

- [Kod oluşturma](../code-generation-in-visual-studio.md)
- [Değişiklikleri Önizle](../../ide/preview-changes.md)
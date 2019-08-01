---
title: Bir yerel değişken ekleme
description: Varolan bir ifadeyi değiştirmek için yerel bir değişken oluşturun. İfadeyi seçin, sağ tıklayın ve hızlı eylemler ve yeniden düzenlemeler menüsünü seçin, ' expression ' ' ın (tüm oluşumlar) için yerel Ekle ' yi seçin.
ms.date: 01/26/2018
ms.topic: reference
author: gewarren
ms.author: gewarren
manager: jillfra
ms.workload:
- dotnet
ms.openlocfilehash: 43f54072d495cfdd6607ccb033ffd1a1713ad8bb
ms.sourcegitcommit: 0f5f7955076238742f2071d286ad8e896f3a6cad
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/25/2019
ms.locfileid: "68483692"
---
# <a name="introduce-a-local-variable-in-visual-studio"></a>Visual Studio'da bir yerel değişken ekleme

Bu kod oluşturma için geçerlidir:

- C#

- Visual Basic

**Yazdırılacak** Varolan bir ifadeyi değiştirmek için hemen yerel bir değişken oluşturmanıza olanak sağlar.

**Oluşturulurken** Daha sonra yerel bir değişkense, daha sonra kolayca kullanılabilecek bir kodunuz var.

**Kaydol** Kodu çeşitli konumlarda kullanmak için birden çok kez kopyalayabilir ve yapıştırabilirsiniz, ancak işlemi bir kez gerçekleştirmek, sonucu yerel bir değişkende depolamak ve içinde yerel değişkeni kullanmak daha iyidir.

## <a name="how-to"></a>Nasıl Yapılır Konuları

1. Yeni bir yerel değişkene atamak istediğiniz ifade vurgulayın.

   - C# İÇİN:

       ![Vurgulanmış kodu C#](media/local-highlight-cs.png)

   - Visual Basic:

       ![Vurgulanmış kodu VB](media/local-highlight-vb.png)

2. Ardından, aşağıdakilerden birini yapın:

   - **Klavye**
      - Tuşuna **Ctrl**+ **.** Tetikleyici için **hızlı Eylemler ve yeniden düzenlemeler** menüsü.
   - **Fare**
      - Sağ tıklayıp **hızlı Eylemler ve yeniden düzenlemeler** menüsü.
      - &nbsp; ![Screwdriver](media/screwdriver.png) Sol kenar boşluğunda görüntülenen simge, metin imleç zaten vurgulanan ifade ile satırda varsa görüntülenir.

   ![Yerel Önizleme Ekle](media/local-preview-cs.png)

3. Açılan menüden **' expression ' için yerel (tüm oluşumlar) Ekle '** yi seçin.

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
---
title: Bir yöntem oluşturma
ms.date: 01/26/2018
ms.prod: visual-studio-dev15
ms.topic: reference
author: gewarren
ms.author: gewarren
manager: jillfra
ms.workload:
- dotnet
ms.openlocfilehash: 2c2de6f8608857d102454d03a98aacd175a22cef
ms.sourcegitcommit: 2193323efc608118e0ce6f6b2ff532f158245d56
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/25/2019
ms.locfileid: "55024948"
---
# <a name="generate-a-method-in-visual-studio"></a>Visual Studio'da bir yöntem oluşturma

Bu kod oluşturma için geçerlidir:

- C#

- Visual Basic

**Ne:** Hemen bir yöntem bir sınıfa eklemenizi sağlar.

**ne zaman:** Size yeni bir yöntem ve düzgün bir şekilde, otomatik olarak bildirir.

**Neden:** Ancak, bu özellik bildirimi otomatik olarak oluşturur, kullanmadan önce yöntem ve parametreler bildirebilirsiniz.

## <a name="how-to"></a>Nasıl Yapılır Konuları

1. İmlecinizi satıra Yerleştir kırmızı dalgalı olduğu. Kırmızı dalgalı çizgi henüz mevcut olmayan bir yöntemi gösterir.

   - C# İÇİN:

       ![Vurgulanmış kodu C#](media/method-highlight-cs.png)

   - Visual Basic:

       ![Vurgulanmış kodu VB](media/method-highlight-vb.png)

2. Ardından, aşağıdakilerden birini yapın:

   - **Klavye**
      - Tuşuna **Ctrl**+**.** Tetikleyici için **hızlı Eylemler ve yeniden düzenlemeler** menüsü.
   - **Fare**
      - Sağ tıklayıp **hızlı Eylemler ve yeniden düzenlemeler** menüsü.
      - Kırmızı dalgalı çizgi gelin ve tıklayın ![Ampul](media/bulb-cs.png) Bu simge görünür.
      - &nbsp; ![Ampul](media/bulb-cs.png) kırmızı dalgalı çizgi içeren satırda metin imleci ise sol kenar boşluğunda görünür simge.

      ![Önizleme yöntemi oluşturma](media/method-preview-cs.png)

3. Seçin **metodunu üret** aşağı açılan menüden.

   > [!TIP]
   > Kullanım **değişiklik önizlemesi** Önizleme pencerenin alt kısmındaki bağlantı [tüm değişiklikleri görmek için](../../ide/preview-changes.md) , oluşturulacak, seçim yapmadan önce.

   Yöntemi, kullanımdan çıkarılan herhangi bir parametre ile oluşturulur.

   - C# İÇİN:

       ![Yöntem sonuç C# oluştur](media/method-result-cs.png)

   - Visual Basic:

       ![Yöntem sonuç VB oluştur](media/method-result-vb.png)

## <a name="see-also"></a>Ayrıca bkz.

- [Kod Oluşturma](../code-generation-in-visual-studio.md)
- [Değişiklikleri Önizleme](../../ide/preview-changes.md)
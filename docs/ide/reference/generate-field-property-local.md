---
title: Alan, özellik, yerel değişken oluştur
ms.date: 01/26/2018
ms.prod: visual-studio-dev15
ms.topic: reference
author: gewarren
ms.author: gewarren
manager: jillfra
ms.workload:
- dotnet
ms.openlocfilehash: d3b22f32669023666451f1981cf9c6fdf6f251e6
ms.sourcegitcommit: e3d96b20381916bf4772f9db52b22275763bb603
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/31/2019
ms.locfileid: "55483607"
---
# <a name="generate-a-field-property-or-local-variable-in-visual-studio"></a>Visual Studio'da bir alan, özelliği veya yerel değişken oluştur

Bu kod oluşturma için geçerlidir:

- C#

- Visual Basic

**Ne:** Hemen önce bildirilmemiş alan, özelliği veya yerel kodu oluşturmanıza olanak sağlar.

**ne zaman:** Size yeni bir alan, özelliği veya yerel yazarken tanıtır ve düzgün bir şekilde, otomatik olarak bildirmek.

**Neden:** Alan, özelliği bildirip veya yerel kullanmadan önce ancak bu özellik bildirimi oluşturur ve otomatik olarak yazın.

## <a name="how-to"></a>Nasıl Yapılır Konuları

1. İmlecinizi satıra Yerleştir kırmızı dalgalı olduğu. Kırmızı dalgalı çizgi, alan, yerel veya henüz mevcut olmayan özellik gösterir.

   - C# İÇİN:

       ![Vurgulanmış kodu C#](media/field-highlight-cs.png)

   - Visual Basic:

       ![Vurgulanmış kodu VB](media/field-highlight-vb.png)

2. Ardından, aşağıdakilerden birini yapın:

   - **Klavye**
      - Tuşuna **Ctrl**+**.** Tetikleyici için **hızlı Eylemler ve yeniden düzenlemeler** menüsü.
   - **Fare**
      - Sağ tıklayıp **hızlı Eylemler ve yeniden düzenlemeler** menüsü.
      - Kırmızı dalgalı çizgi gelin ve tıklayın ![hata ampul](media/error-bulb.png) Bu simge görünür.
      - &nbsp; ![hata ampul](media/error-bulb.png) kırmızı dalgalı çizgi içeren satırda metin imleci ise sol kenar boşluğunda görünür simge.

      ![Alan/özellik/yerel Önizleme oluşturma](media/field-preview-cs.png)

3. Bir oluşturma seçenekleri, aşağı açılan menüden seçin.

   > [!TIP]
   > Kullanım **değişiklik önizlemesi** Önizleme pencerenin alt kısmındaki bağlantı [tüm değişiklikleri görmek için](../../ide/preview-changes.md) , oluşturulacak, seçim yapmadan önce.

   Alan, özelliği veya yerel, kullanımdan çıkarılan türü ile oluşturulur.

   - C# İÇİN:

       ![Yöntem sonuç C# oluştur](media/field-result-cs.png)

   - Visual Basic:

       ![Yöntem sonuç VB oluştur](media/field-result-vb.png)

## <a name="see-also"></a>Ayrıca bkz.

- [Kod Oluşturma](../code-generation-in-visual-studio.md)
- [Değişiklikleri Önizleme](../../ide/preview-changes.md)
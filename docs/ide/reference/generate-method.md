---
title: Visual Studio'da bir yöntem oluşturma
ms.date: 01/26/2018
ms.prod: visual-studio-dev15
ms.technology: vs-ide-general
ms.topic: reference
author: gewarren
ms.author: gewarren
manager: douge
ms.workload:
- dotnet
ms.openlocfilehash: 7d6d7d17810e53de80bfecff697e960613dc06a6
ms.sourcegitcommit: 0a8ac5f2a685270d9ca79bb39d26fd90099bfa29
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 11/09/2018
ms.locfileid: "51295858"
---
# <a name="generate-a-method-in-visual-studio"></a>Visual Studio'da bir yöntem oluşturma

Bu kod oluşturma için geçerlidir:

- C#

- Visual Basic

**Ne:** hemen bir yöntem bir sınıfa eklemenizi sağlar.

**Ne zaman:** yeni bir yöntem ve düzgün bir şekilde, otomatik olarak bildirmek istiyor.

**Neden:** ancak bu özellik bildirimi otomatik olarak oluşturur, yöntemi ve parametreleri, kullanmadan önce bildirebilirsiniz.

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
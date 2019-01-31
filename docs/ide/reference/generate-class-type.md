---
title: Sınıf veya tür oluşturma
ms.date: 01/26/2018
ms.prod: visual-studio-dev15
ms.topic: reference
author: gewarren
ms.author: gewarren
manager: jillfra
f1_keywords:
- vsl.GenerateFromUsage
dev_langs:
- CSharp
- VB
ms.workload:
- dotnet
ms.openlocfilehash: 167c4380f67a51d3e03f2e4241c0c384781ddb43
ms.sourcegitcommit: e3d96b20381916bf4772f9db52b22275763bb603
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/31/2019
ms.locfileid: "55483945"
---
# <a name="generate-a-class-or-type-in-visual-studio"></a>Visual Studio'da bir sınıf veya tür oluşturun

Bu kod oluşturma için geçerlidir:

- C#

- Visual Basic

**Ne:** Hemen bir sınıf veya tür için kod oluşturmanıza olanak sağlar.

**ne zaman:** Size yeni bir sınıf veya tür sunmak ve düzgün bir şekilde, otomatik olarak bildirir.

**Neden:** Ancak, bu özellik sınıfı oluşturun veya otomatik olarak yazın, kullanmadan önce sınıf veya tür bildirebilirsiniz.

## <a name="how-to"></a>Nasıl Yapılır Konuları

1. İmlecinizi satıra Yerleştir kırmızı dalgalı olduğu. Kırmızı dalgalı çizgi henüz mevcut olmayan bir sınıfı gösterir.

   - C# İÇİN:

       ![Vurgulanmış kodu C#](media/class-highlight-cs.png)

   - Visual Basic:

       ![Vurgulanmış kodu VB](media/class-highlight-vb.png)

2. Ardından, aşağıdakilerden birini yapın:

   - **Klavye**
      - Tuşuna **Ctrl**+**.** Tetikleyici için **hızlı Eylemler ve yeniden düzenlemeler** menüsü.
   - **Fare**
      - Sağ tıklayıp **hızlı Eylemler ve yeniden düzenlemeler** menüsü.
      - Kırmızı dalgalı çizgi gelin ve tıklayın ![hata ampul](media/error-bulb.png) Bu simge görünür.
      - &nbsp; ![hata ampul](media/error-bulb.png) kırmızı dalgalı çizgi içeren satırda metin imleci ise sol kenar boşluğunda görünür simge.

      ![Sınıf Önizleme oluşturma](media/class-preview-cs.png)

3. Aşağı açılan menüden seçeneklerden birini belirleyin:

   - Sınıf*TypeName*' yeni dosyasında&mdash;adlı bir sınıf oluşturur *TypeName* adındaki bir dosyaya *TypeName*.cs/.vb
   - Sınıf*TypeName*'&mdash;adlı bir sınıf oluşturur *TypeName* geçerli dosyadaki.
   - İç içe geçmiş sınıf*TypeName*'&mdash;adlı bir sınıf oluşturur *TypeName* geçerli sınıf içinde iç içe geçmiş.
   - Yeni tür üret... &mdash;Yeni bir sınıf veya yapının tüm belirttiğiniz özelliklerini oluşturur.

   > [!TIP]
   > Kullanım **değişiklik önizlemesi** Önizleme pencerenin alt kısmındaki bağlantı [tüm değişiklikleri görmek için](../../ide/preview-changes.md) , oluşturulacak, seçim yapmadan önce.

4. Seçtiyseniz **yeni tür oluşturma** öğesini **oluşturma türü** iletişim kutusu açılır. Erişilebilirlik, tür ve yeni türü konumunu yapılandırın.

   ![Tür oluşturma](media/class-newtype-cs.png)

   Seçim | Açıklama
   --- | ---
   Access | Türü için ayarlanmış *varsayılan*, *dahili* veya *genel* erişim.
   tür | Bu, olarak ayarlanabilir *sınıfı* veya *yapı*.
   Ad | Bu değiştirilemez ve yazdığınız adı olacaktır.
   Proje | Çözümünüz içinde birden çok proje varsa Canlı sınıf/yapı istediğiniz seçebilirsiniz.
   Dosya Adı | Yeni bir dosya oluşturabilir veya varolan bir dosyaya türü ekleyebilirsiniz.

Sınıfın veya yapının oluşturulur. İçin C#, bir yapıcı da oluşturulur.

- C#

   ![Sınıf sonucu oluşturC#](media/class-result-cs.png)

- Visual Basic

   ![VB sınıf sonucu oluştur](media/class-result-vb.png)

## <a name="see-also"></a>Ayrıca bkz.

- [Kod Oluşturma](../code-generation-in-visual-studio.md)
- [Değişiklikleri Önizleme](../../ide/preview-changes.md)
---
title: Oluşturma C# Equals ve GetHashCode metot geçersiz kılmaları
ms.date: 01/26/2018
ms.prod: visual-studio-dev15
ms.topic: reference
author: gewarren
ms.author: gewarren
manager: jillfra
ms.workload:
- dotnet
ms.openlocfilehash: d56a8f94665e20f8ca89b5a682eb6e44602bde0f
ms.sourcegitcommit: 2193323efc608118e0ce6f6b2ff532f158245d56
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/25/2019
ms.locfileid: "54983748"
---
# <a name="generate-equals-and-gethashcode-method-overrides-in-visual-studio"></a>Equals ve oluşturma Visual Studio'da GetHashCode metot geçersiz kılmaları

Bu kod oluşturma için geçerlidir:

- C#

**Ne:** Oluşturmanıza olanak tanır **eşittir** ve **GetHashCode** yöntemleri.

**ne zaman:** Bir veya daha fazla alanlara göre yerine bellekteki nesne konuma göre karşılaştırılması gereken bir türüne sahip olduğunda bu geçersiz kılmaları oluşturur.

**Neden:**

- Bir değer türü uyguluyorsanız, geçersiz kılma düşünmelisiniz **eşittir** ValueType Equals yöntemini varsayılan uygulaması üzerinde yüksek performans elde etmek için yöntemi.

- Bir başvuru türü uyguluyorsanız, geçersiz kılma düşünmelisiniz **eşittir** türünüz noktası, dize, BigNumber ve benzeri gibi bir temel tür gibi görünüyorsa yöntemi.

- Geçersiz kılma **GetHashCode** bir karma tablosunda düzgün çalışması için bir tür izin vermek için yöntemi. Daha fazla rehberliğe okumaya [eşitlik işleçleri](/dotnet/standard/design-guidelines/equality-operators).

## <a name="how-to"></a>Nasıl Yapılır Konuları

1. İmlecinizi, tür bildirimi satırında yere yerleştirin.

   ![Vurgulanmış kodu](media/overrides-highlight-cs.png)

   > [!TIP]
   > Yapmak değil çift tür adı seçin veya menü seçeneği kullanılamaz. Yeni imleç yere satıra yerleştirin.

1. Ardından, aşağıdakilerden birini yapın:

   - Tuşuna **Ctrl**+**.** Tetikleyici için **hızlı Eylemler ve yeniden düzenlemeler** menüsü.

   - Sağ tıklayıp **hızlı Eylemler ve yeniden düzenlemeler** menüsü.

   - &nbsp; ![Tornavida](../media/screwdriver-icon.png) Sol kenar boşluğunda görünür simge.

   ![Geçersiz kılmalar Önizleme oluşturma](media/overrides-preview-cs.png)

1. Seçin **Equals(object) Oluştur** veya **oluşturmak Equals ve GetHashCode** aşağı açılan menüden.

1. İçinde **üyeleri çekme** istediğiniz üye oluşturmak için yöntemleri iletişim kutusunda:

    ![Geçersiz kılmalar iletişim oluştur](media/overrides-dialog-cs.png)

    > [!TIP]
    > İletişim kutusunun alt kısmındaki onay kutusunu kullanarak bu iletişim kutusundan işleçleri oluşturulacak seçebilirsiniz.

   `Equals` Ve `GetHashCode` yöntemleri varsayılan uygulamaları ile oluşturulur.

   ![Metot oluştur](media/overrides-result-cs.png)

## <a name="see-also"></a>Ayrıca bkz.

- [Kod Oluşturma](../code-generation-in-visual-studio.md)
- [Değişiklikleri Önizleme](../../ide/preview-changes.md)
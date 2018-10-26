---
title: Visual Studio'da C# Equals ve GetHashCode metot geçersiz kılmaları oluşturma
ms.date: 01/26/2018
ms.prod: visual-studio-dev15
ms.technology: vs-ide-general
ms.topic: reference
author: gewarren
ms.author: gewarren
manager: douge
ms.workload:
- dotnet
ms.openlocfilehash: 9af687eb4b39afdbe9fd34df1aa03f18ce243ef8
ms.sourcegitcommit: 240c8b34e80952d00e90c52dcb1a077b9aff47f6
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/23/2018
ms.locfileid: "49903120"
---
# <a name="generate-equals-and-gethashcode-method-overrides-in-visual-studio"></a>Equals ve oluşturma Visual Studio'da GetHashCode metot geçersiz kılmaları

Bu kod oluşturma için geçerlidir:

- C#

**Ne:** oluşturmanıza olanak tanır **eşittir** ve **GetHashCode** yöntemleri.

**Ne zaman:** bir veya daha fazla alanlara göre yerine bellekteki nesne konuma göre karşılaştırılması gereken bir tür olduğunda, bu geçersiz kılmaları oluştur.

**Neden:**

- Bir değer türü uyguluyorsanız, geçersiz kılma düşünmelisiniz **eşittir** ValueType Equals yöntemini varsayılan uygulaması üzerinde yüksek performans elde etmek için yöntemi.

- Bir başvuru türü uyguluyorsanız, geçersiz kılma düşünmelisiniz **eşittir** türünüz noktası, dize, BigNumber ve benzeri gibi bir temel tür gibi görünüyorsa yöntemi.

- Geçersiz kılma **GetHashCode** bir karma tablosunda düzgün çalışması için bir tür izin vermek için yöntemi. Daha fazla rehberliğe okumaya [eşitlik işleçleri](/dotnet/standard/design-guidelines/equality-operators).

## <a name="how-to"></a>Nasıl Yapılır Konuları

1. İmlecinizi, tür bildiriminde yerleştirin.

   ![Vurgulanmış kodu](media/overrides-highlight-cs.png)

1. Ardından, aşağıdakilerden birini yapın:

   - **Klavye**
      - Tuşuna **Ctrl**+**.** Tetikleyici için **hızlı Eylemler ve yeniden düzenlemeler** menüsü.
   - **Fare**
      - Sağ tıklayıp **hızlı Eylemler ve yeniden düzenlemeler** menüsü.
      - &nbsp; ![Ampul](media/bulb-cs.png) tür bildirimi içeren satırda metin imleci ise, sol kenar boşluğunda görünür simge.

   ![Geçersiz kılmalar Önizleme oluşturma](media/overrides-preview-cs.png)

1. Seçin **Equals(object) Oluştur** veya **oluşturmak Equals ve GetHashCode** aşağı açılan menüden.

1. İçinde **üyeleri çekme** istediğiniz üye oluşturmak için yöntemleri iletişim kutusunda:

    ![Geçersiz kılmalar iletişim oluştur](media/overrides-dialog-cs.png)

    > [!TIP]
    > Üye listesi altındaki onay kutularını kullanarak bu iletişim kutusundan işleçleri oluşturulacak seçebilirsiniz.

   Equals ve GetHashCode geçersiz kılmalar, varsayılan uygulamaları ile oluşturulur.

   ![Metot oluştur](media/overrides-result-cs.png)

## <a name="see-also"></a>Ayrıca bkz.

- [Kod Oluşturma](../code-generation-in-visual-studio.md)
- [Değişiklikleri Önizleme](../../ide/preview-changes.md)
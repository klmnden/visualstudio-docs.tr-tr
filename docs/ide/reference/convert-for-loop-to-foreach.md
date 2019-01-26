---
title: Dönüştürme kodu yeniden düzenleme bir for döngüsü foreach deyimi
ms.date: 05/10/2018
ms.prod: visual-studio-dev15
ms.topic: reference
author: gewarren
ms.author: gewarren
manager: jillfra
dev_langs:
- CSharp
ms.workload:
- dotnet
ms.openlocfilehash: 16b4a2d4c6f80c2c38b659a54c3d631124754644
ms.sourcegitcommit: 2193323efc608118e0ce6f6b2ff532f158245d56
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/25/2019
ms.locfileid: "54936560"
---
# <a name="refactoring-to-convert-between-a-for-loop-and-a-foreach-statement"></a>Yeniden düzenleme arasında dönüştürmek için bir döngü için ve bir foreach deyimi

Bu makalede iki döngü yapıları arasında dönüştürme hızlı Eylemler yeniden düzenlemeler. Neden isteyebilirsiniz arasında geçiş yapmak için bazı nedenler içeren bir [için](/dotnet/csharp/language-reference/keywords/for) döngü ve [foreach](/dotnet/csharp/language-reference/keywords/foreach-in) kodunuzda deyimi.

## <a name="convert-a-for-loop-to-a-foreach-statement"></a>Dönüştürme bir for döngüsü foreach deyimi

Varsa bir [için](/dotnet/csharp/language-reference/keywords/for) döngü kodunuzda bu yeniden düzenleme öğesine dönüştürmek için kullanabileceğiniz bir [foreach](/dotnet/csharp/language-reference/keywords/foreach-in) deyimi.

Bu yeniden düzenleme için geçerlidir:

- C#

> [!NOTE]
> **Dönüştürmek için foreach** hızlı eylem yeniden düzenleme, yalnızca kullanılabilir [için](/dotnet/csharp/language-reference/keywords/for) döngüleri, tüm üç parça içerir: bir başlatıcı, koşul ve yineleyici.

### <a name="why-convert"></a>Neden Dönüştür

Neden dönüştürmek istediğiniz bir [için](/dotnet/csharp/language-reference/keywords/for) döngüsü bir [foreach](/dotnet/csharp/language-reference/keywords/foreach-in) deyimi içerir:

- Öğelere erişmek için bir dizin olarak dışında döngü içinde yerel bir döngü değişkeninin kullanmayın.

- Kodunuzu basitleştirin ve Başlatıcı, koşul ve yineleyici bölümleri mantık hataları olasılığını azaltmak istediğiniz.

### <a name="how-to-use-it"></a>Kullanımı

1. İçinde giriş işareti koyun `for` anahtar sözcüğü.

1. Tuşuna **Ctrl**+**.** veya tornavida ![tornavida simgesi](../media/screwdriver-icon.png) kod dosyasının boşluğundaki simgeye.

   ![Foreach menüye dönüştürme](media/convert-to-foreach.png)

1. Seçin **'foreach' olarak Dönüştür**. Ya da seçin **değişiklik önizlemesi** açmak için [Değişiklikleri Önizle](../../ide/preview-changes.md) iletişim tıklayın ve ardından **Uygula**.

## <a name="convert-a-foreach-statement-to-a-for-loop"></a>Foreach deyimi için dönüştürme bir for döngüsü

Varsa bir [foreach (C#)](/dotnet/csharp/language-reference/keywords/foreach-in) veya [her biri için... İleri (Visual Basic)](/dotnet/visual-basic/language-reference/statements/for-each-next-statement) deyim, kodunuzda kullanabileceğiniz bu yeniden düzenleme öğesine dönüştürmek için bir [için](/dotnet/csharp/language-reference/keywords/for) döngü.

Bu yeniden düzenleme için geçerlidir:

- C#

- Visual Basic

### <a name="why-convert"></a>Neden Dönüştür

Neden dönüştürmek istediğiniz bir [foreach](/dotnet/csharp/language-reference/keywords/foreach-in) deyimi bir [için](/dotnet/csharp/language-reference/keywords/for) döngü içerir:

- Öğe daha fazlasına erişmek için yerel Döngü değişkeninin döngü içinde kullanmak istiyorsunuz.

- İşiniz [çok boyutlu bir dizi boyunca gezinme](/dotnet/csharp/programming-guide/arrays/using-foreach-with-arrays) ve dizi öğeleri üzerinde daha fazla denetim istiyorsanız.

### <a name="how-to-use-it"></a>Kullanımı

1. İçinde giriş işareti koyun `foreach` veya `For Each` anahtar sözcüğü.

1. Tuşuna **Ctrl**+**.** veya tornavida ![tornavida simgesi](../media/screwdriver-icon.png) kod dosyasının boşluğundaki simgeye.

   ![Menüsünü Dönüştür](media/convert-to-for.png)

1. Seçin **'for' olarak Dönüştür**. Ya da seçin **değişiklik önizlemesi** açmak için [Değişiklikleri Önizle](../../ide/preview-changes.md) iletişim tıklayın ve ardından **Uygula**.

1. Yeniden düzenleme, yeni bir yineleme sayısı değişken oluşturduğundan **Yeniden Adlandır** kutusu Düzenleyicisinin sağ üst köşesinde görüntülenir. Değişken için farklı bir ad seçmek istiyorsanız, yazın ve sonra basın **Enter** veya **Uygula** içinde **Yeniden Adlandır** kutusu. Yeni bir ad seçin istemiyorsanız basın **Esc** veya **Uygula** kapatmak için **Yeniden Adlandır** kutusu.

> [!NOTE]
> İçin C#, bu yeniden düzenlemeler tarafından oluşturulan kodu açık bir tür kullanan veya [var](/dotnet/csharp/language-reference/keywords/var) koleksiyondaki öğelerin türü. Kapsam içinde kod stili ayarları türü oluşturulan kodda, doğrudan veya dolaylı bağlıdır. Bu belirli kod stili ayarları altında makine düzeyinde yapılandırılır **Araçları** > **seçenekleri** > **metin düzenleyici**  >  **C#**  >  **Kod stili** > **genel** > **\'var' Tercihler**, ya da çözüm düzeyinde bir [EditorConfig](../../ide/editorconfig-code-style-settings-reference.md#implicit-and-explicit-types) dosya. Kod stili ayarı değiştirirseniz **seçenekleri**, değişikliklerin etkili olabilmesi için kod dosyasını açın.

## <a name="see-also"></a>Ayrıca bkz.

- [Yeniden Düzenleme](../refactoring-in-visual-studio.md)
- [Değişiklikleri Önizleme](../../ide/preview-changes.md)
---
title: LINQ sorgusu için foreach deyimi dönüştürmek için kodu yeniden düzenleyin
ms.date: 05/15/2018
ms.topic: reference
author: gewarren
ms.author: gewarren
manager: jillfra
dev_langs:
- CSharp
ms.workload:
- dotnet
ms.openlocfilehash: 237c6215971cbbac5dec25fd81c995cf87ed57c6
ms.sourcegitcommit: b468d71052a1b8a697f477ab23a3644de139f1e9
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/19/2019
ms.locfileid: "67261730"
---
# <a name="refactoring-to-convert-linq-to-a-foreach-statement"></a>Foreach deyimi için LINQ dönüştürmek için yeniden düzenleme

Bu yeniden düzenleme dönüştürmek için kullanma [LINQ Sorgu söz dizimi](/dotnet/csharp/programming-guide/concepts/linq/query-syntax-and-method-syntax-in-linq) için bir [foreach](/dotnet/csharp/language-reference/keywords/foreach-in) deyimi.

Bu yeniden düzenleme için geçerlidir:

- C#

## <a name="how-to-use-it"></a>Kullanımı

1. Tüm LINQ Sorgu başlayarak seçin `from`.

   > [!NOTE]
   > Bu yeniden düzenleme yalnızca sorgu sözdizimi ve yöntem sözdizimi ile ifade edilen LINQ sorguları dönüştürmek için kullanılabilir.

1. Tuşuna **Ctrl**+ **.** veya tornavida ![tornavida simgesi](../media/screwdriver-icon.png) kod dosyasının boşluğundaki simgeye.

   ![Foreach hızlı Eylemler menüsüne LINQ Dönüştür](media/convert-linq-to-foreach.png)

1. Seçin **'foreach' olarak Dönüştür**. Ya da seçin **değişiklik önizlemesi** açmak için [Değişiklikleri Önizle](../../ide/preview-changes.md) iletişim tıklayın ve ardından **Uygula**.

> [!NOTE]
> İçin C#, bu yeniden düzenlemeler tarafından oluşturulan kodu açık bir tür kullanan veya [var](/dotnet/csharp/language-reference/keywords/var) yineleme değişkeni için `foreach` döngü. Kapsam içinde kod stili ayarları türü oluşturulan kodda, doğrudan veya dolaylı bağlıdır. Bu belirli kod stili ayarları altında makine düzeyinde yapılandırılır **Araçları** > **seçenekleri** > **metin düzenleyici**  >  **C#**  >  **Kod stili** > **genel** >  **\'var' Tercihler**, ya da çözüm düzeyinde bir [EditorConfig](../../ide/editorconfig-language-conventions.md#implicit-and-explicit-types) dosya. Kod stili ayarı değiştirirseniz **seçenekleri**, değişikliklerin etkili olabilmesi için kod dosyasını açın.

## <a name="see-also"></a>Ayrıca bkz.

- [LINQ](/dotnet/standard/using-linq)
- [Yeniden Düzenleme](../refactoring-in-visual-studio.md)
- [Değişiklikleri Önizleme](../../ide/preview-changes.md)
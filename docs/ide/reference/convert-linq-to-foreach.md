---
title: LINQ sorgusu için foreach deyimi dönüştürmek için kodu yeniden düzenleyin
ms.date: 05/15/2018
ms.prod: visual-studio-dev15
ms.topic: reference
author: gewarren
ms.author: gewarren
manager: douge
dev_langs:
- CSharp
ms.workload:
- dotnet
ms.openlocfilehash: 23b8446b0fa44cccc3ae18ad789fd5b45e514033
ms.sourcegitcommit: 37fb7075b0a65d2add3b137a5230767aa3266c74
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/02/2019
ms.locfileid: "53937302"
---
# <a name="refactoring-to-convert-linq-to-a-foreach-statement"></a>Foreach deyimi için LINQ dönüştürmek için yeniden düzenleme

Bu yeniden düzenleme dönüştürmek için kullanma [LINQ Sorgu söz dizimi](/dotnet/csharp/programming-guide/concepts/linq/query-syntax-and-method-syntax-in-linq) için bir [foreach](/dotnet/csharp/language-reference/keywords/foreach-in) deyimi.

Bu yeniden düzenleme için geçerlidir:

- C#

## <a name="how-to-use-it"></a>Kullanımı

1. Tüm LINQ Sorgu başlayarak seçin `from`.

   > [!NOTE]
   > Bu yeniden düzenleme yalnızca sorgu sözdizimi ve yöntem sözdizimi ile ifade edilen LINQ sorguları dönüştürmek için kullanılabilir.

1. Tuşuna **Ctrl**+**.** veya tornavida ![tornavida simgesi](../media/screwdriver-icon.png) kod dosyasının boşluğundaki simgeye.

   ![Foreach hızlı Eylemler menüsüne LINQ Dönüştür](media/convert-linq-to-foreach.png)

1. Seçin **'foreach' olarak Dönüştür**. Ya da seçin **değişiklik önizlemesi** açmak için [Değişiklikleri Önizle](../../ide/preview-changes.md) iletişim tıklayın ve ardından **Uygula**.

> [!NOTE]
> İçin C#, bu yeniden düzenlemeler tarafından oluşturulan kodu açık bir tür kullanan veya [var](/dotnet/csharp/language-reference/keywords/var) yineleme değişkeni için `foreach` döngü. Kapsam içinde kod stili ayarları türü oluşturulan kodda, doğrudan veya dolaylı bağlıdır. Bu belirli kod stili ayarları altında makine düzeyinde yapılandırılır **Araçları** > **seçenekleri** > **metin düzenleyici**  >  **C#**  >  **Kod stili** > **genel** > **\'var' Tercihler**, ya da çözüm düzeyinde bir [EditorConfig](../../ide/editorconfig-code-style-settings-reference.md#implicit-and-explicit-types) dosya. Kod stili ayarı değiştirirseniz **seçenekleri**, değişikliklerin etkili olabilmesi için kod dosyasını açın.

## <a name="see-also"></a>Ayrıca bkz.

- [LINQ](/dotnet/standard/using-linq)
- [Yeniden Düzenleme](../refactoring-in-visual-studio.md)
- [Değişiklikleri Önizleme](../../ide/preview-changes.md)
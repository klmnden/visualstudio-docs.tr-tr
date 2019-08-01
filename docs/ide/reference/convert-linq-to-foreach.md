---
title: LINQ sorgusunu foreach ifadesine dönüştürmek için kodu yeniden düzenleme
description: Sorgu sözdiziminde yazılmış herhangi bir LINQ sorgusunu foreach ifadesine Dönüştür.
ms.date: 05/15/2018
ms.topic: reference
author: gewarren
ms.author: gewarren
manager: jillfra
dev_langs:
- CSharp
ms.workload:
- dotnet
ms.openlocfilehash: 446d0f3a4988552e8e1fbbac32ca150491975d94
ms.sourcegitcommit: 0f5f7955076238742f2071d286ad8e896f3a6cad
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/25/2019
ms.locfileid: "68483683"
---
# <a name="refactoring-to-convert-linq-to-a-foreach-statement"></a>LINQ öğesini foreach ifadesine dönüştürmek için yeniden düzenleme

[LINQ sorgu söz dizimini](/dotnet/csharp/programming-guide/concepts/linq/query-syntax-and-method-syntax-in-linq) [foreach](/dotnet/csharp/language-reference/keywords/foreach-in) ifadesine dönüştürmek için bu yeniden düzenlemeyi kullanın.

Bu yeniden düzenleme için geçerlidir:

- C#

## <a name="how-to-use-it"></a>Kullanımı

1. İle `from`başlayan LINQ sorgusunun tamamını seçin.

   > [!NOTE]
   > Bu yeniden düzenleme, yalnızca sorgu söz dizimi ile ifade edilen LINQ sorgularını dönüştürmek için kullanılabilir ve Yöntem sözdizimi değildir.

1. Tuşuna **Ctrl**+ **.** ya da kod dosyasının kenar boşluğundaki ![screwdriver screwdriver simge](../media/screwdriver-icon.png) simgesine tıklayın.

   ![LINQ to foreach hızlı eylemler menüsünü Dönüştür](media/convert-linq-to-foreach.png)

1. **' Foreach ' olarak Dönüştür**' ü seçin. Ya da değişiklikleri [Önizle iletişim kutusunu](../../ide/preview-changes.md) açmak Için **Değişiklikleri Önizle** ' yi seçin ve ardından **Uygula**' yı seçin.

> [!NOTE]
> İçin C#, bu yeniden düzenlemeler tarafından oluşturulan kod, `foreach` döngünün yineleme değişkeni için açık bir tür ya da [var](/dotnet/csharp/language-reference/keywords/var) kullanır. Oluşturulan koddaki tür açık veya örtük, kapsamdaki kod stili ayarlarına bağlıdır. Bu özel kod stili ayarları, **Araçlar** > **Seçenekler** > **metin Düzenleyicisi** > **C#**  > **kod** stilialtında >  makine düzeyinde yapılandırılır **Genel** var ' tercihleri veya bir [editorconfig](../../ide/editorconfig-language-conventions.md#implicit-and-explicit-types) dosyasındaki çözüm düzeyinde.  **\'**  >  **Seçenekler**' de bir kod stili ayarını değiştirirseniz değişikliklerin etkili olması için kod dosyasını yeniden açın.

## <a name="see-also"></a>Ayrıca bkz.

- [LINQ](/dotnet/standard/using-linq)
- [Yeniden Düzenleme](../refactoring-in-visual-studio.md)
- [Değişiklikleri Önizleme](../../ide/preview-changes.md)
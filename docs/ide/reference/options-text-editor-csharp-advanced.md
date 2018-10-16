---
title: Seçenekler, Metin Düzenleyici, C#, Gelişmiş
ms.date: 11/04/2016
ms.prod: visual-studio-dev15
ms.technology: vs-ide-general
ms.topic: reference
f1_keywords:
- VS.ToolsOptionsPages.Text_Editor.CSharp.Outlining
- VS.ToolsOptionsPages.Text_Editor.CSharp.Advanced
author: gewarren
ms.author: gewarren
manager: douge
ms.workload:
- dotnet
ms.openlocfilehash: 16c92111fc29071447d4af5e736b881fa7c7a769
ms.sourcegitcommit: e680e8ac675f003ebcc8f8c86e27f54ff38da662
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/16/2018
ms.locfileid: "49356749"
---
# <a name="options-text-editor-c-advanced"></a>Seçenekler, Metin Düzenleyici, C#, Gelişmiş

Kullanım **Gelişmiş** Düzenleyici biçimlendirme ayarlarını değiştirmek, yeniden düzenleme kod, Seçenekler sayfası ve XML belge açıklamaları için C#. Bu seçenekler sayfası erişmek için kendi seçtikleri **Araçları** > **seçenekleri**ve ardından **metin düzenleyici** > **C#**  >  **Gelişmiş**.

> [!NOTE]
> Tüm seçenekler burada listelenir.

## <a name="analysis"></a>Çözümleme

- Tam çözüm analizini etkinleştirme

   Çözümdeki tüm dosyalarda etkinleştirir kod analizi, yalnızca kod dosyaları açın. Daha fazla bilgi için [tam çözüm analizini](../../code-quality/how-to-enable-and-disable-full-solution-analysis-for-managed-code.md).

## <a name="using-directives"></a>Using yönergeleri

- Using deyimlerini sıralarken önce 'System' yönergelerini Yerleştir

   Bu onay kutusu seçildiğinde, **kullanımları Kaldır ve Sırala** sağ tıklama menüsünde sıralar komutunu `using` yönergeleri ve yerler listenin üst kısmındaki 'System' ad alanları

   Sıralamadan önce:

   ```csharp
   using AutoMapper;
   using FluentValidation;
   using System.Collections.Generic;
   using System.Linq;
   using Newtonsoft.Json;
   using System;
   ```
   
   Sıraladıktan sonra:

   ```csharp
   using System;
   using System.Collections.Generic;
   using System.Linq;
   using AutoMapper;
   using FluentValidation;
   using Newtonsoft.Json;
   ```
   
- Yönerge gruplarını kullanarak Ayır

   Bu onay kutusu seçildiğinde, **kullanımları Kaldır ve Sırala** sağ tıklama menüsünü komutta ayıran `using` aynı kök ad alanına sahip yönergeleri grupları arasında boş bir satıra ekleyerek yönergeleri.

   Sıralamadan önce:

   ```csharp
   using AutoMapper;
   using FluentValidation;
   using System.Collections.Generic;
   using System.Linq;
   using Newtonsoft.Json;
   using System;
   ```
   
   Sıraladıktan sonra:
   
   ```csharp
   using AutoMapper;
   
   using FluentValidation;
   
   using Newtonsoft.Json;
   
   using System;
   using System.Collections.Generic;
   using System.Linq;
   ```
   
- Başvuru bütünleştirilmiş kodları ve NuGet paketleri içinde türler için using ekleme 

   Seçili olduğunda, bir [hızlı eylem](../quick-actions.md) NuGet paketini yüklemek ve eklemek kullanılabilir bir `using` başvurulmayan türleri için yönerge.

   ![Visual Studio'da NuGet paketini yüklemek için hızlı eylem](media/nuget-lightbulb.png)
  
## <a name="highlighting"></a>Vurgulama

- İmlecin altındaki sembole başvuruları Vurgula

   İmleç bir sembol içinde konumlandırıldığında veya sembol tıkladığınızda, kod dosyasındaki o simgenin tüm örnekleri vurgulanır.

## <a name="outlining"></a>Anahat Oluşturma

- Dosyalar açıldığında anahat moduna gir

   Bu onay kutusu seçildiğinde, otomatik olarak daraltılabilir kod bloklarını oluşturan kod dosyası özetlenmektedir. Bir dosya açıldığında, ilk kez #regions blokları ve etkin olmayan kod blokları daraltır.

## <a name="editor-help"></a>Düzenleyici Yardımı

- / / / İçin XML belge açıklamaları oluşturma

   Yazdıktan sonra bu onay kutusu seçildiğinde, XML belge açıklamaları için XML öğeleri ekler `///` yorum giriş. XML belgeleri hakkında daha fazla bilgi için bkz. [XML belgeleri yorumları (C# programlama Kılavuzu)](/dotnet/csharp/programming-guide/xmldoc/xml-documentation-comments).

## <a name="see-also"></a>Ayrıca bkz.

- [Nasıl yapılır: INSERT belgeleri oluşturmak için XML açıklamaları](../../ide/reference/generate-xml-documentation-comments.md)
- [XML belgeleri yorumları (C# programlama Kılavuzu)](/dotnet/csharp/programming-guide/xmldoc/xml-documentation-comments)
- [XML açıklamaları (C# Kılavuzu) ile kodunuzu belgeleme](/dotnet/csharp/codedoc)
- [Dile özgü düzenleyici seçeneklerini ayarlama](../../ide/reference/setting-language-specific-editor-options.md)
- [C# IntelliSense](../../ide/visual-csharp-intellisense.md)

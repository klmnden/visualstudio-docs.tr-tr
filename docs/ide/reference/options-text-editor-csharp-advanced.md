---
title: Seçenekler, Metin Düzenleyici, C#, Gelişmiş
ms.date: 01/16/2019
ms.topic: reference
f1_keywords:
- VS.ToolsOptionsPages.Text_Editor.CSharp.Outlining
- VS.ToolsOptionsPages.Text_Editor.CSharp.Advanced
author: gewarren
ms.author: gewarren
manager: jillfra
ms.workload:
- dotnet
ms.openlocfilehash: 010f2a2e6dc163f24a29e8e352b21d8ef8d72b48
ms.sourcegitcommit: 21d667104199c2493accec20c2388cf674b195c3
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/08/2019
ms.locfileid: "55927522"
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

   Bu onay kutusu seçildiğinde, **kullanımları Kaldır ve Sırala** sağ tıklama menüsünde sıralar komutunu `using` yönergeleri ve yerde listenin üst kısmındaki 'System' ad.

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

- Reference bütünleştirilmiş kodlarında türler için using Öner
- NuGet paketlerinde türler için using Öner

   Bu seçenek seçildiğinde, bir [hızlı eylem](../quick-actions.md) NuGet paketini yüklemek ve eklemek kullanılabilir bir `using` başvurulmayan türleri için yönerge.

   ![Visual Studio'da NuGet paketini yüklemek için hızlı eylem](media/nuget-lightbulb.png)

## <a name="highlighting"></a>Vurgulama

- İmlecin altındaki sembole başvuruları Vurgula

   İmleç bir sembol içinde konumlandırıldığında veya sembol tıkladığınızda, kod dosyasındaki o simgenin tüm örnekleri vurgulanır.

## <a name="outlining"></a>Anahat Oluşturma

- Dosyalar açıldığında anahat moduna gir

   Bu onay kutusu seçildiğinde, otomatik olarak daraltılabilir kod bloklarını oluşturan kod dosyası özetlenmektedir. Bir dosya açıldığında, ilk kez #regions blokları ve etkin olmayan kod blokları daraltır.

- Yordam satır ayıraçlarını Göster

   Metin düzenleyici, yordamların görsel kapsamını belirtir. Bir çizgi çizilir *.cs* konumlarda projenizin kaynak dosyaları aşağıdaki tabloda listelenen:

   |.Cs kaynak dosya konumu|Satır konumu örneği|
   |---------------------------------|------------------------------|
   |Sonra bir blok bildirimi yapısı kapatma|-Sonunda sınıfı, yapısı, modülü, arabirim veya numaralandırma<br />-Özelliği, işlev veya alt after<br />-Get ve set değil arasında bir özellikte yan tümceleri|
   |Tek satır yapıları bir dizi sonra|-İçeri aktarma deyimlerini after, önce bir sınıf dosyası içinde bir tür tanımı<br />-Bir sınıftaki tüm yordamları önce tanımlanan değişkenleri after|
   |Tek satır bildirimlerinden sonra (blok düzey bildirimleri)|-İçeri aktarma deyimlerini aşağıdaki deyimleri, değişken bildirimleri, olay bildirimleri, temsilci bildirimleri devralır ve DLL ifadeleri bildirme|

## <a name="block-structure-guides"></a>Blok yapısı kılavuzları

Süslü ayraçlar arasında noktalı dikey çizgileri görüntülemek için bu onay kutularını seçin (**{}**) kod. Daha sonra kolayca kod blokları tek tek bildirimi düzeyinizi görebilirsiniz ve kod düzeyi oluşturur.

## <a name="editor-help"></a>Düzenleyici Yardımı

- / / / İçin XML belge açıklamaları oluşturma

   Yazdıktan sonra bu onay kutusu seçildiğinde, XML belge açıklamaları için XML öğeleri ekler `///` yorum giriş. XML belgeleri hakkında daha fazla bilgi için bkz. [XML belgeleri yorumları (C# programlama Kılavuzu)](/dotnet/csharp/programming-guide/xmldoc/xml-documentation-comments).

## <a name="see-also"></a>Ayrıca bkz.

- [Nasıl yapılır: Belgeleri oluşturmak için XML açıklamalarını ekleme](../../ide/reference/generate-xml-documentation-comments.md)
- [XML belgeleri yorumları (C# programlama Kılavuzu)](/dotnet/csharp/programming-guide/xmldoc/xml-documentation-comments)
- [XML açıklamaları (C# Kılavuzu) ile kodunuzu belgeleme](/dotnet/csharp/codedoc)
- [Dile özgü düzenleyici seçeneklerini ayarlama](../../ide/reference/setting-language-specific-editor-options.md)
- [C# IntelliSense](../../ide/visual-csharp-intellisense.md)

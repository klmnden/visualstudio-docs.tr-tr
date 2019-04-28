---
title: Gelişmiş Seçenekler, metin düzenleyici, Basic (VB)
ms.date: 01/16/2019
ms.topic: reference
f1_keywords:
- VS.ToolsOptionsPages.Visual_Basic.Editor
- VS.ToolsOptionsPages.Text_Editor.Basic.Editor
- VS.ToolsOptionsPages.Visual_Basic_Editor.Editor
- VS.ToolsOptionsPages.Text_Editor.Basic.SimplifiedEditorPage
- VS.ToolsOptionsPages.Text_Editor.Basic
- VS.ToolsOptionsPages.Text_Editor.Basic.Advanced
- VS.ToolsOptionsPages.Text_Editor.Basic.VB_Specific
helpviewer_keywords:
- Basic Text Editor Options dialog box
ms.assetid: 5a8cafca-f7b4-4a2d-92ce-6894a7673d00
author: gewarren
ms.author: gewarren
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: aa331fea595c2143dd3ab47aa562fbd61277f81f
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62817794"
---
# <a name="options-text-editor-basic-visual-basic-advanced"></a>Gelişmiş Seçenekler, metin düzenleyici, temel (Visual Basic)
**VB belirli** özellik sayfasında **temel** klasörü **metin düzenleyici** klasörü **seçenekleri** (**araçları** menüsü) iletişim kutusunda, aşağıdaki özellikleri içerir:

## <a name="analysis"></a>Çözümleme

- Tam çözüm analizini etkinleştirme

   Çözümdeki tüm dosyalarda etkinleştirir kod analizi, yalnızca kod dosyaları açın. Daha fazla bilgi için [tam çözüm analizini](../../code-quality/how-to-enable-and-disable-full-solution-analysis-for-managed-code.md).

## <a name="using-directives"></a>Using yönergeleri

- Using deyimlerini sıralarken önce 'System' yönergelerini Yerleştir

   Bu onay kutusu seçildiğinde, **kullanımları Kaldır ve Sırala** sağ tıklama menüsünde sıralar komutunu `using` yönergeleri ve yerde listenin üst kısmındaki 'System' ad.

- Yönerge gruplarını kullanarak Ayır

   Bu onay kutusu seçildiğinde, **kullanımları Kaldır ve Sırala** sağ tıklama menüsünü komutta ayıran `using` aynı kök ad alanına sahip yönergeleri grupları arasında boş bir satıra ekleyerek yönergeleri.

- Reference bütünleştirilmiş kodlarında türler için using Öner
- NuGet paketlerinde türler için using Öner

   Bu seçenek seçildiğinde, bir [hızlı eylem](../quick-actions.md) NuGet paketini yüklemek ve eklemek kullanılabilir bir `using` başvurulmayan türleri için yönerge.

   ![Visual Studio'da NuGet paketini yüklemek için hızlı eylem](media/nuget-lightbulb.png)

## <a name="highlighting"></a>Vurgulama

 **Başvuruları ve anahtar sözcükleri vurgulamasını etkinleştirmenin**

Metin Düzenleyicisi gibi bir simgenin tüm örnekleri veya bir yan tümcesindeki tüm anahtar sözcükler vurgulayabilirsiniz `If..Then`, `While...End While`, veya `Try...Catch...Finally`. Vurgulanan başvurulara veya anahtar sözcükler tuşlarına basarak gezinebilirsiniz **Ctrl** + **Shift** + **aşağı ok** veya **Ctrl**   +  **Shift** + **yukarı ok**.

## <a name="outlining"></a>Anahat Oluşturma

**Anahat oluşturma modunu etkinleştir**

Kod Düzenleyicisi'nde bir dosyayı açtığınızda, belge anahat modunda görüntüleyebilirsiniz. Bkz: [anahat](../../ide/outlining.md) daha fazla bilgi için. Bu seçenek belirlendiğinde, bir dosyayı açtığınızda anahat oluşturma özelliği etkinleştirilir.

**Yordam satır ayıraçlarını Göster**

Metin düzenleyici, yordamların görsel kapsamını belirtir. Bir çizgi çizilir *.vb* konumlarda projenizin kaynak dosyaları aşağıdaki tabloda listelenen:

|.Vb kaynak dosya konumu|Satır konumu örneği|
|---------------------------------|------------------------------|
|Sonra bir blok bildirimi yapısı kapatma|-Sonunda sınıfı, yapısı, modülü, arabirim veya numaralandırma<br />-Özelliği, işlev veya alt after<br />-Get ve set değil arasında bir özellikte yan tümceleri|
|Tek satır yapıları bir dizi sonra|-İçeri aktarma deyimlerini after, önce bir sınıf dosyası içinde bir tür tanımı<br />-Bir sınıftaki tüm yordamları önce tanımlanan değişkenleri after|
|Tek satır bildirimlerinden sonra (blok düzey bildirimleri)|-İçeri aktarma deyimlerini aşağıdaki deyimleri, değişken bildirimleri, olay bildirimleri, temsilci bildirimleri devralır ve DLL ifadeleri bildirme|

## <a name="block-structure-guides"></a>Blok yapısı kılavuzları

Seçili olduğunda, dikey çizgileri Düzenleyicisi'nde bu satırı Yukarı tek bir kod bloklarını kolayca belirlemenize olanak sağlayan yapılandırılmış kod blokları ile görünür. Örneğin, bir satırı arasındaki bkz `Sub` ve `EndSub` içinde bir `Sub` deyimi.

## <a name="editor-help"></a>Düzenleyici Yardımı

**(Kodu yeniden biçimlendirme) düzgün listeleme** metin düzenleyici, uygun şekilde kodunuzu yeniden biçimlendirir. Bu seçenek belirlendiğinde, Kod Düzenleyici olur:

- Kodunuz doğru sekme konumuna Hizala

- Anahtar sözcükler, değişkenler ve doğru çalışması için nesneler recase

- Eksik ekleme `Then` için bir `If...Then` deyimi

- İşlev çağrıları için parantez ekleyin

- Bitiş tırnak işaretleri eksik dizelere ekleme

- Üstel gösterim yeniden biçimlendirin

- Tarihleri yeniden biçimlendirin

**Bitiş yapılarını otomatik ekleme**

Yazdığınızda — Örneğin, bir yordam bildirimi ilk satırını `Sub Main`— tuşuna basın **Enter**, eşleşen bir metin düzenleyicisi ekler `End Sub` satır. Benzer şekilde, eklerseniz bir [için](/dotnet/visual-basic/language-reference/statements/for-next-statement) döngüsü, metin düzenleyici ekler eşleşen `Next` deyimi. Bu seçenek belirlendiğinde, Kod Düzenleyicisi bitiş yapısı otomatik olarak ekler.

**Interface ve MustOverride üyelerinin otomatik ekleme**

İşlerseniz bir `Implements` deyimi veya bir `Inherits` ifadesi için bir sınıf, metin düzenleyici ekler prototipleri uygulanan ya da geçersiz, sırasıyla sahip üyeler için.

**Hata düzeltme önerilerini etkinleştirmek**

Metin düzenleyici, sık karşılaşılan çözümler önermek ve uygun düzeltmeyi kodunuza sonra uygulanır seçmenize olanak tanır.

## <a name="see-also"></a>Ayrıca bkz.

- [Genel, Ortam, Seçenekler İletişim Kutusu](../../ide/reference/general-environment-options-dialog-box.md)
- [Seçenekler, Metin Düzenleyici, Tüm Diller, Sekmeler](../../ide/reference/options-text-editor-all-languages-tabs.md)

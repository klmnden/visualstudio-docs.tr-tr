---
title: C# Düzenleyicisi biçimlendirme seçenekleri
ms.date: 08/14/2018
ms.topic: reference
f1_keywords:
- VS.ToolsOptionsPages.Text_Editor.CSharp.Formatting.Spacing
- VS.ToolsOptionsPages.Text_Editor.CSharp.Formatting.NewLines
- VS.ToolsOptionsPages.Text_Editor.CSharp.Formatting.Indentation
- VS.ToolsOptionsPages.Text_Editor.CSharp.Formatting.Wrapping
- VS.ToolsOptionsPages.Text_Editor.CSharp.Formatting
- VS.ToolsOptionsPages.Text_Editor.CSharp.Formatting.General
- VS.ToolsOptionsPages.Text_Editor.CSharp.Code_Style.Formatting.General
helpviewer_keywords:
- formatting options [C#]
- Text editor Options dialog box, formatting
author: gewarren
ms.author: gewarren
manager: jillfra
ms.workload:
- dotnet
ms.openlocfilehash: b555ede6ecf406f98c2e1ae9384b61664e8226cf
ms.sourcegitcommit: b468d71052a1b8a697f477ab23a3644de139f1e9
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/19/2019
ms.locfileid: "67260412"
---
# <a name="options-dialog-box-text-editor--c--code-style--formatting"></a>Seçenekler iletişim kutusu: Metin düzenleyici \> C# \> kod stili \> biçimlendirme

Kullanım **biçimlendirme** Seçenekleri sayfası ve onun alt ([**girinti**](#indentation-page), **yeni satırlar**, **aralığı** ve **sarmalama**) Kod düzenleyicisinde kod biçimlendirme seçeneklerini ayarlamak için.

Bu seçenekler sayfası erişmek için kendi seçtikleri **Araçları** > **seçenekleri** menü çubuğundan. İçinde **seçenekleri** iletişim kutusunda **metin düzenleyici** > **C#**  > **kod stili**  >  **Biçimlendirme**.

> [!TIP]
> **Girinti**, **yeni satırlar**, **aralığı**, ve **sarmalama** alt her gösteren alttaki Önizleme penceresini görüntüleyin Her seçeneği etkin. Önizleme penceresini kullanmak için biçimlendirme seçeneği seçin. Önizleme penceresini seçeneği örneği gösterilmektedir. Bir ayar radyo düğmesinin veya onay kutusunu, yeni ayar etkisini göstermek için önizleme penceresi güncelleştirmeleri seçerek değiştirdiğinizde.

## <a name="formatting-general-page"></a>Biçimlendirme (Genel) sayfası

### <a name="general-settings"></a>Genel ayarlar

Bu ayarlar etkiler *olduğunda* Kod düzenleyicisinde biçimlendirme seçeneklerini kod için geçerlidir.

|Etiketle|Açıklama|
|-----------|-----------------|
|**Yazarken Otomatik Biçimlendir**|Seçili olmadığında, **; deyimi biçimlendirme** ve **bloğu}** seçenekleri devre dışı bırakıldı.|
|**Biçim ifadesi üzerinde otomatik olarak;**|Seçili olduğunda, düzenleyici için seçili biçimlendirme seçeneklerine göre tamamlanma deyimleri biçimlendirir.|
|**Otomatik olarak bloğu}**|Bu onay kutusu seçildiğinde, biçimleri kod blokları için Düzenleyicisi kod bloğu tamamlar tamamlamaz seçili biçimlendirme seçeneklerine göre.|
|**Sonrasında Otomatik Biçimlendir**|Bu onay kutusu seçildiğinde, metin biçimleri, **Enter** düzenleyici için seçilen biçimlendirme seçenekleri uyacak şekilde basıldığında.|
|**Yapıştırıldığında otomatik olarak Biçimlendir**|Seçili olduğunda, düzenleyici için seçilen biçimlendirme seçenekleri uyacak şekilde düzenleyicisine yapıştırılan metin biçimlendirir.|

::: moniker range="vs-2019"

Kod stili ayarları için daha önce uygulandıysa C# kullanarak dosyaları **belgeyi Biçimlendir** işlevi olarak kullanıma sunuldu Visual Studio 2017, komut [ **kod Temizleme** ](../code-styles-and-code-cleanup.md#apply-code-styles).

::: moniker-end

::: moniker range="vs-2017"

### <a name="format-document-settings"></a>Biçim belgesi ayarları

Bu ayarları yapılandırmak **belgeyi Biçimlendir** bir dosyada ek kod temizleme işlemini gerçekleştirmek için komutu. Bu ayarları nasıl uygulanacağı hakkında daha fazla bilgi için bkz. [belgeyi Biçimlendir komut](../code-styles-and-code-cleanup.md#apply-code-styles).

|Etiketle|Açıklama|Karşılık gelen EditorConfig ve Araçlar > Seçenekler kuralları|
|-----------|-----------------|-----------------|-----------------|
|**Tüm uygulama C# biçimlendirme kurallarını (Girinti, sarmalama, aralık)**|**Belgeyi Biçimlendir** her zaman biçimlendirme sorunları giderir komutu. Bu ayar değiştirilemez.| [Çekirdek EditorConfig seçeneği](../../ide/create-portable-custom-editor-options.md)<br/>[.NET EditorConfig biçimlendirme seçenekleri](../../ide/editorconfig-formatting-conventions.md)<br/><br/>**Araçlar** > **seçenekleri** > **metin düzenleyici**  >  **C#**  >   **Biçimlendirme** > [**girinti** veya **yeni satırlar** veya **aralığı** veya **sarmalama**]|
|**Biçimlendirme sırasında ekleme kodu temizleme gerçekleştirin**|Bu onay kutusu seçildiğinde, düzeltmeler aşağıda belirtilen kuralları geçerlidir **Edit.FormatDocument** komutu.| Yok |
|**Gereksiz kullanımları Kaldır**|Seçili olduğunda, gereksiz kaldırır `using` yönergeleri olduğunda **Edit.FormatDocument** tetiklenir.| Yok |
|**Kullanımları sıralama**|Bu onay kutusu seçildiğinde, sıralar `using` yönergeleri olduğunda **Edit.FormatDocument** tetiklenir.| dotnet_sort_system_directives_first<br/><br/>**Araçlar** > **seçenekleri** > **metin düzenleyici** > **C#**  > **Gelişmiş**   >  **Yer 'System' yönergelerini ilk kullanımları sıralarken** |
|**Küme ayraçları için tek satır denetim ifadeleri Ekle/Kaldır**|Bu onay kutusu seçildiğinde, ekler veya küme ayraçları tek satır denetimi deyimlerini kaldırır, **Edit.FormatDocument** tetiklenir.| csharp_prefer_braces<br/><br/>**Araçlar** > **seçenekleri** > **metin düzenleyici** > **C#**  > **kod stili**   >  **Kod bloğu tercihleri** > **küme ayraçlarını tercih et** |
|**Erişilebilirlik değiştiricileri Ekle**|Bu onay kutusu seçildiğinde, eksik erişilebilirlik değiştiricileri ekler, **Edit.FormatDocument** tetiklenir.| dotnet_style_require_accessibility_modifiers |
|**Erişilebilirlik değiştiricileri Sırala**|Bu onay kutusu seçildiğinde, erişilebilirlik değiştiricileri sıralar, **Edit.FormatDocument** tetiklenir.| csharp_preferred_modifier_order<br/>visual_basic_preferred_modifier_order |
|**İfade veya engelleme gövdesi tercihleri Uygula**|İfade gövdeli üyeler gövdeleri engellemek için bu onay kutusu seçildiğinde, dönüştürür ya da tam tersi zaman **Edit.FormatDocument** tetiklenir.| [İfade gövdeli üye EditorConfig seçeneği](../../ide/editorconfig-language-conventions.md#expression-bodied-members)<br/><br/>**Araçlar** > **seçenekleri** > **metin düzenleyici** > **C#**  > **kod stili**   >  **İfade tercihleri** > **yöntemleri, Oluşturucular, vb. için ifade gövdesi kullan.** |
|**Örtük/açık tür tercihleri Uygula**|Bu onay kutusu seçildiğinde, dönüştürür `var` açık tür veya tam tersi zaman **Edit.FormatDocument** tetiklenir.| [Açık tür EditorConfig seçeneği](../../ide/editorconfig-language-conventions.md#implicit-and-explicit-types)<br/><br/>**Araçlar** > **seçenekleri** > **metin düzenleyici** > **C#**  > **kod stili**   >  **'var' tercihleri** |
|**Satır içi 'out' değişken tercihleri Uygula**|Seçili olduğunda, satır içleri `out` değişkenleri burada mümkün olduğunda **Edit.FormatDocument** tetiklenir.| csharp_style_inlined_variable_declaration<br/><br/>**Araçlar** > **seçenekleri** > **metin düzenleyici** > **C#**  > **kod stili**   >  **Değişken tercihleri** > **satır içi değişken bildirimini tercih et** |
|**Dil/framework tür tercihleri Uygula**|Seçildiğinde, language türleri dönüştürür framework türleri veya tam tersi zaman **Edit.FormatDocument** tetiklenir.| dotnet_style_predefined_type_for_locals_parameters_members<br/>dotnet_style_predefined_type_for_member_access<br/><br/>**Araçlar** > **seçenekleri** > **metin düzenleyici** > **C#**  > **kod stili**   >  **önceden tanımlanmış tür tercihleri** |
|**Nesne/toplama başlatma tercihleri Uygula**|Bu onay kutusu seçildiğinde, mümkün olduğunda nesne ve koleksiyon başlatıcıları kullanır, **Edit.FormatDocument** tetiklenir.| dotnet_style_object_initializer<br/>dotnet_style_collection_initializer<br/><br/>**Araçlar** > **seçenekleri** > **metin düzenleyici** > **C#**  > **kod stili**   >  **İfade tercihleri** > **nesne başlatıcısını tercih et** veya **koleksiyon başlatıcısını tercih et** |
|**'This.' niteliği tercihleri Uygula**|Seçili olduğunda geçerlidir `this.` tercihleri olduğunda **Edit.FormatDocument** tetiklenir.| [Bu. Nitelik EditorConfig seçeneği](../../ide/editorconfig-language-conventions.md#this-and-me)<br/><br/>**Araçlar** > **seçenekleri** > **metin düzenleyici** > **C#**  > **kod stili**   >  **'this.' tercihleri** |
|**Mümkün olduğunda özel alanları salt okunur yapın**|Seçili olduğunda, özel alanlar yapar `readonly` burada mümkün olduğunda **Edit.FormatDocument** tetiklenir.| dotnet_style_readonly_field<br/><br/>**Araçlar** > **seçenekleri** > **metin düzenleyici** > **C#**  > **kod stili**   >  **Alan tercihleri** > **salt okunur tercih et** |
|**Gereksiz atamaları Kaldır**|Bu onay kutusu seçildiğinde, mümkün olduğunda gereksiz atamalar kaldırır, **Edit.FormatDocument** tetiklenir.| Yok |
|**Kullanılmayan değişkenler Kaldır**|Bu onay kutusu seçildiğinde, ne zaman kullanılmayan değişkenler kaldırır **Edit.FormatDocument** tetiklenir.| Yok |

![Visual Studio'da C# kod temizleme ayarları](media/format-document-settings.png)

::: moniker-end

## <a name="indentation-page"></a>Girinti sayfası

Girintileme seçenekleri sayfasında bu kodu otomatik olarak biçimlendirildiğinde uygulayın. Bir dosya kodu yapıştırın, kod otomatik olarak biçimlendirilmiş bir örneği olduğunda **otomatik olarak, yapıştırma sırasında Biçimlendir** seçilir. ( **Otomatik olarak, yapıştırma sırasında Biçimlendir** seçenektir altında **biçimlendirme** > **genel**.)

![C#Visual Studio Metin Düzenleyicisi girinti seçenekleri](media/csharp-indentation-options.png)

> [!TIP]
> Ayrıca vardır Girintileme seçenekleri üzerinde **metin düzenleyici** > **C#**  > **sekmeleri** seçenekler sayfası. Bu seçenekler yalnızca bastığınızda Kod düzenleyicisinde imleci burada yerleştirir belirlemek **Enter** bir satırın sonunda.
>
> ![C#Metin Düzenleyici sekmesi seçenekleri Visual Studio'da](media/csharp-tabs-options.png)

## <a name="see-also"></a>Ayrıca bkz.

- [Genel, ortam, Seçenekler iletişim kutusu](../../ide/reference/general-environment-options-dialog-box.md)
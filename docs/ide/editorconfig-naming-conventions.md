---
title: .NET adlandırma kuralları için EditorConfig dosyaları
ms.date: 11/20/2017
ms.topic: reference
helpviewer_keywords:
- naming conventions [EditorConfig]
- EditorConfig naming conventions
author: gewarren
ms.author: gewarren
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: bb72f491046d16f028561c19995a27a6ab64a830
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62557326"
---
# <a name="net-naming-conventions-for-editorconfig"></a>EditorConfig için .NET adlandırma kuralları

Adlandırma kuralları, sınıflar, özellikler ve yöntemler gibi kod öğeleri adlandırma ilgilendiriyor. Örneğin, Genel üyeler büyük harfle yazılmalıdır veya zaman uyumsuz yöntemler "Async" sonlandırması gerektiğini belirtebilirsiniz. Bunları belirterek bu kuralları zorunlu kılabilir bir [.editorconfig dosyasındaki](../ide/create-portable-custom-editor-options.md). Adlandırma kuralı ihlallerini ya da görünür **hata listesi** veya adı altında bir öneri olarak önem derecesine bağlı olarak, kuralınız için seçin. İhlalleri görmek için projeyi derlemek için gerek yoktur.

Adlandırma kuralları en belirgin sıralı çok az özgü EditorConfig dosyasında. Uygulanabilir ilk kuralı karşılaştı uygulanan yalnızca bir kuraldır. Ancak, birden çok kural varsa *özellikleri* bu ada sahip özelliği önceliklidir aynı ada sahip en son bulunamadı. Daha fazla bilgi için [dosya hiyerarşisi ve öncelik](create-portable-custom-editor-options.md#file-hierarchy-and-precedence).

Her bir adlandırma kuralı için aşağıda açıklanan özelliklerini kullanarak geçerli simgeleri ve adlandırma stili kuralı zorunlu tutmak için bir önem derecesi belirtmelisiniz. Özelliklerin sırası önemli değildir.

Başlamak için her kural tam olarak açıklamak için gereken özellikleri kullanacağınız, adlandırma kuralı için bir başlık seçin. Örneğin, `public_members_must_be_capitalized` bir adlandırma kuralı için iyi ve açıklayıcı bir ad. Seçtiğiniz olarak başlığa başvuracağınız **< namingRuleTitle\>**  olarak bölümlerde.

## <a name="symbols"></a>Simgeleri

İlk olarak, bir grubu için adlandırma kuralı uygulamak için sembolleri tanımlayın. Bu özellik aşağıdaki biçime sahiptir:

`dotnet_naming_rule.<namingRuleTitle>.symbols = <symbolTitle>`

Değiştirerek simgeleri grubu için bir ad verin **< symbolTitle\>**  açıklayıcı bir başlık örneğin değerini `public_symbols`. Kullanacağınız **< symbolTitle\>**  açıklayan üç özellik adlarını kural simgeleri değeri (simge, Erişilebilirlik düzeyleri ve değiştiriciler türleri için) uygulanır.

### <a name="kinds-of-symbols"></a>Tür simgeleri

Adlandırma kuralı uygulamak için semboller türünü tanımlamak için bir özelliği şu biçimde belirtin:

`dotnet_naming_symbols.<symbolTitle>.applicable_kinds = <values>`

Aşağıdaki listede, izin verilen değerler gösterilir ve virgül ile ayırarak birden çok değer belirtebilirsiniz.

- \* (tüm sembolleri belirtmek için bu değeri kullanın)
- ad alanı
- sınıf
- struct 
- arabirim
- enum
- özellik
- yöntemi
- alan
- olay
- temsilci
- parametre
- type_parameter
- yerel
- local_function

### <a name="accessibility-levels-of-symbols"></a>Erişilebilirlik düzeyleri simgeleri

Erişilebilirlik düzeyleri adlandırma kuralı uygulamak istediğiniz simgeleri tanımlamak için bir özellik adı şu biçimde belirtin:

`dotnet_naming_symbols.<symbolTitle>.applicable_accessibilities = <values>`

Aşağıdaki listede, izin verilen değerler gösterilir ve virgül ile ayırarak birden çok değer belirtebilirsiniz.

- \* (tüm erişilebilirlik düzeyleri belirtmek için bu değeri kullanın)
- public
- iç veya arkadaş
- private
- protected
- korumalı\_iç veya protected_friend
- özel\_korumalı
- yerel

   `local` Bir yöntem içinde tanımlanan simgeleri erişilebilirlik düzeyi uygular. Kodda, Erişilebilirlik belirtilemez sembolleri için adlandırma kuralları tanımlamak için yararlıdır. Örneğin, belirtirseniz `applicable_accessibilities = local` sabitleri için bir adlandırma kuralı üzerinde (`required_modifiers = const`), yalnızca bir yöntem içinde tanımlı sabitler ve olmayan bir tür içinde tanımlanan kuralı uygulanır.

   ```csharp
   class TypeName
   {
     // Constant defined in a type.
     const int X = 3;

     void Method()
     {
       // Constant defined in a method with "local" accessibility.
       const int Y = 4;
     }
   }
   ```

### <a name="symbol-modifiers-optional"></a>Sembol değiştiriciler (isteğe bağlı)

Değiştiriciler adlandırma kuralı uygulamak istediğiniz simgeleri tanımlamak için bir özellik adı şu biçimde belirtin:

`dotnet_naming_symbols.<symbolTitle>.required_modifiers = <values>`

Aşağıdaki liste gösterir (birden çok değer virgülle ayırın) izin verilen değerler:

- `abstract` veya `must_inherit`
- `async`
- `const`
- `readonly`
- `static` veya `shared`

   > [!NOTE]
   > İçin bir adlandırma kuralı varsa `static` veya `shared` simgeler, ayrıca uygulanan `const` örtük olarak statik olduğundan semboller. İstemiyorsanız `static` uygulamak için adlandırma kuralı `const` sembolleri oluşturmak için ayrı bir adlandırma kuralı `const` semboller.

Bir adlandırma kuralı sahip imzaları eşleşen *tüm* belirtilen değiştiricilere `required_modifiers`. Bu özelliği atarsanız, varsayılan değer olan boş bir listeyle kullanılır, diğer bir deyişle, hiçbir özel değiştiriciler eşleştirmek için gereklidir. Bu sembolün değiştiriciler olsun veya olmasın bu kuralın uygulanacağı üzerinde hiçbir etkisi yok anlamına gelir.

> [!TIP]
> Değerini belirtmeyin `*` için `required_modifiers`. Bunun yerine, yalnızca atlamak `required_modifiers` özelliği Toptan ve adlandırma kuralınıza değiştiricisi herhangi bir türden uygulanır.

## <a name="style"></a>Stil

Şu grup için adlandırma kuralı uygulamak için simgeleri tanımladığınıza göre biz adlandırma stili açıklamanız gerekir. Bir stil adı belirli bir önek veya belirli bir sonek olduğundan veya kelimeler adında belirli bir karakteriyle ayrılır olabilir. Ayrıca, bir büyük harf stili belirtebilirsiniz. Stil özelliği şu biçimdedir:

`dotnet_naming_rule.<namingRuleTitle>.style = <styleTitle>`

Stil değiştirerek bir ad verin **< styleTitle\>**  açıklayıcı bir başlık örneğin değerini `first_word_upper_case_style`. Kullanacağınız **< styleTitle\>**  adlandırma stili (öneki ve soneki, sözcük ayırıcı karakteri ve büyük/küçük harf) tanımlayan özellik adlarını değeri. Bir veya daha fazla bu özellik, stil açıklamak için kullanın.

### <a name="require-a-prefix"></a>Bir önek gerektirir

Sembol adları belirli karakterle başlamalıdır belirtmek için bu özelliği kullanın:

`dotnet_naming_style.<styleTitle>.required_prefix = <prefix>`

### <a name="require-a-suffix"></a>Bir sonek gerektirir

Sembol adları belirli karakter ile sona ermelidir belirtmek için bu özelliği kullanın:

`dotnet_naming_style.<styleTitle>.required_suffix = <suffix>`

### <a name="require-a-certain-word-separator"></a>Belirli bir sözcük ayırıcı gerektirir

Kelimeler sembol adları belirli bir karakter ile ayrılmalıdır belirtmek için bu özelliği kullanın:

`dotnet_naming_style.<styleTitle>.word_separator = <separator character>`

### <a name="require-a-capitalization-style"></a>Bir büyük harf stili gerektirir

Sembol adları belirli büyük/küçük harf stilini belirlemek için bu özelliği kullanın:

`dotnet_naming_style.<styleTitle>.capitalization = <value>`

Bu özellik için izin verilen değerler şunlardır:

- pascal_case
- camel_case
- İlk\_word_upper
- tüm\_üst
- all_lower

> [!NOTE]
> Bir büyük harf stili adlandırma stiliniz yoksayıldı, adlandırma stili, aksi takdirde bir parçası olarak belirtmeniz gerekir.

## <a name="severity"></a>Önem Derecesi

Adlandırma kuralınıza ihlalini önemini açıklamak için bir özelliği şu biçimde belirtin:

`dotnet_naming_rule.<namingRuleTitle>.severity = <value>`

Aşağıdaki tabloda verilen önem derecesi değerlerini ve onların ne anlama geldiğini gösterir:

Önem Derecesi | Efekt
------------ | -------------
yok veya Sessiz | Bu stil ardından, hiçbir şey kullanıcıya göstermez; Ancak, otomatik olarak oluşturulan kod, bu stil izler.
Öneri | Bu stil ardından, kullanıcı için ilk iki karakter üzerinde temel alınan noktaların bir öneri olarak gösterir. Derleme zamanında hiçbir etkisi yoktur.
warning | Bu stil ardından, derleyici uyarı olarak göster **hata listesi**.
error | Bu stil ardından, bir derleyici hatası Göster **hata listesi**.

> [!NOTE]
> Adlandırma kuralı ihlallerini görmek için projenizi oluşturmanız gerekmez. Kod düzenleme gibi görünürler ya da **hata listesi** veya bir öneri olarak.

## <a name="example"></a>Örnek

Aşağıdaki *.editorconfig* dosyası, ortak özellikler, yöntemler, alanlar, olaylar ve temsilciler büyük harfle yazılmalıdır olduğunu belirten bir adlandırma kuralı içerir. Bu adlandırma değerleri birbirinden ayırmak için virgül kullanarak birden çok tür, kuralın uygulanacağı simge belirtir dikkat edin.

```EditorConfig
# Public members must be capitalized (public_members_must_be_capitalized)
[*.{cs,vb}]
dotnet_naming_rule.public_members_must_be_capitalized.symbols   = public_symbols
dotnet_naming_symbols.public_symbols.applicable_kinds           = property,method,field,event,delegate
dotnet_naming_symbols.public_symbols.applicable_accessibilities = public
dotnet_naming_symbols.public_symbols.required_modifiers         = readonly

dotnet_naming_rule.public_members_must_be_capitalized.style    = first_word_upper_case_style
dotnet_naming_style.first_word_upper_case_style.capitalization = first_word_upper

dotnet_naming_rule.public_members_must_be_capitalized.severity = suggestion
```

Aşağıdaki ekran görüntüsünde, Düzenleyici'de şu adlandırma kuralını etkisini gösterir. İki genel değişkenleri ilk harfi büyük harf adlandırılmış sahiptir. Biri bir `const`, ve `readonly`. Adlandırma kuralı yalnızca uygulandığı beri `readonly` simgeleri, yalnızca `readonly` değişkeni bir adlandırma kuralı öneri gösterir.

![Adlandırma kuralı önerisi](media/editorconfig-naming-rule-suggestion.png)

Artık ihlali önem derecesini değiştirelim `warning`:

```EditorConfig
dotnet_naming_rule.public_members_must_be_capitalized.severity = warning
```

Ad ihlalini altında bir öneri görmek yerine kod dosyanızın kapatıp yeşil dalgalı ve bir uyarı görürsünüz **hata listesi**:

![Adlandırma kuralı Uyarısı](media/editorconfig-naming-rule-warning.png)

## <a name="see-also"></a>Ayrıca bkz.

- [.NET dil ve biçimlendirme kuralları](../ide/editorconfig-code-style-settings-reference.md)
- [Taşınabilir özel düzenleyici seçenekleri oluşturma](../ide/create-portable-custom-editor-options.md)
- [.NET derleyici platformu'nın .editorconfig dosyasındaki](https://github.com/dotnet/roslyn/blob/master/.editorconfig)

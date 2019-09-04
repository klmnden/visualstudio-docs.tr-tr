---
title: Normal ifadeler kullanma
ms.date: 06/12/2019
ms.topic: conceptual
f1_keywords:
- vsregularexpressionhelp
- vs.regularexpressionhelp
- vs.wildcardsbuilder
- vs.netregularexpressionhelp
- vs.wildcards
helpviewer_keywords:
- regular expressions [Visual Studio]
- regular expressions
author: gewarren
ms.author: gewarren
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: aaea2e8a2c4fbbead563bd9565cf84466e00c75c
ms.sourcegitcommit: 9c07ae6fb18204ea080c8248994a683fa12e5c82
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/04/2019
ms.locfileid: "70293433"
---
# <a name="use-regular-expressions-in-visual-studio"></a>Visual Studio'da normal ifadeler kullanma

Visual Studio, metni bulmak ve değiştirmek için [.net normal ifadelerini](/dotnet/standard/base-types/regular-expressions) kullanır.

## <a name="regular-expression-examples"></a>Normal ifade örnekleri

Aşağıdaki tabloda bazı normal ifade karakterleri, işleçler, yapılar ve model örnekleri yer almaktadır. Daha kapsamlı bir başvuru için bkz. [normal ifade dili](/dotnet/standard/base-types/regular-expression-language-quick-reference).

|Amaç|İfade|Örnek|
|-------------|----------------|-------------|
|Tek bir karakterle Eşleştir (satır sonu hariç). Daha fazla bilgi için, bkz. [herhangi bir karakter](/dotnet/standard/base-types/character-classes-in-regular-expressions#any-character-).|biçimindeki telefon numarasıdır.|`a.o`"About" içinde "Acro" ve "" değil "About" ve "ABO" içinde "Aro" ile eşleşir|
|Önceki ifadenin sıfır veya daha fazla tekrarlamalarını eşleştirin (mümkün olduğunca çok karakterle Eşleştir). Daha fazla bilgi için bkz. [sıfır veya daha fazla kez eşleşme](/dotnet/standard/base-types/quantifiers-in-regular-expressions#match-zero-or-more-times-).|*|`a*r` "rack" daki "r", "ark" içinde "ar" ve "aardvark", "aar" ile eşleşir.|
|Sıfır veya daha fazla kez herhangi bir karakterle eşleştir (joker karakter \*)|.*|`c.*e` "comme" "racket", "comment" "comme" ve "Code" ve "code" ile eşleşir.|
|Önceki ifadenin bir veya daha çok tekrarı ile Eşleştir (mümkün olduğu kadar çok karakterle Eşleştir). Daha fazla bilgi için bkz. [bir veya daha fazla kez eşleşme](/dotnet/standard/base-types/quantifiers-in-regular-expressions#match-one-or-more-times-).|+|`e.+d`"besleyici" içinde "eed" eşleşir ancak "Ed" olarak eşleşmez|
|Bir veya daha fazla (joker?) herhangi bir karakterle eşleştir|.+|`e.+e`"besleyici" içinde "epi" ile eşleşir ancak "Ee" değil|
|Önceki ifadenin sıfır veya daha fazla tekrarlamalarını eşleştirin (mümkün olduğunca az karakter eşleştirin). Daha fazla bilgi için bkz. [sıfır veya daha fazla kez eşleşme (geç eşleşme)](/dotnet/standard/base-types/quantifiers-in-regular-expressions#match-zero-or-more-times-lazy-match-).|*?|`e.*?e`"besleyici" içinde "Ee" ile eşleşir ancak "göz yormayabilir"|
|Önceki ifadenin bir veya daha çok tekrarı ile Eşleştir (mümkün olduğu kadar az karakterle Eşleştir). Daha fazla bilgi için bkz. [bir veya daha fazla kez eşleşme (geç eşleşme)](/dotnet/standard/base-types/quantifiers-in-regular-expressions#match-one-or-more-times-lazy-match-).|+?|`e.+?e`"Enterprise" içinde "Ente" ve "erprise" ile eşleşir ancak "Enterprise" sözcüğünün tamamını kullanmaz|
|Eşleşme dizesini [bir satırın veya dizenin başına](/dotnet/standard/base-types/anchors-in-regular-expressions#start-of-string-or-line-) bağla|^|`^car`"otomobil" sözcüğüyle yalnızca bir satırın başlangıcında göründüğünde eşleşir|
|Eşleşme dizesini [bir satırın sonuna](/dotnet/standard/base-types/anchors-in-regular-expressions#end-of-string-or-line-) bağla|\r?$|`end\r?$`yalnızca bir satırın sonunda göründüğünde "End" ile eşleşir|
|Eşleşme dizesini dosyanın sonuna bağlantı|$|`end$`Yalnızca dosyanın sonunda göründüğünde "End" ile eşleşir|
|Bir kümedeki tek bir karakterle eşleştir|[abc]|`b[abc]`"ba", "BB" ve "BC" ile eşleşir|
|Karakter aralığındaki herhangi bir karakterle eşleştir|[a-f]|`be[n-t]`"altta", "Ben" içinde "bir" ve "bes" içinde "Bet" ve "altı" içinde "bes" ile eşleşir, ancak "aşağıda" değil|
|Yakalama ve parantez içinde yer alan ifadesi örtük olarak numaralandır|()|`([a-z])X\1` "aXa" ve "bXb" ancak değil "aXb" ile eşleşir. "\1", ilk ifade grubu "[a-z]" anlamına gelir. Daha fazla bilgi için bkz. [yakalama grupları ve değiştirme desenleri](#capture-groups-and-replacement-patterns). |
|Eşlemeyi geçersiz kıl|(?!abc)|`real(?!ity)` "gerçek" bir "realty" ve "really" eşleşir ancak değil içinde "gerçeklik." Ayrıca ikinci "real" (ancak değil ilk "real") "realityreal" içinde bulur.|
|Belirli bir karakter kümesinde olmayan herhangi bir karakterle eşleştirin. Daha fazla bilgi için bkz. [negatif karakter grubu](/dotnet/standard/base-types/character-classes-in-regular-expressions#negative-character-group-).|[^ abc]|`be[^n-t]`"önceki" içinde "BEF", "Behind" içinde "beh" ve "Bel" içinde "aşağıda" değil, "Bel" ile eşleşir|
|Simgeden önceki veya bir ifadeden sonraki ifadeyle Eşleştir|&#124;|`(sponge|mud) bath`"sünge banyo" ve "Mud banyo" ile eşleşir|
|Ters eğik çizgiden sonraki [karakteri kaçış](/dotnet/standard/base-types/character-escapes-in-regular-expressions)| \\ |`\^`^ karakteriyle eşleşir|
|Önceki karakterin veya grubun oluşum sayısını belirtin. Daha fazla bilgi için bkz. [tam n kez eşleşme](/dotnet/standard/base-types/quantifiers-in-regular-expressions#match-exactly-n-times-n).|{n}, burada ' n ' oluşum sayısıdır|`x(ab){2}x`"xabex" ile eşleşir<br/>`x(ab){2,3}x`"xabex" ve "xabababx" ile eşleşir ancak "xababababx" olarak eşleşmez|
|[Unicode kategorisindeki metni eşleştirin](/dotnet/standard/base-types/character-classes-in-regular-expressions#unicode-category-or-unicode-block-p). Unicode karakter sınıfları hakkında daha fazla bilgi için bkz. [Unicode standart 5,2 karakter özellikleri](http://www.unicode.org/versions/Unicode5.2.0/ch04.pdf).|\p{X}, "X" değerinin Unicode numarası olduğu.|`\p{Lu}`"Thomas tikan" içinde "T" ve "D" ile eşleşir|
|[Sözcük sınırını Eşleştir](/dotnet/standard/base-types/anchors-in-regular-expressions#word-boundary-b)|\b (bir karakter sınıfı dışında `\b` bir sözcük sınırını belirler ve bir karakter sınıfı içinde `\b` Geri Al ile eşleşir.)|`\bin`"in" içinde "içinde" eşleşir ancak "Pinto" Not etmez|
|Satır sonuyla eşleştir (diğer bir deyişle, satır başı, izleyen yeni bir satır)|\r?\n|`End\r?\nBegin`"End" ve "Begin" ile yalnızca "End" satırdaki son dize olduğunda ve "Begin" bir sonraki satırdaki ilk dizeyse|
|Herhangi bir [sözcük karakteri](/dotnet/standard/base-types/character-classes-in-regular-expressions#word-character-w) Eşleştir|\w|`a\wd`"Add" ve "A1D" ile eşleşir, ancak "a d" eşleşmez|
|Herhangi bir [boşluk karakteriyle](/dotnet/standard/base-types/character-classes-in-regular-expressions#whitespace-character-s) Eşleştir|\s|`Public\sInterface`"ortak arabirim" ifadesi ile eşleşir|
|Herhangi bir [ondalık basamak karakteriyle](/dotnet/standard/base-types/character-classes-in-regular-expressions#decimal-digit-character-d) Eşleştir|\d|`\d`"3456", "2" ve "1" içinde "1" içinde "3" ve "1" ile eşleşir|
|Unicode karakterini eşleştir|\uXXXX nerede XXXX Unicode karakter değerini belirtir.|`\u0065`"e" karakteriyle eşleşir|
|Tanımlayıcı eşleştir|\b [\_\w-[0-9]] [\_\w]*\b|"Type1" ile eşleşir, ancak "& Type1" veya "#define" olarak eşleşmez|
|Tırnak işaretleri içindeki bir dizeyle eşleştir|((\\".+?\\")&#124;('.+?'))|Tek veya çift tırnak içinde herhangi bir dizeyle eşleşir|
|Onaltılık bir sayıyla eşleştir|\b0 [xx] ([0-9A-FA-F] +\)\b|"0xc67f" ile eşleşir ancak "0xc67g" olarak eşleşmez|
|Eşleşme tamsayıları ve ondalık sayıları|\b[0-9]*\\.\*[0-9]+\b|"1,333" ile eşleşir|

> [!TIP]
> Windows işletim sistemlerinde satırların çoğu "\r\n" (bir yeni satırın izlediği bir satır başı) bitmelidir. Bu karakterler görünür değildir ancak düzenleyicide bulunur ve .NET normal ifade hizmetine iletilir.

## <a name="capture-groups-and-replacement-patterns"></a>Yakalama grupları ve değiştirme desenleri

Yakalama grubu, normal bir ifadenin alt ifadesini toplar ve bir giriş dizesinin alt dizesini yakalar. Normal ifadenin içinde yakalanan grupları kullanabilirsiniz (örneğin, yinelenen bir sözcüğe bakmak için) veya değiştirme düzeninde. Ayrıntılı bilgi için bkz. [normal ifadelerde yapıları gruplandırma](/dotnet/standard/base-types/grouping-constructs-in-regular-expressions).

Numaralandırılmış bir yakalama grubu oluşturmak için, alt ifadeyi normal ifade deseninin parantezleri ile çevreleyin. Yakalamaları, normal ifadede açma parantezinin konumuna göre otomatik olarak soldan sağa numaralandırılır. Yakalanan gruba erişmek için:

- **normal ifade içinde**: Kullanın `\number`. Örneğin, `\1` normal ifadede `(\w+)\s\1` ilk yakalama grubuna `(\w+)`başvuru yapılır.

- **değiştirme**düzeninde: Kullanın `$number`. Örneğin, gruplanan normal ifadeyle `(\d)([a-z])` iki grupları tanımlar: ilk grubu tek bir ondalık basamak içeren ve ikinci grubu arasında tek bir karakter içeren **bir** ve **z**. İfade aşağıdaki dizede dört eşleşme bulur: **1a 2b 3c 4d**. Değiştirme dizesi `z$1` yalnızca ilk gruba (`$1`) başvurur ve dizeyi **Z1 Z2 Z3 Z4**öğesine dönüştürür.

Aşağıdaki görüntüde bir normal ifade `(\w+)\s\1` ve bir değiştirme dizesi `$1`gösterilmektedir. Normal ifade ve değiştirme deseninin her ikisi de otomatik olarak numaralandırılan ilk yakalama grubuna başvurur. Visual Studio 'daki **hızlı değiştirme** iletişim kutusunda **Tümünü Değiştir** ' i seçtiğinizde, yinelenen sözcükler metinden kaldırılır.

![Visual Studio 'da Numaralandırılmış yakalama grubunu gösteren hızlı değiştirme](media/numbered-capture-group.png)

> [!TIP]
> **Hızlı değiştirme** Iletişim kutusunda **Normal ifadeleri kullan** düğmesinin seçili olduğundan emin olun.

### <a name="named-capture-groups"></a>Adlandırılmış yakalama grupları

Bir yakalama grubunun otomatik numaralandırmasına güvenmek yerine, buna bir ad verebilirsiniz. Adlandırılmış bir yakalama grubunun sözdizimi vardır `(?<name>subexpression)`.

Numaralandırılmış yakalama grupları gibi adlandırılmış yakalama grupları, normal ifadenin içinde veya değiştirme düzeninde kullanılabilir. Adlandırılmış yakalama grubuna erişmek için:

- **normal ifade içinde**: Kullanın `\k<name>`. Örneğin, `\k<repeated>` normal ifadede `(?<repeated>\w+)\s\k<repeated>` , adlandırılmış `repeated` ve alt ifadesi olan yakalama grubuna başvuruda bulunur `\w+`.

- **değiştirme**düzeninde: Kullanın `${name}`. Örneğin: `${repeated}`.

Örnek olarak, aşağıdaki görüntüde bir normal ifade `(?<repeated>\w+)\s\k<repeated>` ve bir değiştirme dizesi `${repeated}`gösterilmektedir. Hem normal ifade hem de değiştirme deseninin adlı `repeated`yakalama grubu başvurusu. Visual Studio 'daki **hızlı değiştirme** iletişim kutusunda **Tümünü Değiştir** ' i seçtiğinizde, yinelenen sözcükler metinden kaldırılır.

![Visual Studio 'da adlandırılmış bir yakalama grubunu gösteren hızlı değiştirme](media/named-capture-group.png)

> [!TIP]
> **Hızlı değiştirme** Iletişim kutusunda **Normal ifadeleri kullan** düğmesinin seçili olduğundan emin olun.

Adlandırılmış yakalama grupları hakkında daha fazla bilgi için bkz. [eşleşen alt Ifadeler adlandırılmış](/dotnet/standard/base-types/grouping-constructs-in-regular-expressions#named-matched-subexpressions). Değiştirme desenlerinde kullanılan normal ifadeler hakkında daha fazla bilgi için bkz. [normal Ifadelerde değişimler](/dotnet/standard/base-types/substitutions-in-regular-expressions).

## <a name="see-also"></a>Ayrıca bkz.

- [Normal ifade dili](/dotnet/standard/base-types/regular-expression-language-quick-reference)
- [Metin bulma ve değiştirme](../ide/finding-and-replacing-text.md)

---
title: Normal ifadeler kullanma
ms.date: 03/26/2018
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
ms.openlocfilehash: b20cf3692cf76f602eb11b0a53a1669c919f1679
ms.sourcegitcommit: 9753c7544cec852ca5efd0834e0956d9e53a5734
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/13/2019
ms.locfileid: "67043577"
---
# <a name="use-regular-expressions-in-visual-studio"></a>Visual Studio'da normal ifadeler kullanma

Visual Studio kullanan [.NET normal ifadeler](/dotnet/standard/base-types/regular-expressions) metin bulma ve değiştirme için.

## <a name="regular-expression-examples"></a>Normal ifade örnekleri

Aşağıdaki tablolarda, bazı normal ifade karakterleri, işleçler, yapıları ve düzeni örnekleri içerir. Daha eksiksiz bir başvuru için bkz: [normal ifade dili](/dotnet/standard/base-types/regular-expression-language-quick-reference).

|Amaç|İfade|Örnek|
|-------------|----------------|-------------|
|(Satır sonu hariç) tek bir karakterle Eşleştir. Daha fazla bilgi için [herhangi bir karakterle](/dotnet/standard/base-types/character-classes-in-regular-expressions#any-character-).|biçimindeki telefon numarasıdır.|`a.o` "Around" öğesinde "ARO" ve "about" öğesinde "abo" ancak değil "eri" "arasında" ile eşleşir.|
|Önünde gelen ifadenin sıfır veya daha çok tekrarı ile eşleştir (mümkün olduğu kadar çok karakterle Eşleştir). Daha fazla bilgi için [eşleşen sıfır veya daha fazla kez](/dotnet/standard/base-types/quantifiers-in-regular-expressions#match-zero-or-more-times-).|*|`a*r` "rack" daki "r", "ark" içinde "ar" ve "aardvark", "aar" ile eşleşir.|
|Sıfır veya daha fazla kez herhangi bir karakterle eşleştir (joker karakter \*)|.*|`c.*e` "comme" "racket", "comment" "comme" ve "Code" ve "code" ile eşleşir.|
|Önünde gelen ifadenin bir veya daha çok tekrarı ile eşleştir (mümkün olduğu kadar çok karakterle Eşleştir). Daha fazla bilgi için [bir veya daha fazla kez eşleştir](/dotnet/standard/base-types/quantifiers-in-regular-expressions#match-one-or-more-times-).|+|`e.+d` "eed" içindeki "eede" ile eşleşir ancak değil "ed" eşleşir.|
|Bir veya daha fazla (joker?) herhangi bir karakterle eşleştir|.+|`e.+e` "eede" ile eşleşir ancak değil "ee" içindeki "eede" ile eşleşir.|
|Önünde gelen ifadenin sıfır veya daha çok tekrarı ile eşleştir (mümkün olduğu kadar az karakterle Eşleştir). Daha fazla bilgi için [sıfır veya daha fazla kez (lazy eşleşme) eşleşen](/dotnet/standard/base-types/quantifiers-in-regular-expressions#match-zero-or-more-times-lazy-match-).|*?|`e.*?e` "eede" ile eşleşir ancak "eede" içinde "ee" ile eşleşir.|
|Önünde gelen ifadenin bir veya daha çok tekrarı ile eşleştir (mümkün olduğu kadar az karakterle Eşleştir). Daha fazla bilgi için [bir veya daha fazla kez (lazy eşleşme) eşleşen](/dotnet/standard/base-types/quantifiers-in-regular-expressions#match-one-or-more-times-lazy-match-).|+?|`e.+?e` "Telefo" ve "erprise" ile "Kurumsal" ancak değil tüm "enterprise" kelimesinin eşleşir.|
|Eşleşme dizesini bağlantı [bir dize veya satır başlangıcı](/dotnet/standard/base-types/anchors-in-regular-expressions#start-of-string-or-line-)|^|`^car` yalnızca satırın başında göründüğünde "car" sözcüğü eşleştirir.|
|Eşleşme dizesini bağlantı [bir satır sonu](/dotnet/standard/base-types/anchors-in-regular-expressions#end-of-string-or-line-)|\r?$|`end\r?$` "yalnızca, bir satırın sonunda göründüğünde end" ile eşleşir.|
|Eşleşme dizesini dosyanın sonuna bağlantı|$|`end$` "yalnızca bu dosyanın sonunda göründüğünde end" ile eşleşir.|
|Bir kümedeki tek bir karakterle eşleştir|[abc]|`b[abc]` "ba", "bb" ve "bc" ile eşleşir.|
|Karakter aralığındaki herhangi bir karakterle eşleştir|[a-f]|`be[n-t]` "içinde"between","beneath"içinde" ben"ve"bes""beside", ancak"below"bet" eşleşir.|
|Yakalama ve parantez içinde yer alan ifadesi örtük olarak numaralandır|()|`([a-z])X\1` "aXa" ve "bXb" ancak değil "aXb" ile eşleşir. "\1", ilk ifade grubu "[a-z]" anlamına gelir.|
|Eşlemeyi geçersiz kıl|(?!abc)|`real(?!ity)` "gerçek" bir "realty" ve "really" eşleşir ancak değil içinde "gerçeklik." Ayrıca ikinci "real" (ancak değil ilk "real") "realityreal" içinde bulur.|
|Belirli bir karakter kümesinde olmayan herhangi bir karakterle eşleş. Daha fazla bilgi için [negatif karakter grubu](/dotnet/standard/base-types/character-classes-in-regular-expressions#negative-character-group-).|[^ abc]|`be[^n-t]` "önce", "behind", "beh" içinde "bef" ile eşleşir ve "BEh" "below", ancak "beneath".|
|Önce ifadesi veya bir sonraki eşleşen|&#124;|`(sponge\|mud) bath` "sponge bath" ve "mud bath" ile eşleşir|
|[Kaçış karakteri](/dotnet/standard/base-types/character-escapes-in-regular-expressions) eğik çizgiyi takip eden| \\ |`\^` bir karakterle eşleşir ^.|
|Önceki karakterin veya grubun oluşum sayısını belirtin. Daha fazla bilgi için [tam olarak n kez eşleştir](/dotnet/standard/base-types/quantifiers-in-regular-expressions#match-exactly-n-times-n).|{n}, burada 'n' oluşum sayısıdır|`x(ab){2}x` "xababx" ile eşleşir ve `x(ab){2,3}x` "xababx" ve "xabababx ile eşleşir" ancak değil "xababababx" ile eşleşir.|
|[Eşleşen bir Unicode kategorisinin metinde](/dotnet/standard/base-types/character-classes-in-regular-expressions#unicode-category-or-unicode-block-p). Unicode karakter sınıfları hakkında daha fazla bilgi için bkz: [Unicode standart 5.2 karakter özellikleri](http://www.unicode.org/versions/Unicode5.2.0/ch04.pdf).|\p{X}, "X" değerinin Unicode numarası olduğu.|`\p{Lu}` "T" ve "Thomas Doe" içinde "D" ile eşleşir.|
|[Bir sözcük sınırını eşleştir](/dotnet/standard/base-types/anchors-in-regular-expressions#word-boundary-b)|\b (bir karakter sınıfı dışında `\b` bir sözcük sınırını belirler ve bir karakter sınıfı içinde `\b` Geri Al ile eşleşir.)|`\bin` "içinde" inside "içinde" değil "pinto" eşleşir.|
|(Yeni bir satır tarafından izlenen diğer bir deyişle, bir satır başı) bir satır sonuyla eşleştir|\r?\n|`End\r?\nBegin` "Son" ve "olduğunda yalnızca"End"bir satırdaki son dizeyse ve"Begin"sonraki satırdaki ilk dizedir Begin" ile eşleşir.|
|Tüm eşleşen [sözcük karakteri](/dotnet/standard/base-types/character-classes-in-regular-expressions#word-character-w)|\w|`a\wd` eşleşme "Ekle" ve "a1d ile eşleşir" ancak "a d".|
|Tüm eşleşen [boşluk karakteri](/dotnet/standard/base-types/character-classes-in-regular-expressions#whitespace-character-s)|\s|`Public\sInterface` ' % s'ifadesinin "Ortak arabirim" ile eşleşir.|
|Tüm eşleşen [ondalık basamak karakteri](/dotnet/standard/base-types/character-classes-in-regular-expressions#decimal-digit-character-d)|\d|`\d` eşleşiyor ve "3", "3456" 23" içinde" 2"ve"1"içinde"1".|
|Unicode karakterini eşleştir|\uXXXX nerede XXXX Unicode karakter değerini belirtir.|`\u0065` "e" karakteriyle eşleşir.|
|Tanımlayıcı eşleştir|\b [\_\w-[0-9]] [\_\w]*\b|Eşleşme "type1" değil "& type1" veya "#define".|
|Tırnak işaretleri içindeki bir dizeyle eşleştir|((\\".+?\\")&#124;('.+?'))|Tek veya çift tırnak içindeki herhangi bir dizeyle eşleşir.|
|Onaltılık bir sayıyla eşleştir|\b0[xX]([0-9a-fA-F]+\)\b|"0xc67f ile eşleşir" değil "0xc67g" ile eşleşir.|
|Eşleşme tamsayıları ve ondalık sayıları|\b[0-9]*\\.\*[0-9]+\b|"1.333" eşleşir.|

> [!TIP]
> Windows işletim sistemlerinde satırların çoğu "\r\n" (bir yeni satırın izlediği bir satır başı) bitmelidir. Bu karakterler görünür değildir ancak düzenleyicide bulunur ve .NET normal ifade hizmetine iletilir.

## <a name="capture-groups-and-replacement-patterns"></a>Yakalama grupları ve değiştirme desenleri

Bir yakalama grubu, normal bir ifadenin bir alt ifade betimleyen ve bir Giriş dizesinin bir alt dizesi yakalar. Normal ifade (örneğin bir yinelenen sözcük,), kendi içinde yakalanan gruplar kullanabilirsiniz veya bir değiştirme deseninde. Ayrıntılı bilgi için bkz. [gruplandırma yapıları normal ifadeler](/dotnet/standard/base-types/grouping-constructs-in-regular-expressions).

Numaralandırılmış yakalama grubu oluşturmak için alt ifade normal ifade deseninde ayraç ile çevreleyin. Yakalamalar, açma parantezi konumunu normal ifadede göre sağa soldan otomatik olarak numaralandırılır. Yakalanan grubu erişmek için:

- **Normal ifade içindeki**: Kullanım `\number`. Örneğin, `\1` normal ifadede `(\w+)\s\1` ilk yakalama grubu başvuruyor `(\w+)`.

- **bir değiştirme deseninde**: Kullanım `$number`. Örneğin, gruplanan normal ifadeyle `(\d)([a-z])` iki grupları tanımlar: ilk grubu tek bir ondalık basamak içeren ve ikinci grubu arasında tek bir karakter içeren **bir** ve **z**. İfade, aşağıdaki dizede dört eşleşme bulur: **1a 2b 3c 4d**. Değiştirme dizesi `z$1` yalnızca ilk grup başvurur (`$1`) ve bir dizeye dönüştürür **z1 z2 z3 z4**.

Bir normal ifade aşağıdaki resimde gösterilmektedir `(\w+)\s\1` ve bir değiştirme dizesi `$1`. Normal ifade hem değiştirme deseni, otomatik olarak 1 numaralı ilk yakalama grubu başvuru. Seçeneğini belirlediğinizde **Tümünü Değiştir** içinde **hızlı Değiştir** iletişim kutusu Visual Studio'da sözcükleri metinden kaldırılır tekrarlanan.

![Visual Studio'da bir numaralandırılmış yakalama grubu gösteren hızlı Değiştir](media/numbered-capture-group.png)

> [!TIP]
> Emin **normal ifadeler kullanmanız** düğmesi seçildiğinde, **hızlı Değiştir** iletişim kutusu.

### <a name="named-capture-groups"></a>Adlandırılmış yakalama grupları

Bir yakalama grubu otomatik numaralandırma üzerinde işlemine güvenmek yerine, bir ad verebilirsiniz. Adlandırılmış yakalama grubu sözdizimi `(?<name>subexpression)`.

Adlandırılmış yakalama gruplar, ister yakalama gruplarının numaralı, normal ifade içinde veya bir değiştirme deseninde kullanılabilir. Adlandırılmış yakalama grubu erişmek için:

- **Normal ifade içindeki**: Kullanım `\k<name>`. Örneğin, `\k<repeated>` normal ifadede `(?<repeated>\w+)\s\k<repeated>` adlı yakalama grubu başvuruyor `repeated` ve, alt ifade `\w+`.

- **bir değiştirme deseninde**: Kullanım `${name}`. Örneğin: `${repeated}`

Örneğin, bir normal ifade aşağıdaki resimde gösterilmektedir `(?<repeated>\w+)\s\k<repeated>` ve bir değiştirme dizesi `${repeated}`. Normal ifade hem değiştirme deseni, adlandırılmış yakalama grubu başvuru `repeated`. Seçeneğini belirlediğinizde **Tümünü Değiştir** içinde **hızlı Değiştir** iletişim kutusu Visual Studio'da sözcükleri metinden kaldırılır tekrarlanan.

![Visual Studio'da bir adlandırılmış yakalama grubu gösteren hızlı Değiştir](media/named-capture-group.png)

> [!TIP]
> Emin **normal ifadeler kullanmanız** düğmesi seçildiğinde, **hızlı Değiştir** iletişim kutusu.

Adlandırılmış yakalama grupları hakkında daha fazla bilgi için bkz. [adlandırılmış eşleşen alt ifadeler](/dotnet/standard/base-types/grouping-constructs-in-regular-expressions#named-matched-subexpressions). Değiştirme desenlerinde kullanılan düzenli ifadeler hakkında daha fazla bilgi için bkz. [normal ifadelerdeki değişimler](/dotnet/standard/base-types/substitutions-in-regular-expressions).

## <a name="see-also"></a>Ayrıca bkz.

- [Normal ifade dili](/dotnet/standard/base-types/regular-expression-language-quick-reference)
- [Metin bulma ve değiştirme](../ide/finding-and-replacing-text.md)

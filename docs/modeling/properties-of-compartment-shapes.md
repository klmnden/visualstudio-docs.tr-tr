---
title: Bölme Şekillerinin Özellikleri
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- vs.dsltools.dsldesigner.compartmentshape
helpviewer_keywords:
- Domain-Specific Language, compartment shape
author: gewarren
ms.author: gewarren
manager: douge
ms.workload:
- multiple
ms.prod: visual-studio-dev15
ms.openlocfilehash: 6a15432e170c814a6e80aebb86a9db31d073a98b
ms.sourcegitcommit: 37fb7075b0a65d2add3b137a5230767aa3266c74
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/02/2019
ms.locfileid: "53835227"
---
# <a name="properties-of-compartment-shapes"></a>Bölme Şekillerinin Özellikleri
Bölme şekilleri bir etki alanı sınıfı bir etki alanına özgü dil görüntülemek için kullanabileceğiniz şekilleri biridir. Genişletin ve bölmeleri daraltın.

 Daha fazla bilgi için [etki alanına özgü bir dili tanımlama nasıl](../modeling/how-to-define-a-domain-specific-language.md). Bu özellikler kullanma hakkında daha fazla bilgi için bkz. [bir etki alanına özgü dili özelleştirme ve genişletme](../modeling/customizing-and-extending-a-domain-specific-language.md).

 Bölme şekilleri aşağıdaki tabloda listelenen özelliklere sahiptir.

|Özellik|Açıklama|Varsayılan|
|-|-|-|
|Varsayılan genişletme daraltma durumu|Varsa `Expanded`, bölmeleri oluşturma gösterilir. Varsa `Collapsed`, bunlar değildir.|Genişletilmiş|
|Dolgu rengi|Bu şeklin dolgu rengi.|Beyaz|
|Dolgu gradyanı modu|Bu şeklin dolgu gradyanı modu.|Yatay|
|Geometri|Bu şeklin (dikdörtgen veya Yuvarlatılmış dikdörtgen) geometri.|Dikdörtgen|
|Varsayılan bağlantı noktalarını içerir|Varsa `True`şeklin üst, alt, sol kullanır ve doğru bağlantı noktaları oluşturulan tasarımcıdaki.|False|
|Tek bir bölme üstbilgi görünür mi|Varsa `False`ve tek bir bölme şekli içeriyor, bölmenin üst bilgisi görünür değil.|Doğru|
|Anahat rengi|Bu şeklin ana hat rengi.|Siyah|
|Ana hat kesik çizgi stili|(Düz, kesik çizgi, nokta, çizgi nokta, çizgi nokta nokta, özel), bu şeklin ana hat kesik çizgi stilinin.|Düz|
|Anahat kalınlığı|Bu şeklin ana hat kalınlığı.|0.03125|
|Metin rengi|Bu şeklin ile ilişkili metin dekoratörleri için kullanılan renk.|Siyah|
|Erişim değiştiricisi|Bölme şekli, erişim düzeyi (`public` veya `internal`).|Ortak|
|Özel Öznitelikler|Bu bölme şekli oluşturulan kaynak kod sınıfı öznitelikler eklemek için kullanılır|\<yok >|
|Çift oluşturur türetilmiş|Varsa `True`, hem temel sınıf hem de (geçersiz kılmalar aracılığıyla özelleştirmeyi desteklemek için) bir kısmi sınıf oluşturulur. Daha fazla bilgi için [geçersiz kılma ve oluşturulan sınıflar genişletme](../modeling/overriding-and-extending-the-generated-classes.md).|False|
|Özel oluşturucu vardır.|Varsa `True`, kaynak kodunda özel bir oluşturucu sağlanacaktır. Daha fazla bilgi için [geçersiz kılma ve oluşturulan sınıflar genişletme](../modeling/overriding-and-extending-the-generated-classes.md).|False|
|Devralma değiştiricisi|Bölme şekli oluşturulan kaynak kodu sınıf devralma türü açıklar (`none`, `abstract` veya `sealed`).|Hiçbiri|
|Temel bölme şekli|Bu şeklin temel sınıf.|(hiçbiri)|
|Ad|Bu şeklin adı.|Geçerli ad|
|Ad Alanı|Bu şeklin ile bağlantılı olan ad alanı.|Geçerli ad alanı|
|Araç İpucu türü|Nasıl bir araç ipucu (sabit, değişken veya hiçbiri) tanımlanır. Fixed ise ardından değerini `Fixed Tooltip Text` özelliği, araç ipucu olarak kullanılır; ardından değişken durumunda, araç ipucu özel kodda tanımlanır.|yok|
|Notlar|Bu şekille ilişkilendirilmiş resmi olmayan notlar.|\<yok >|
|İlk yükseklik|Bu şeklin inç cinsinden başlangıç yüksekliği. Bölme şekilleri için bu üst bilgisi bölümü yalnızca yüksekliğini ve yeniden boyutlandırılamıyor.|1.|
|Başlangıç genişliği|Bu şeklin inç cinsinden başlangıç genişliği.|1,5|
|Özellik olarak kullanıma sunulan dolgu rengi<br /><br /> İfşa edilen dolgu gradyanı modu<br /><br /> Ana hat rengi özellik olarak kullanıma sunulan<br /><br /> Ana hat kesik çizgi stilinin özellik olarak kullanıma sunulan<br /><br /> Anahat kalınlığı özellik olarak kullanıma sunulan<br /><br /> Kullanıma sunan metin rengi|Varsa `True`, kullanıcının belirtilen özelliği bir şeklin ayarlayabilirsiniz. Bunu ayarlamak için Şekil tanımı sağ tıklatıp **ekleme kullanıma sunulan**.|False|
|Açıklama|Oluşturulan tasarımcının belge için kullanılır.|\<yok >|
|Görünen Ad|Bu şekil için oluşturulan tasarımcıda görüntülenecek ad.|\<yok >|
|Sabit araç ipucu metni|Sabit bir araç ipucu için kullanılan metin.|\<yok >|
|Yardım anahtar sözcüğü|Bu şeklin için F1 Yardımı dizini oluşturmak için kullanılan anahtar sözcüğü.|\<yok >|

## <a name="see-also"></a>Ayrıca Bkz.

- [Etki alanına özgü dil araçları sözlüğü](https://msdn.microsoft.com/ca5e84cb-a315-465c-be24-76aa3df276aa)
---
title: Diyagramların özellikleri
ms.date: 10/31/2018
ms.topic: reference
f1_keywords:
- vs.dsltools.dsldesigner.dsldiagram
helpviewer_keywords:
- Domain-Specific Language, diagram
author: gewarren
ms.author: gewarren
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 05c348edfa4665b138ac0f6069b0afaf6735da7a
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62999259"
---
# <a name="properties-of-diagrams"></a>Diyagramların özellikleri
Diyagramları oluşturulan tasarımcıdaki nasıl görüntüleneceğini belirten özellikleri ayarlayabilirsiniz. Örneğin, bir metin için varsayılan rengi diyagramda belirtebilirsiniz.

 Daha fazla bilgi için [etki alanına özgü bir dili tanımlama nasıl](../modeling/how-to-define-a-domain-specific-language.md). Bu özellikler kullanma hakkında daha fazla bilgi için bkz. [özelleştirme ve bir etki alanına özgü dili genişletir](../modeling/customizing-and-extending-a-domain-specific-language.md).

 Aşağıdaki tabloda, diyagramların özellikleri listeler.

|Özellik|Açıklama|Varsayılan|
|-|-|-|
|Dolgu rengi|Diyagramın dolgu rengi.|Beyaz|
|Metin rengi|Diyagram üzerinde görüntülenen metnin rengi.|Siyah|
|Erişim değiştiricisi|Erişim değiştiricisi bir sınıfın (public veya internal).|Ortak|
|Özel Öznitelikler|Oluşturulan kodun sınıf için öznitelikleri eklemek için kullanılır.|\<yok >|
|Çift oluşturur türetilmiş|Varsa `True`, hem temel sınıf hem de (geçersiz kılmalar aracılığıyla özelleştirmeyi desteklemek için) bir kısmi sınıf oluşturulur. Daha fazla bilgi için [geçersiz kılmak ve oluşturulan sınıflar genişletmek](../modeling/overriding-and-extending-the-generated-classes.md).|False|
|Özel oluşturucu vardır.|Varsa `True`, kaynak kodunda özel bir oluşturucu sağlanacaktır. Daha fazla bilgi için [geçersiz kılmak ve oluşturulan sınıflar genişletmek](../modeling/overriding-and-extending-the-generated-classes.md)...|False|
|Devralma değiştiricisi|Devralma diyagramından oluşturulan kaynak kodu sınıf türünü açıklar (`none`, `abstract`, veya `sealed`).|Yok.|
|Temel Diyagram|Bu diyagram, temel sınıf.|(hiçbiri)|
|Ad|Bu diyagram adı.|Geçerli ad|
|Ad Alanı|Bu diyagram ile bağlantılı olan ad alanı.|Geçerli ad alanı|
|Temsil edilen sınıf|Bu diyagramda temsil eden kök etki alanı sınıfı.|Varsa geçerli kök sınıfı|
|Notlar|Bu öğeyle ilişkili resmi olmayan notlar.|\<yok >|
|Özellik olarak kullanıma sunan dolgu rengi|Varsa `True`, kullanıcı oluşturulan tasarımcının diyagramın dolgu rengi ayarlayabilirsiniz. Bu özelliği ayarlamak için diyagramda şekle sağ tıklayın ve **ekleme kullanıma sunulan**.|False|
|Metin rengi özellik olarak kullanıma sunar.|Varsa `True`, kullanıcı diyagramda metin rengini oluşturulan tasarımcıdaki ayarlayabilirsiniz. Bu özelliği ayarlamak için diyagramda şekle sağ tıklayın ve **ekleme kullanıma sunulan**.|False|
|Açıklama|Oluşturulan tasarımcının belgelemek için kullanılan bir açıklaması.|\<yok >|
|Görünen Ad|Bu diyagram için oluşturulan tasarımcıda görüntülenecek ad.|\<yok >|
|Yardım anahtar sözcüğü|Bu diyagram için F1 Yardımı dizini oluşturmak için kullanılan anahtar sözcüğü.|\<yok >|

## <a name="see-also"></a>Ayrıca bkz.

[Etki alanına özgü dil araçları sözlüğü](https://msdn.microsoft.com/ca5e84cb-a315-465c-be24-76aa3df276aa)

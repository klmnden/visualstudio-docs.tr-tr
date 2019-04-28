---
title: Etki Alanı Sınıflarının Özellikleri
ms.date: 11/04/2016
ms.topic: reference
helpviewer_keywords:
- Domain-Specific Language, domain class
author: gewarren
ms.author: gewarren
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: fb66a0d497c86091f689f119e57a5230f125e8de
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62999188"
---
# <a name="properties-of-domain-classes"></a>Etki Alanı Sınıflarının Özellikleri
Etki alanı sınıfları aşağıdaki tabloda özelliklere sahiptir. Etki alanı sınıfları hakkında daha fazla bilgi için bkz: [anlama modelleri, sınıfları ve ilişkileri](../modeling/understanding-models-classes-and-relationships.md). Bu özellikler kullanma hakkında daha fazla bilgi için bkz. [bir etki alanına özgü dili özelleştirme ve genişletme](../modeling/customizing-and-extending-a-domain-specific-language.md).

|Özellik|Açıklama|Varsayılan|
|-|-|-|
|Erişim değiştiricisi|Etki alanı sınıfı, erişim düzeyi (`public` veya `internal`).|`public`|
|Özel Öznitelikler|Bu alan sınıfından oluşturulan kaynak kod sınıfı öznitelikler eklemek için kullanılır.|\<yok >|
|Çift oluşturur türetilmiş|Varsa `True`, hem temel sınıf hem de (geçersiz kılmalar aracılığıyla özelleştirmeyi desteklemek için) bir kısmi sınıf oluşturulur. Daha fazla bilgi için [geçersiz kılma ve oluşturulan sınıflar genişletme](../modeling/overriding-and-extending-the-generated-classes.md).|`False`|
|Özel oluşturucu vardır.|Varsa `True`, kaynak kodunda özel bir oluşturucu sağlanacaktır. Daha fazla bilgi için [geçersiz kılma ve oluşturulan sınıflar genişletme](../modeling/overriding-and-extending-the-generated-classes.md).|`False`|
|Devralma değiştiricisi|Alan sınıfından oluşturulan kaynak kodu sınıf devralma türü açıklar (`none`, `abstract` veya `sealed`).|`none`|
|Temel sınıf|Bu etki alanı sınıfı türetiliyorsa temel sınıfın adı.|\<yok >|
|Ad|Bu alan sınıfının adı.|Geçerli ad|
|Ad Alanı|Bu alan sınıfının ad alanı.|Geçerli ad alanı|
|Notlar|Bu alan sınıfıyla ilişkili resmi olmayan notlar.|\<yok >|
|Açıklama|Belge oluşturulan tasarımcının kullanıcı Arabirimi için kullanılan bir açıklaması.|\<yok >|
|Görünen Ad|Bu etki alanı sınıfı için oluşturulan tasarımcıda görüntülenecek ad.|\<yok >|
|Yardım anahtar sözcüğü|Bu etki alanı sınıfı için F1 Yardımı dizini oluşturmak için kullanılan isteğe bağlı anahtar sözcük.|\<yok >|

## <a name="see-also"></a>Ayrıca Bkz.

- [Etki alanına özgü dil araçları sözlüğü](https://msdn.microsoft.com/ca5e84cb-a315-465c-be24-76aa3df276aa)
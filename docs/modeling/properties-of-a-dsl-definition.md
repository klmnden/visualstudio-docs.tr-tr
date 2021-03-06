---
title: DSL Tanımının Özellikleri
ms.date: 11/04/2016
ms.topic: reference
helpviewer_keywords:
- Domain-Specific Language, definition file
author: gewarren
ms.author: gewarren
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: e63a5ab794261a395fb091016f177ffca9d35692
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62964306"
---
# <a name="properties-of-a-dsl-definition"></a>DSL Tanımının Özellikleri
DslDefinition özelliklerini tanımlayın *etki alanına özgü dil* sürümü numaralandırma gibi tanımı özellikleri. DslDefinition özellikleri görünür **özellikleri** pencere, diyagramdaki boş bir alanı tıkladığınızda *etki alanına özgü dil tasarımcısını*.

 Daha fazla bilgi için [etki alanına özgü bir dili tanımlama nasıl](../modeling/how-to-define-a-domain-specific-language.md). Bu özellikler kullanma hakkında daha fazla bilgi için bkz. [bir etki alanına özgü dili özelleştirme ve genişletme](../modeling/customizing-and-extending-a-domain-specific-language.md).

 DslDefinition aşağıdaki tabloda özelliklere sahiptir:

|Özellik|Açıklama|Varsayılan|
|-|-|-|
|Erişim değiştiricisi|Alan sınıfına ait erişim değiştiricisinin public veya internal olduğunu belirler.|public|
|Özel Öznitelikler|Özel öznitelikler etki alanı sınıfı için tanımlanmış.<br /><br /> **Not** bir öznitelik eklemek için Gözat düğmesini kullanın.|\<yok >|
|Şirket adı|Sistem kayıt defterinde geçerli şirket adı adı.|Geçerli bir şirket adı|
|Ad|Bu alan sınıfının adı.|Geçerli ad|
|Ad Alanı|Bu alan sınıfıyla ilişkili ad alanı.|Geçerli ad alanı|
|Paket GUID'si|Bu DSL için oluşturulan Visual Studio Paket guid'i.|\<yok >|
|Paket Namespace|Bu DSL için oluşturulan Visual Studio paketinin ad alanı.|\<yok >|
|Ürün Adı|Bu DSL için oluşturulan Visual Studio paketine kaydedilecek ürünün adı.|\<yok >|
|Notlar|Bu alan sınıfıyla ilişkili notları.|\<yok >|
|Açıklama|Bu etki alanı sınıfı için açıklama.|\<yok >|
|Görünen Ad|Bu etki alanı sınıfı için oluşturulan tasarımcıda görüntülenecek ad.|\<yok >|
|Yardım anahtar sözcüğü|Bu alan sınıfıyla ilişkili Yardım anahtar sözcüğü.|\<yok >|
|Yapı|Bu etki alanına özgü dil tanımı için artımlı derleme numarası.|0|
|Ana sürüm|Bu etki alanına özgü dil tanımı için artımlı başlıca yapı numarası.|1.|
|Alt sürüm|Bu etki alanına özgü dil tanımı için artımlı alt yapı numarası.|0|
|Gözden geçirme|Artımlı düzeltme numarası için bu etki alanına özgü dil tanımı oluşturun.|0|

## <a name="see-also"></a>Ayrıca Bkz.

- [Etki alanına özgü dil araçları sözlüğü](https://msdn.microsoft.com/ca5e84cb-a315-465c-be24-76aa3df276aa)
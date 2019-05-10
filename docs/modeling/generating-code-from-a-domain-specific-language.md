---
title: Etki Alanına Özgü Dilden Kod Oluşturma
ms.date: 11/04/2016
ms.topic: conceptual
author: gewarren
ms.author: gewarren
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 37c60ed42e7d4a7604dc3d99f7e0311c7000b99c
ms.sourcegitcommit: 6a19c5ece38a70731496a38f2ef20676ff18f8a4
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/09/2019
ms.locfileid: "65476518"
---
# <a name="generating-code-from-a-domain-specific-language"></a>Etki Alanına Özgü Dilden Kod Oluşturma

Microsoft [!INCLUDE[dsl](../modeling/includes/dsl_md.md)] modellerinde temsil verilerden kod, belgeler, yapılandırma dosyalarını ve diğer yapıları üretmek için güçlü bir yol sağlar. Kullanarak [!INCLUDE[dsl](../modeling/includes/dsl_md.md)], verilerinizi temsil eden sınıf kümesi oluşturabileceğiniz ve adları sınıflarda metin şablonlarınızı yazabilirsiniz ve özellikleri, bu verileri yansıtır.

Örneğin, Fabrikam, müşteri adları ve e-posta adreslerini bir XML dosyası vardır. Geliştiricileri, müşteri özellikleri adı ve e-posta ile bir sınıf olan bir modeli oluşturun. Bunlar, bir HTML sayfasının parçası tüm müşteriler tablosunu oluşturan bu parça içeren verileri işlemek için çeşitli metin şablonlarını yazma:

```
<table>
<# foreach (Customer c in ContactList) {  #>
  <tr><td> <#= c.FullName #> </td>
      <td> <#= c.EmailAddress #> </td> </tr>
<# } #>  </table>
```

Müşteri veritabanı işlendiğinde, XML dosyasını modeli deposuna okunur. A *yönerge işlemcisi*, kullanılarak oluşturulan [!INCLUDE[dsl](../modeling/includes/dsl_md.md)], müşteri sınıfı metin şablonunun kod için kullanılabilir hale getirir. Birçok metin şablonları aynı deponun karşı çalıştırabilirsiniz.

Metin şablonları için temel [!INCLUDE[dsl](../modeling/includes/dsl_md.md)]. VSPackage'ı ve araçları, Visual Studio ile tümleştirmek için kullanılan denetimler de etki alanı model öğeleri için kaynak kodunu oluşturmak için kullanılır.

Bu bölümde oluşturmak, değiştirmek ve metin şablonları kullanılan hata ayıklama için yollardan bazılarını ele alınmaktadır [!INCLUDE[dsl](../modeling/includes/dsl_md.md)].

## <a name="in-this-section"></a>Bu Bölümde

[Metin şablonlarından modellere erişme](../modeling/accessing-models-from-text-templates.md)\
Metin şablonlarında etki alanına özgü dil başvurma hakkında temel bilgiler sağlar.

[İzlenecek yol: Bir modele erişen metin şablonunda hata ayıklama](../modeling/walkthrough-debugging-a-text-template-that-accesses-a-model.md)\
Bir etki alanına özgü dil başvuran bir metin şablonunda hata ayıklama ve sorun giderme yapılacağını açıklar.

[İzlenecek yol: Üretilen bir yönerge işlemcisine ana bilgisayar bağlama](../modeling/walkthrough-connecting-a-host-to-a-generated-directive-processor.md)\
Özel bir ana bilgisayar üretilen bir yönerge işlemcisine bağlama açıklar.

[DslTextTransform komutu](../modeling/the-dsltexttransform-command.md)\
Etki alanına özgü diller başvuru metin şablonları için komut satırında TextTransform yürütülebilir dosyayı çalıştırır komut dosyası açıklanmaktadır.

## <a name="reference"></a>Başvuru

[T4 metin şablonu yazma](../modeling/writing-a-t4-text-template.md)\
Metin şablonu yönergeleri ve denetim blokları söz dizimi sağlar.

## <a name="related-sections"></a>İlgili Bölümler

[T4 metin şablonları kullanarak tasarım zamanı kodu oluşturma](../modeling/design-time-code-generation-by-using-t4-text-templates.md)\
Metin şablonu dönüştürme süreci açıklanmaktadır.

[Derleme sürecinde kod oluşturma](../modeling/code-generation-in-a-build-process.md)\
Bir DSL bir yapı sunucusunda gelen dosyaları oluşturuyorsanız bu konuyu okuyun.
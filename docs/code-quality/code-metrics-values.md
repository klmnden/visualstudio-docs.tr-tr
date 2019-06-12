---
title: Kod ölçümlerini Hesapla
ms.date: 11/02/2018
ms.topic: conceptual
helpviewer_keywords:
- code metrics [Visual Studio]
author: gewarren
ms.author: gewarren
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 960c2b546abe3554a5912efde9bd09bb5b2189b7
ms.sourcegitcommit: cc5fd59e5dc99181601b7db8b28d7f8a83a36bab
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/11/2019
ms.locfileid: "66835956"
---
# <a name="code-metrics-values"></a>Kod ölçüm değerleri

Artan karmaşıklık modern yazılım uygulamaları, kodu güvenilir ve sürdürülebilir hale getirme zorluk da artırır. Kod ölçümleri, geliştiricilere, geliştirdikleri daha iyi bir anlayış kod sağlayan yazılım ölçü kümesidir. Kod ölçümleri avantajlarından yararlanarak, geliştiriciler hangi türleri ve/veya yöntemleri yeniden işledi veya daha kapsamlı test anlayabilirsiniz. Geliştirme ekipleri olası riskleri belirlemek, bir proje geçerli durumunu anlamanıza ve yazılım geliştirme sırasında ilerlemeyi.

Geliştiriciler Visual Studio, karmaşıklığı ve bakımı, yönetilen kodun ölçüm kod ölçümleri verileri üretme için kullanabilirsiniz. Bütün bir çözüm ya da tek bir proje için kod ölçümleri verileri oluşturulabilir.

Visual Studio'da kod ölçümleri verileri üretme hakkında daha fazla bilgi için bkz: [nasıl yapılır: Kod ölçümleri verileri üretme](../code-quality/how-to-generate-code-metrics-data.md).

## <a name="software-measurements"></a>Yazılım ölçümleri

Aşağıdaki liste, kodu Visual Studio hesaplar ölçümleri sonuçları gösterir:

- **Bakım dizini** -0 ile 100 arasında göreceli bir kolayca kod bakım temsil eden dizin değeri hesaplar. Yüksek bir değer daha iyi bakım anlamına gelir. Renk kodlu derecelendirmeleri, hızlı bir şekilde kodunuzda sorunlu noktaları tanımlamak için kullanılabilir. Yeşil bir derecelendirme 20 ile 100 arasında ve kod iyi bakım sahip olduğunu gösterir. Sarı bir derecelendirme 10 ile 19 arasında ve kod oldukça sürdürülebilir olduğunu gösterir. Kırmızı derecesi 0 ile 9 arasında bir derecelendirme ve düşük bakım belirtir. Daha fazla bilgi için [bakım dizini aralığı ve anlamı](https://blogs.msdn.microsoft.com/codeanalysis/2007/11/20/maintainability-index-range-and-meaning/) blog gönderisi.

- **Döngüsel karmaşıklık** -kod yapısal karmaşıklığını ölçer. Program akışını farklı kod yollarında sayısını hesaplayarak oluşturulur. Karmaşık denetim akışı olan bir program iyi kod kapsamını elde etmek için daha fazla test gerektirir ve daha az sürdürülebilir. Daha fazla bilgi için [döngüzel karmaşıklığına Wikipedia girişini](https://wikipedia.org/wiki/Cyclomatic_complexity).

- **Devralma derinliği** -birbirine, tüm sürümlerde temel sınıfa devralınan farklı sınıflar sayısını gösterir. Devralma derinliği, devralınan sınıflar herhangi bir temel sınıf bir değişiklik etkileyebilir, eşlenmesiyle sınıfına benzer. Bu sayı, daha derin arttıkça devralma ve temel sınıf değişiklikleri bir bölme içinde elde etmek için yüksek olası değiştirin. Devralma derinliği için düşük bir değere iyidir ve yüksek bir değer bozuk.

- **Sınıf bağlantısından** -bağlantı parametreleri, yerel değişkenler, dönüş türleri, yöntem çağrılarını, genel veya şablon örneklemeleri, temel sınıflar, arabirim uygulamalarını, dış türlerinde tanımlanan alanların benzersiz sınıflarına ölçer ve özniteliği düzenleme. İyi yazılım tasarımı, türleri ve yöntemleri uyumun yüksek olması sahip ve eşlenmesiyle düşük olduğunu belirler. Yüksek bağlantısından yeniden kullanabilir ve diğer türleri, birçok bağımlılıkları nedeniyle korumak zor bir tasarımın belirtisidir. Daha fazla bilgi için [sınıf bağlantısından](https://blogs.msdn.microsoft.com/zainnab/2011/05/25/code-metrics-class-coupling/) blog gönderisi.

- **Kod satırlarını** -yaklaşık kod içinde satır sayısını belirtir. Sayısı IL kodunu alır ve bu nedenle satır kaynak kodu dosyasının tam sayı değil. Yüksek bir sayı, bir türün veya yöntemin çok fazla iş yapmak çalışıyor ve bölünmesi gösterebilir. Ayrıca, tür veya yöntem korumak zor olabilir gösterebilir.

   > [!NOTE]
   > [Komut satırı sürüm](../code-quality/how-to-generate-code-metrics-data.md#command-line-code-metrics) IL yerine kaynak kodunu analiz için kodunu gerçek kod satırlarını ölçümleri araç sayar.

## <a name="anonymous-methods"></a>Anonim yöntemler

Bir *anonim yöntem* ada sahip bir yöntem. Anonim yöntemler, en sık temsilcinin parametre olarak bir kod bloğu geçirmek için kullanılır. Bir yöntem veya erişimci gibi yöntemi bildiren bir üye ile ilişkili bir üyesi bildirilen anonim bir yöntem için kod ölçümleri sonuçları. Bunlar, bu yöntemi çağıran bir üye ile ilişkili değildir.

## <a name="generated-code"></a>Oluşturulan kod

Bazı yazılım araçları ve derleyicileri, bir projeye eklenir ve proje Geliştirici görmezsiniz veya değiştirme kod oluşturur. Çoğunlukla, ölçüm değerleri hesaplarken kod ölçümleri oluşturulmuş kodu yoksayar. Bu, hangi geliştirici bakın ve değiştirme yansıtacak şekilde ölçüm değerleri sağlar.

Geliştirici bakın ve değiştirme kodu olduğundan Windows Forms için oluşturulan kodu yok sayıldı değil.

## <a name="next-steps"></a>Sonraki adımlar

- [Nasıl yapılır: Kod ölçümleri verileri üretme](../code-quality/how-to-generate-code-metrics-data.md)
- [Kod ölçümleri sonuçları penceresini kullanma](../code-quality/working-with-code-metrics-data.md)

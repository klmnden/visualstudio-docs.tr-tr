---
title: MSBuild sözlüğü | Microsoft Docs
ms.date: 11/04/2016
ms.topic: reference
ms.assetid: f767d8e4-24d8-4803-80eb-e857202dbe2c
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: f074bf7b5c7077b1c4808d7d3035be0c6366d526
ms.sourcegitcommit: d0425b6b7d4b99e17ca6ac0671282bc718f80910
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/21/2019
ms.locfileid: "56642722"
---
# <a name="msbuild-glossary"></a>MSBuild sözlüğü
Bu terimler Microsoft Build Engine (MSBuild) ve bileşenlerini açıklamak için kullanılır.

## <a name="glossary"></a>Sözlük
 Üçüncü taraf satıcılarından yolları başvuru derlemelerini bulmak için tasarım zamanı çözünürlüğü burada bakabilirsiniz destekledikleri framework'ün her sürümü için depoladığınız AssemblyFoldersEx bir kayıt defteri konumu.

 Toplu işleme toplu işleme anlamına gelir öğeleri olarak bilinen farklı kategorilere ayırma *toplu*öğe meta verileri ve bir hedef veya görevi bir kez her batch kullanarak çalıştırarak göre. MSBuild denk olan toplu işleme için--yapısı döngü. Daha fazla bilgi için [toplu işleme](../msbuild/msbuild-batching.md).

 MSBuild nesneyi, potansiyel olarak görünür, bir proje ve birden çok proje yapı içinde oluşturulan tüm alt projeler için örneğin, bir genel özellikse, yapı kapsamını derleme kapsamı açıklar.

 alt projenin bakın *proje, alt*.

 Koşul birçok MSBuild öğeleri koşullu olarak tanımlanabilir; diğer bir deyişle, `Condition` özniteliği öğesinde görünür. Koşullu öğelerin içeriği, koşul olarak değerlendirilmedikçe yoksayılır `true`. Daha fazla bilgi için [koşullar](../msbuild/msbuild-conditions.md).

 bkz: öğe tanımı *öğe tanımı*.

 öğesi bir derleme yürütme aşamasında yayma, öğeleri oluşturulan ya da alt görevleri tarafından değiştirilen `Output` olan öğeler `ItemName` özniteliği. Görev "Yeni öğeleri göstermek için" kabul edilir.

 özelliği bir derleme yürütme aşamasında yayma, özellikleri oluşturan ya da alt görevleri tarafından değiştirilen `Output` olan öğeler `PropertyName` özniteliği. Görev "yeni özellik yaymak için" kabul edilir.

 Değerlendirme proje derlemesi ilk aşaması olan değerlendirme aşaması. Tüm özellikleri ve öğeleri projede göründükleri sırayla değerlendirilir. İçeri aktarılan projeleri, projede karşılaştığından değerlendirilir. Değerlendirme sırasında yürütme aşamasında ve özellikleri veya yayma bildirmek veya musunuz öğeleri göz ardı edilir kadar hedefler ve görevler çalıştırılmaz.

 yürütme aşaması yürütme proje derlemesi ikinci aşamasıdır. Seçilen hedefler oluşturulur ve görevleri çalıştırma. Özellikleri ve öğeleri oluşturan veya değiştiren değerlendirme değerlerine kıyasla.

 işlev, özellik bakın *özelliği işlevi*.

 işlevi, öğesi öğe işlevi bakın.

 öğesi öğeleri, derleme sistemine girişleri ve öğe adlarına dayalı öğe türlerine gruplanır. Öğeleri genelde dosyaları temsil ederler. Öğeleri öğe türüne göre adlandırılır çünkü koşulları, ait oldukları *öğesi* ve *öğe değeri* birbirlerinin yerine kullanılabilir. Daha fazla bilgi için [öğeleri](../msbuild/msbuild-items.md).

 öğe tanımı öğe tanımı gruplarındaki herhangi bir öğesi türü için varsayılan meta veri ekleme öğesi tanımları içerir. İyi bilinen meta verileri gibi varsayılan meta veri belirtilen öğe türündeki tüm öğeleri ile ilişkilidir. Varsayılan meta veri açıkça bir öğe tanımında geçersiz kılınabilir. Daha fazla bilgi için [öğesi tanımları](../msbuild/item-definitions.md).

 öğe işlevi öğesi işlevleri, projede öğeleri hakkında bilgi alın. Bu işlevler, başlangıç Distinct() öğeleri basitleştirin ve öğeler arasında döngü daha hızlıdır. Öğe yolları ve dizeleri işlemek için işlevi vardır. Daha fazla bilgi için [öğe işlevleri](../msbuild/item-functions.md)

 bkz: meta veri öğesi *meta öğesi*.

 öğe türü öğesi türleri parametre olarak görevleri için kullanılabilir öğe listeleri içeren adlandırılır. Görevler, derleme işleminin adımları gerçekleştirmek için öğe değerlerini kullanın. Daha fazla bilgi için [öğeleri](../msbuild/msbuild-items.md).

 meta verileri, bir öğe ile ilişkili ad-değer çiftleri koleksiyonu öğesi öğe meta verilerdir. Meta veri öğesi için açıklayıcı bilgiler sağlar ve iyi bilinen meta verileri dışında isteğe bağlıdır. Daha fazla bilgi için [öğeleri](../msbuild/msbuild-items.md).

 meta verileri, önceden tanımlanmış bir değer kullanılarak başlatılır salt okunur öğe meta verileri iyi bilinen iyi bilinen meta verilerdir. İyi bilinen meta verileri bir dosyaya başvuran bir öğe için açıklayıcı bilgileri sağlar. Örneğin, adlı iyi bilinen meta veri değeri `FullPath` başvurulan dosyasının tam yoludur. Daha fazla bilgi için [öğeleri](../msbuild/msbuild-items.md).

 Çoklu hedefleme yeteneği için birçok farklı CLR'nin ve MSBuild ve Visual Studio'dan çerçeveleri hedeflemek bir derleme veya uygulama projesi.

 Framework'ün tamamını bir alt kümesi profil. Bu, bir makineye indirilmesi gereken miktarı en aza indirmek için kullanılır.

 Proje dosyası bir proje dosyası denetleyen yapı MSBuild komut dosyası içerir. Proje dosyaları, genellikle ile biten bir dosya uzantısına sahip *proj*, gibi *.csproj* veya *.vbproj*. Proje dosyaları, özellik dosyaları ve hedef dosyalarını içe.

 Bir özellik, derleme işlemini denetlemek için kullanılan bir anahtar-değer çifti özelliğidir. Daha fazla bilgi için [MSBuild özellikleri](../msbuild/msbuild-properties.md).

 özelliği, ortam ortam özelliği aynı ada sahip bir sistem ortam değişkeninin değeri için otomatik olarak başlatılan bir özelliktir. Daha fazla bilgi için [MSBuild özellikleri](../msbuild/msbuild-properties.md).

 özellik dosyası bir özellik dosyası çoğunlukla özelliği grupları ve yapıya rehberlik öğesi gruplarını içeren bir proje dosyasıdır. İsteğe bağlı olarak kural olarak, dosya uzantısına sahip *.props*. Özellik dosyaları genellikle ilişkili proje dosyalarını başlangıcında alınır.

 işlevi bir özellik işlevi bir sistem özelliği veya MSBuild komut değerlendirmek için kullanılan yöntemin özelliğidir. Özellik yöntemleri, sistem saatini okuyabilir, dizeleri karşılaştırmak, normal ifadeleri eşleştirebilir ve diğer eylemleri gerçekleştirmek için kullanılabilir. Daha fazla bilgi için [özellik işlevleri](../msbuild/property-functions.md).

 özellik işlevi, iç içe özellik işlevleri birleştirilebilir için form daha karmaşık işlevleri. Örneğin,

 `$([MSBuild]::BitwiseAnd(32,   $([System.IO.File]::GetAttributes(tempFile))))`

 Daha fazla bilgi için [özellik işlevleri](../msbuild/property-functions.md).

 özelliği, genel derleme işlemini denetlemek için kullanılan bir anahtar-değer çifti genel bir özelliktir. Genel özellikleri kullanarak veya bir komut isteminde ayarlama `Properties` özniteliği bir [MSBuild görevi](../msbuild/msbuild-task.md)ve bir yapının değerlendirme aşamasında değiştirilemez. Daha fazla bilgi için [MSBuild özellikleri](../msbuild/msbuild-properties.md).

 özelliği, yerel yerel yapı işlemini denetlemek için kullanılan bir anahtar-değer çifti özelliğidir. Bu terim, yalnızca bir genel özellikse olmayan bir özelliğe ayırt etmek için kullanılır.

 özelliği, kayıt defteri bir kayıt defteri özelliği sistem kayıt defteri alt anahtarının değeri okuyan bir özel sözdizimi kullanılarak ayarlanan bir değere sahip. Daha fazla bilgi için [MSBuild özellikleri](../msbuild/msbuild-properties.md).

 özelliği, ayrılmış bir özellik derleme işlemini denetlemek için kullanılan bir anahtar-değer çiftidir ayrılmış. Ayrılmış özellikler için önceden tanımlanmış değerler otomatik olarak başlatılır. Daha fazla bilgi için [MSBuild özellikleri](../msbuild/msbuild-properties.md).

 proje kapsamı proje kapsamı yalnızca içeren proje dosyası ve bunu içe aktaran tüm projeleri için görünür olan gibi yerel bir özellik, bir MSBuild nesne açıklar.

 Proje alt bir alt proje, Proje yapı sırasında MSBuild görevi tarafından oluşturulur. Bu yeni proje, projenin içeren veya MSBuild görevi içeren hedef alır bir alt öğesidir. Tarafından değiştirilmediği sürece alt projenin ana proje genel özelliklerini devralır `Properties` özniteliği.

 listeyi yeniden dağıtım listesidir: belirli bir çerçeve için karşılık gelen derleme listesi.

 başvuru bütünleştirilmiş kodu tasarım zamanında bir uygulama oluşturmak için kullanılan bir derleme. Başvuru bütünleştirilmiş kodu özel arabirimler kendisinden kaldırıldı ve gerçek kod, yalnızca meta veri ve ortak arabirimler bırakarak sahip olabilir.

 kayıt defteri özelliği bakın *özelliği, kayıt defteri*.

 Bir hedef, görevler, belirli bir sıraya göre gruplandıran ve proje dosyasının bölümlerini derleme işlemine giriş noktaları olarak kullanıma sunar. Daha fazla bilgi için [hedefleri](../msbuild/msbuild-targets.md).

 Hedef, çalışan, bkz: hedef oluşturma.

 Hedef, artımlı derleme nedeniyle değerlendiriliyor, hedefleri olası değişiklikler için özellikleri ve öğeleri çözümlenmesi gerekir. Hedef atlandı olsa bile, bu değişikliklerin yapılması gerekir. Bir hedef değerlendirirken bu analizini gerçekleştirme ve bu değişiklikler yapmayı anlamına gelir. Daha fazla bilgi için [artımlı derlemeleri](../msbuild/incremental-builds.md).

 Hedef, bir hedef yürütme yürütülürken, değerlendirme ve hiç koşul sahip olan veya, koşul true olarak değerlendirilen tüm görevleri yürütme anlamına gelir. Artımlı derleme sırasında hedef atlandı veya yürütülen, ancak bunlar her zaman değerlendirilir. Daha fazla bilgi için hedef, değerlendirme.

 false değerlendiren bir koşul olan hedef çalıştıran hedef, yani çalıştırılmaz, derleme üzerinde hiçbir etkisi olmaz. Hedefleri çalıştırın ya da çalıştırılan atlandı veya. Her iki durumda da, hedef olarak değerlendirilir. Daha fazla bilgi için hedef, değerlendirme.

 Hedef, artımlı derleme, tüm çıktı dosyalarının güncel olduğundan sonra hedef atlandı, diğer bir deyişle, hedef değerlendirilir, ancak hedef içindeki görevlerin yürütülmez olduğunu belirlerse, atlanıyor. Daha fazla bilgi için hedef, değerlendirme.

 Hedef Çerçeve adı (örneğin,. framework tanımlayan bir adı NETFramework, Silverlight, vb.), sürüm ve hedeflemek istediğiniz profil (örneğin, istemci, sunucu, vb.).

 targeting Pack listenin belirtilen bir çerçeve ve bu çerçeve için başvuru bütünleştirilmiş kodları kümesi ile dağıtılmış bir derleme.

 çoğunlukla hedefler ve yapıya rehberlik görevleri içeren bir proje dosyası hedefler dosyası bir hedefleri dosyasıdır. İsteğe bağlı olarak kural olarak, dosya uzantısına sahip *.targets*. Hedef dosyalar genellikle ilişkili proje dosyalarını sonunda içeri aktarılır.

 Görev görevleridir yürütülebilir koddur, [!INCLUDE[vstecmsbuild](../extensibility/internals/includes/vstecmsbuild_md.md)] projeleri derleme işlemlerini gerçekleştirmek için kullanın. Örneğin, bir görev giriş dosyalarını derleyebilir ya da bir harici araç çalıştırabilir. Daha fazla bilgi için [görevleri](../msbuild/msbuild-tasks.md).

 dönüştürme bir dönüştürme, başka bir öğe koleksiyonuna bire bir dönüştürmedir. Öğe koleksiyonlarını dönüştürmek bir proje etkinleştirmeye ek olarak, bir dönüştürme giriş ve çıkışlarını arasında doğrudan bir eşleme tanımlamak bir hedef sağlar. Daha fazla bilgi için [dönüştüren](../msbuild/msbuild-transforms.md).

 iyi bilinen meta verilere bakın *iyi bilinen meta*.

## <a name="see-also"></a>Ayrıca bkz.
- [MSBuild](../msbuild/msbuild.md)
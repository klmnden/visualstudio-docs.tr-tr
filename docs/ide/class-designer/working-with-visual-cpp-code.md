---
title: Visual C++ Kodu ile Çalışma (Sınıf Tasarımcısı)
ms.date: 06/21/2017
ms.prod: visual-studio-dev15
ms.topic: conceptual
f1_keywords:
- vs.classdesigner.cpplimitation
helpviewer_keywords:
- Visual C++, Class Designer
- Class Designer, Visual C++ support
- Class Designer, limitations
- Class Designer, tasks in Visual C++
- Visual C++, class diagrams
- C++, class diagrams
- C++, Class Designer
ms.assetid: f5b40921-2ef7-4de0-b595-45b44c79ffa6
author: gewarren
ms.author: gewarren
manager: jillfra
ms.workload:
- cplusplus
ms.openlocfilehash: 1497730cf7c2b2e9abc17ec6cb82179deebb30d7
ms.sourcegitcommit: 2193323efc608118e0ce6f6b2ff532f158245d56
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/25/2019
ms.locfileid: "54948056"
---
# <a name="work-with-visual-c-code-in-class-designer"></a>Sınıf tasarımcısında Visual C++ kod ile çalışma

**Sınıf Tasarımcısı** adlı bir görsel tasarım yüzeyi görüntüler bir *sınıf diyagramı* kod öğeleri, projenizdeki görsel bir gösterimini sağlar. Tasarım ve sınıflar ve diğer proje türleri görselleştirmek için sınıf diyagramlarını kullanabilirsiniz.

**Sınıf Tasarımcısı** aşağıdaki C++ kod öğeleri destekler:

- (Birden çok devralma ilişkisi olabilir bir yönetilen sınıf şeklinin benzer) sınıfı

- Anonim sınıf (anonim tür sınıfı görünümün oluşturulan adını görüntüler.)

- Şablon sınıfı

- Yapı

- Enum

- Makro (makro sonrası işlenen görünümünü görüntüler)

- tür tanımı

> [!NOTE]
> Bu bir modelleme projesinde oluşturduğunuz UML sınıf diyagramı ile aynı değildir. Daha fazla bilgi için [UML Class Diagrams: Başvuru](../../modeling/create-uml-modeling-projects-and-diagrams.md).

## <a name="troubleshoot-type-resolution-and-display-issues"></a>Tür çözümlemesi ilgili sorunları gidermek ve sorunları görüntüle

### <a name="location-of-source-files"></a>Kaynak dosyalarının konumu

**Sınıf Tasarımcısı** kaynak dosyalarının konumunu izler mi değil. Bu nedenle, proje değiştirmek ya da kaynak dosyalarını projenizde, taşıma **Sınıf Tasarımcısı** parça türü (özellikle kaynak türü bir tür tanımı, temel sınıflar veya ilişki türlerini) kaybedebilir. Gibi bir hata alabilirsiniz **Sınıf Tasarımcısı bu türü görüntüleyemiyor**. Bunu yaparsanız, değiştirilmiş ya da yeni yerlerine kaynak kodu yeniden görüntülemek için sınıf diyagramına sürükleyin.

### <a name="update-and-performance-issues"></a>Güncelleştirme ve performans sorunları

Visual C++ projeleri için sınıf diyagramında görüntülenecek kaynak dosyada bir değişiklik 30 ila 60 saniye sürebilir. Bu gecikmeye de neden **Sınıf Tasarımcısı** hata vermesini **hiçbir tür seçiminde bulundu**. Bunun gibi bir hata alırsanız, tıklayın **iptal** hata iletisi ve bekleme görünmesini kod öğesi için **sınıf görünümü**. Bu yapıldıktan sonra **Sınıf Tasarımcısı** görüntüleyebilir türü olmalıdır.

Bir sınıf diyagramı, kodda yaptığınız değişikliklerle güncelleştirmezse diyagramı kapatın ve yeniden açın gerekebilir.

### <a name="type-resolution-issues"></a>Tür çözümlemesi sorunları

**Sınıf Tasarımcısı** türleri aşağıdaki nedenlerden dolayı çözmek mümkün olmayabilir:

- Bir proje veya sınıf diyagramı içeren bir projeden başvurulan değil derleme türüdür. Bu hatayı düzeltmek için proje ya da türünü içeren derlemeyi bir başvuru ekleyin. Daha fazla bilgi için [bir projedeki başvuruları yönetme](../managing-references-in-a-project.md).

- Türü doğru kapsamda, bu nedenle değil **Sınıf Tasarımcısı** yeri belirlenemiyor. Kodu eksik olmadığından emin olun bir `using`, `imports`, veya `#include` deyimi. Ayrıca, türü (veya ilişkili bir türün) içinde bulunduğu orijinal yere ad alanı dışında taşınmış değil, emin olun.

- Türü yok (veya açıklama satırı). Bu hatayı düzeltmek için bilgisayarınızda değil yorum veya türü silinmiş olması emin olun.

- Türü bir #import yönergesi tarafından başvurulan bir kitaplıkta yer alır. İçin oluşturulan kodu (.tlh dosyası) el ile eklemek için olası bir geçici çözüm olan bir # üstbilgi dosyasına include yönergesi.

- Emin **Sınıf Tasarımcısı** girdiğiniz türünü destekler. Bkz: [C++ kod öğeleri için kısıtlamalar](#limitations-for-c-code-elements).

Tür çözümleme sorunu için görmek en olası hata **kodu sınıf diyagramına bir veya daha fazla şekilleri için bulunamadı '\<öğesi >'**. Bu hata iletisini kodunuzu hatadır gelmeyebilir. Bu, Sınıf Tasarımcısı yalnızca kodunuzu görüntüleyemedi gösterir. Aşağıdaki ölçüleri deneyin:

- Türü olduğundan emin olun. Yanlışlıkla değil yorum veya kaynak kodu silinmiş olduğundan emin olun.

- Türü çözmeye çalışın. Bir proje ya da sınıf diyagramı içeren bir projeden başvurulan değil derleme türü olabilir. Bu hatayı düzeltmek için proje ya da türünü içeren derlemeyi bir başvuru ekleyin. Daha fazla bilgi için [bir projedeki başvuruları yönetme](../managing-references-in-a-project.md).

- Sınıf Tasarımcısı bulabilmesi türü doğru kapsamda olduğundan emin olun. Kodu eksik olmadığından emin olun bir `using`, `imports`, veya `#include` deyimi. Ayrıca, türü (veya ilişkili bir türün) içinde bulunduğu orijinal yere ad alanı dışında taşınmış değil, emin olun.

### <a name="troubleshoot-other-error-messages"></a>Diğer hata iletilerinde sorun giderme

Microsoft Developer Network (MSDN) ortak forumlarında sorun giderme hataları ve Uyarıları ile ilgili Yardım bulabilirsiniz. Bkz: [Visual Studio Sınıf Tasarımcısı Forumu](http://go.microsoft.com/fwlink/?linkid=160754).

## <a name="limitations-for-c-code-elements"></a>C++ kod öğeleri için kısıtlamalar

- Bir Visual C++ proje yüklendiğinde **Sınıf Tasarımcısı** salt okunur şekilde işlevleri. Sınıf diyagramı değiştirebilirsiniz, ancak sınıf diyagramından kaynak koduna değişiklikleri kaydedemezsiniz.

- **Sınıf Tasarımcısı** yalnızca yerel C++ semantiği destekler. Yönetilen kod derlenmiş Visual C++ projeleri için **Sınıf Tasarımcısı** yalnızca yerel türler kod öğelerini görselleştirin. Bu nedenle, bir projeye bir sınıf diyagramı ekleyebilirsiniz ancak **Sınıf Tasarımcısı** öğeleri burada görselleştirmek izin vermez `IsManaged` özelliği `true` (diğer bir deyişle, değer türleri ve başvuru türleri).

- Visual C++ projeleri için **Sınıf Tasarımcısı** türünün tanımını okur. Örneğin, bir üstbilgi (.h) dosyasına tanımlayan bir tür ve üyeleri tanımlayan bir uygulama (.cpp) dosyasında varsayalım. Uygulama (.cpp) dosyasında "sınıf diyagramını görüntüle" çağırma **Sınıf Tasarımcısı** hiçbir şey görüntülemez. Başka bir örnek olarak kullanan bir .cpp dosya çubuğunda "sınıf diyagramını görüntüle" çağırma bir `#include` deyimini diğer dahil etme dosyaları, ancak herhangi bir gerçek sınıf tanımı içermiyor **Sınıf Tasarımcısı** yeniden hiçbir şey görüntüler.

- C++ yerel koda derlenmiş sürece IDL (.idl) dosyaları, COM arabirimi tanımlayın ve tür kitaplığı, diyagramlarında görüntülemez.

- **Sınıf Tasarımcısı** genel işlevler ve değişkenler desteklemez.

- **Sınıf Tasarımcısı** birleşimler desteklemez. Ayrılan belleğin yalnızca tutarı Birliği'nin en büyük veri üyesi için gerekli olduğu sınıf özel bir tür budur.

- **Sınıf Tasarımcısı** temel veri türleri gibi görüntülemez `int` ve `char`.

- **Sınıf Tasarımcısı** proje doğru başvuru türlerine sahip değilse, geçerli projenin dışında tanımlanan türlerinden görüntülemez.

- **Sınıf Tasarımcısı** iç içe geçmiş türler ancak iç içe türü ve diğer türleri arasında ilişkileri görüntüleyebilir.

- **Sınıf Tasarımcısı** void olan veya void türünden türetilen türler görüntülenemiyor.

## <a name="see-also"></a>Ayrıca bkz.

- [Sınıfları ve Türleri Tasarlama ve Görüntüleme (Sınıf Tasarımcısı)](designing-and-viewing-classes-and-types.md)
- [Sınıf Tasarımcısı Hataları Hakkında Ek Bilgiler](additional-information-about-errors.md)
- [Sınıf Tasarımcısında Visual C++ Sınıfları](visual-cpp-classes.md)
- [Sınıf Tasarımcısında Visual C++ Yapılandırmaları](visual-cpp-structures.md)
- [Sınıf Tasarımcısında Visual C++ Numaralandırmaları](visual-cpp-enumerations.md)
- [Sınıf Tasarımcısında Visual C++ Typedefs](visual-cpp-typedefs.md)

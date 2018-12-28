---
title: Parametre bilgisi, listesi üyeleri ve hızlı bilgi
ms.date: 05/25/2018
ms.prod: visual-studio-dev15
ms.technology: vs-ide-general
ms.topic: conceptual
f1_keywords:
- vc.tools.intellisense
helpviewer_keywords:
- Quick info
- Parameter info
- Complete word
- List members
- IntelliSense [Visual Studio]
author: gewarren
ms.author: gewarren
manager: douge
ms.workload:
- multiple
ms.openlocfilehash: 7e28c3a09197fd3fe0b45d40a3402f484ab867d7
ms.sourcegitcommit: 935e341a02dba1c2aa3b6e89469388aa6e626f7f
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 12/20/2018
ms.locfileid: "53684908"
---
# <a name="intellisense-in-visual-studio"></a>Visual Studio IntelliSense

IntelliSense birçok özellik içeren bir kod tamamlama yardımcısıdır: Üyeleri listeleme, parametre bilgisi, hızlı bilgi ve tam sözcük. Bu özellikler, kullanmakta olduğunuz kod hakkında daha fazla bilgi edinmek için yazmakta olduğunuz ve özellikleri ve yöntemleri ile yalnızca birkaç tuş vuruşu çağrıları ekleyin parametreleri izlemenize yardımcı olur.

IntelliSense'in birçok yönü dile özgüdür. Farklı diller için IntelliSense hakkında daha fazla bilgi için bkz. altında listelenen konulara [Ayrıca bkz:](#see-also) bölümü.

## <a name="list-members"></a>Üyeleri Listeleme

Bir tetikleyici karakteri yazdıktan sonra bir tür (veya ad alanı) geçerli üyelerin listesi görüntülenir (örneğin, bir süre (`.`) yönetilen kodda veya `::` C++'ta). Karakterleri yazmaya devam ederseniz liste yalnızca bu karakterlerle başlayan üyeleri içerecek şekilde filtrelenir veya burada başlangıcını *herhangi* adı Word'de bu karakterleri ile başlar. Ortası büyük küçük harfleri her sözcüğün ilk harfini eşleşmeleri görmek için üye adı yalnızca girebilmeniz için IntelliSense "ortası büyük harf eşleştirme" de gerçekleştirir.

Bir öğeyi seçtikten sonra bunu kodunuza tuşlarına basarak ekleyebilirsiniz **sekmesini** veya bir boşluk girerek. Öğeyi seçip bir nokta yazarsanız, bu noktanın arkasında başka üye listesini getiren bir öğe görüntülenir. Bir öğe seçtiğinizde, öğeyi eklemeden önce öğeye ilişkin Hızlı Bilgi alırsınız.

Üye listesinde, soldaki simge ad alanı, sınıf, işlev veya değişken gibi bir üye türünü temsil eder. Simgelerin bir listesi için bkz. [sınıf görünümü ve Nesne Tarayıcısı simgeleri](../ide/class-view-and-object-browser-icons.md). Basabilirsiniz şekilde liste oldukça uzun olabilir **PgUp** ve **PgDn** yukarı veya aşağı hareket etmek.

![Visual Studio üye listesi](../ide/media/vs2015_intellisense.png)

Çağırabilirsiniz **üyeleri Listele** yazarak el ile özellik **Ctrl**+**J**seçip **Düzenle**  >  **IntelliSense** > **üyeleri Listele**, seçerek veya **üyeleri Listele** Düzenleyici araç çubuğunda düğme. Boş bir satırda veya tanınabilir bir kapsamın dışında çağrıldığında, bu liste genel ad alanında simgeleri görüntüler.

Üyeleri listeleme (BT'nin özellikle görünmemesi için) varsayılan olarak devre dışı bırakmak için Git **Araçları** > **seçenekleri** > **tüm diller**ve seçimini **otomatik üyeleri Listele**. Yalnızca belirli bir dil için liste üyelerini devre dışı bırakmak isterseniz, Git **genel** bu dil için ayarlar.

Sadece yazdığınız metnin kodun içine eklendiği öneri moduna da geçebilirsiniz. Örneğin, liste ve ENTER tuşuna değil bir tanımlayıcı girmeniz **sekmesini**, tamamlama modunda bu giriş yazılan tanımlayıcının yerini alır. Tamamlama modu ile öneri modu arasında geçiş yapmak için basın **Ctrl**+**Alt**+**alanı**, ya da seçin **Düzenle**  >  **IntelliSense** > **tamamlama modunu Değiştir**.

## <a name="parameter-info"></a>Parametre Bilgisi

Parametre Bilgisi; bir yöntem, öznitelik genel tür parametresi (C#) veya şablon (C++) tarafından istenen parametrelerin sayısı, adları ve türleri hakkında bilgi verir.

Kalın yazı tipli parametre, işlevi yazarken gerekli olan bir sonraki parametreyi gösterir. Aşırı yüklenmiş işlevler için kullanabileceğiniz **yukarı** ve **aşağı** işlev aşırı yüklemelerinin ilişkin alternatif parametre bilgilerini görüntülemek için ok tuşlarını.

![Parametre Bilgisi](../ide/media/vs2015_param_info.png)

XML Belgeleri yorumlarıyla işlevlere ve parametrelere ek açıklamalar koyduğunuzda, yorumlar Parametre Bilgisi olarak görüntülenir. Daha fazla bilgi için [tedarik XML kodu açıklamalarını](reference/generate-xml-documentation-comments.md).

Parametre bilgisi seçerek el ile çağırabilirsiniz **Düzenle** > **IntelliSense** > **parametre bilgisi**, tuşuna basarak **Ctrl**  + **Shift**+**alanı**, seçerek veya **parametre bilgisi** Düzenleyici araç çubuğunda düğme.

## <a name="quick-info"></a>Hızlı Bilgi

Hızlı bilgi kodunuzdaki herhangi bir tanımlayıcı için bütün bildirimi görüntüler.

![Visual Studio hızlı bilgi](../ide/media/vs2015_quick_info.png)

Bir üye seçtiğinizde **üyeleri Listele** kutusunda, hızlı bilgi de görünür.

![Parametre bilgisi bir c&#35; kod dosyası](../ide/media/vs2015_paraminfo.png)

Seçerek hızlı Bilgi'yi el ile çağırabilirsiniz **Düzenle** > **IntelliSense** > **hızlı bilgi**, tuşuna basarak **Ctrl** + **miyim**, seçerek veya **hızlı bilgi** Düzenleyici araç çubuğunda düğme.

Bir işlev aşırı yüklenmişse, IntelliSense, tüm aşırı yük biçimleri için bilgileri görüntülemeyebilir.

Hızlı bilgi C++ kodu için giderek kapatabilirsiniz **Araçları** > **seçenekleri** > **metin düzenleyici** > **C / C++** > **Gelişmiş**ve ayarı **otomatik hızlı bilgi** için `false`.

## <a name="complete-word"></a>Tam Sözcük

Tam sözcük, terim belirsizliğini ortadan kaldıracak yeterli sayıda karakter girdikten sonra değişken, komut veya işlev adının kalanını tamamlar. Tam sözcük seçerek çağırabilirsiniz **Düzenle** > **IntelliSense** > **tam sözcük**, tuşuna basarak **Ctrl** + **Alanı**, seçerek veya **tam sözcük** Düzenleyici araç çubuğunda düğme.

## <a name="intellisense-options"></a>IntelliSense seçenekleri

IntelliSense seçenekleri varsayılan olarak açıktır. Bunları devre dışı bırakmak için seçin **Araçları** > **seçenekleri** > **metin düzenleyici** ve seçimini **parametre bilgileri**veya **otomatik üyeleri Listele** üyeleri listeleme özelliğini istemiyorsanız.

## <a name="troubleshoot-intellisense"></a>IntelliSense sorunlarını giderme

IntelliSense seçenekleri, belirli durumlarda beklediğiniz gibi çalışmayabilir.

**İmleç, kod bir hatadır.** Eksik bir işlev varsa IntelliSense'i kullanmanız mümkün olmayabilir veya IntelliSense kod öğelerini ayrıştıramayabileceğinden olmayabileceğinden imleç üzerindeki kodda başka bir hata bulunmaktadır. Uygulanabilir kodu açıklama olarak ekleyerek bu sorunu çözebilirsiniz.

**İmleç bir kod yorum var.** İmleç, kaynak dosyanızdaki bir açıklamada ise IntelliSense kullanamazsınız.

**İmleç bir dize sabit değeri var.** İmleç aşağıdaki örnekte olduğu gibi bir dize etrafında tırnak işaretlerinin içinde ise IntelliSense kullanamazsınız:

```cpp
MessageBox( hWnd, "String literal|")
```

**Otomatik seçenekler kapalıdır.** Varsayılan olarak, IntelliSense otomatik çalışır, ancak bunu devre dışı bırakabilirsiniz. Otomatik deyim tamamlama devre dışı olsa bile, bir IntelliSense özelliğini çağırabilirsiniz.

## <a name="see-also"></a>Ayrıca bkz.

- [Visual Basic IntelliSense](../ide/visual-basic-specific-intellisense.md)
- [C# IntelliSense](../ide/visual-csharp-intellisense.md)
- [JavaScript IntelliSense](../ide/javascript-intellisense.md)
- [Yazma ve yeniden düzenleme kod (C++)](/cpp/ide/writing-and-refactoring-code-cpp)
- [XML kodu açıklamalarını sağlayın](reference/generate-xml-documentation-comments.md)
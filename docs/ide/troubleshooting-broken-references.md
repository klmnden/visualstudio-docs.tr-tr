---
title: Bozuk başvurularda sorun giderme
ms.date: 03/21/2017
ms.prod: visual-studio-dev15
ms.topic: troubleshooting
helpviewer_keywords:
- C# projects, references
- Visual Basic projects, references
- troubleshooting references
- referencing files from projects
- referencing components, troubleshooting
author: gewarren
ms.author: gewarren
manager: douge
ms.workload:
- multiple
ms.openlocfilehash: c4d45dc01201747240f2ebbc50854b77fd31ec0f
ms.sourcegitcommit: 37fb7075b0a65d2add3b137a5230767aa3266c74
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/02/2019
ms.locfileid: "53847132"
---
# <a name="troubleshoot-broken-references"></a>Bozuk başvurularda sorun giderme

Uygulamanızı kırık referans kullanmaya çalışırsa, bir özel durum hatası oluşturulur. Yükleyememesine başvurulan bileşen bulmak için hatanın birincil tetikleyici olmakla birlikte bozuk bir referans kabul edilebilir birkaç durum mevcuttur. Aşağıdaki listede bu örnekler gösterilmektedir:

- Proje başvuru yolu yanlış veya eksik.

- Başvurulan dosya silindi.

- Başvurulan dosya yeniden adlandırıldı.

- Ağ bağlantısı veya kimlik doğrulaması başarısız oldu.

- Bilgisayarda yüklü olmayan bir COM bileşenine başvuru yapılır.

Bu sorunları çözümler aşağıda verilmiştir.

> [!NOTE]
> Derlemelerde dosyaları, proje dosyasındaki mutlak yollar ile başvurulur. Bu nedenle, başvurulan bir derlemenin yerel ortamlarında eksik geliþtiricili ortamında çalışan kullanıcıların mümkündür. Bu hataları önlemek için projeden projeye başvurular eklemek için bu gibi durumlarda daha iyi olur. Daha fazla bilgi için [Derlemelerle programlama](/dotnet/framework/app-domains/programming-with-assemblies).

## <a name="reference-path-is-incorrect"></a>Başvuru yolu yanlış

Farklı bilgisayarlarda Paylaşılan projeleri, bir bileşen farklı bir dizinde her bilgisayarda bulunan, bazı başvuruları bulunmayabilir. Başvurular, Bileşen dosyası adı altında depolanır (örneğin, *MyComponent*). Bir projeye bir başvuru eklendiğinde, Bileşen dosyası klasör konumuna (örneğin, *C:\MyComponents*) eklenir **ReferencePath** proje özelliği.

Bir proje açıldığında, başvuru yolu dizinleri bakarak bu başvurulan bileşen dosyaları bulmayı dener. Proje bileşeni gibi farklı bir dizinde depolar bir bilgisayarda açıldığında *D:\MyComponents*başvurusu bulunamıyor ve bir hata görünür **görev listesi**.

Bu sorunu gidermek için kırık referans silebilir ve sonra onu kullanarak değiştirmek **Başvuru Ekle** iletişim kutusu. Başka bir çözüm **başvuru yolu** öğesini projenin özellik sayfaları'nda ve klasörler listesinde, doğru konuma işaret edecek şekilde değiştirin. **Başvuru yolu** özelliği, her bilgisayardaki her kullanıcı için kalıcıdır. Bu nedenle, Başvuru yolunuza değiştirme projenin diğer kullanıcıların etkilemez.

> [!TIP]
> Projeden projeye başvurular, bu sorun yoktur. Mümkünse, bu nedenle, bunları dosya başvuruları yerine kullanın.

### <a name="to-fix-a-broken-project-reference-by-correcting-the-reference-path"></a>Bozuk bir proje başvurusu, başvuru yolu düzelterek düzeltmek için

1. İçinde **Çözüm Gezgini**, proje düğümüne sağ tıklayın ve tıklayın **özellikleri**.

   **Proje Tasarımcısı** görünür.

1. Visual Basic kullanıyorsanız **başvuruları** sayfasında ve tıklayın **başvuru yolları** düğmesi. İçinde **başvuru yolları** iletişim içinde başvurmak istediğiniz öğeyi içeren klasörün yolunu yazın **klasör** alan ve ardından **klasörü Ekle** düğmesi.

    Kullanıyorsanız C#seçin **başvuru yolları** sayfası. İçinde **klasör** alan, başvuru ve ardından istediğiniz öğeyi içeren klasörün yolunu yazın **klasörü Ekle** düğmesi.

## <a name="referenced-file-has-been-deleted"></a>Başvurulan dosya silindi

Bu, başvurulan dosya silindi ve artık sürücüde mevcut mümkündür.

### <a name="to-fix-a-broken-project-reference-for-a-file-that-no-longer-exists-on-your-drive"></a>Artık bir dosya bozuk proje başvurusunu sürücünüzde düzeltmek için

- Başvuruyu silin.

- Başvuru bilgisayarınızda başka bir konum varsa, o konumdan okuyun.

## <a name="referenced-file-has-been-renamed"></a>Başvurulan dosya yeniden adlandırıldı

Bu, başvurulan dosya yeniden adlandırıldı mümkündür.

### <a name="to-fix-a-broken-reference-for-a-file-that-has-been-renamed"></a>Bozuk bir başvuruyu yeniden adlandırıldı bir dosya için düzeltme

- Başvuru silin ve ardından yeniden adlandırılan dosyaya bir başvuru ekleyin.

- Başvuru bilgisayarınızda başka bir konum varsa, onu o konumdan okumak zorundasınız.

## <a name="network-connection-or-authentication-has-failed"></a>Ağ bağlantısı veya kimlik doğrulaması başarısız oldu

Erişilemeyen dosyalar için birçok olası nedenleri şunlar olabilir: başarısız bir ağ bağlantısı veya örneğin başarısız bir kimlik doğrulama. Her bir nedenden kurtarma benzersiz bir çeşit olabilir; Örneğin, gerekli kaynaklara erişim için yerel yönetici başvurmanız gerekebilir. Ancak, başvuru silme ve onu kullanan kod çözme her zaman bir seçenektir.

## <a name="com-component-is-not-installed-on-computer"></a>COM bileşeni bilgisayarda yüklü değil

Bir kullanıcı bir COM bileşenine bir başvuru eklemiştir ve bu bileşeni yüklü olmayan bir bilgisayarda kodu çalıştırmak ikinci bir kullanıcı çalışırsa, ikinci kullanıcı başvuru bozuk olduğunu belirten bir hata alırsınız. Bileşeni, ikinci bilgisayara yükleniyor. hatayı düzeltin. COM bileşenleri başvurular projelerinizde kullanma hakkında daha fazla bilgi için bkz. [.NET Framework uygulamalarında COM birlikte çalışabilirliği](/dotnet/visual-basic/programming-guide/com-interop/com-interoperability-in-net-framework-applications).

## <a name="see-also"></a>Ayrıca bkz.

- [Başvurular Sayfası, Proje Tasarımcısı (Visual Basic)](../ide/reference/references-page-project-designer-visual-basic.md)
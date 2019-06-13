---
title: Mac için Visual Studio’yu Genişletme
description: Mac özellikleri ve işlevleri için Visual Studio uzantı paketleri adlı modülleriyle genişletilebilir. Bu kılavuzun ilk bölümü, bir basit bir belgeye tarih ve saat için Visual Studio'yu Mac uzantı paketi oluşturur. İkinci bölümü, bu kılavuzun uzantı paketi sistemi temelleri ve bazı çekirdek temelini Mac için Visual Studio'nun API'leri sunar.
author: conceptdev
ms.author: crdun
ms.date: 05/07/2019
ms.technology: vs-ide-sdk
ms.assetid: D5245AB0-8404-426B-B538-F49125E672B2
ms.openlocfilehash: 1753eef9987bc59be55298489e10c5698eb944cc
ms.sourcegitcommit: 91c7f1b525e0c22d938bc4080ba4ceac2483474f
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/12/2019
ms.locfileid: "67033128"
---
# <a name="extending-visual-studio-for-mac"></a>Mac için Visual Studio’yu Genişletme

Mac için Visual Studio modülleri adlı bir dizi oluşur *uzantı paketleri*. Uzantı paketleri gibi ek bir dil veya yeni bir proje şablonu için destek, Mac için Visual Studio için yeni işlevleri tanıtmak için kullanabilirsiniz.

Uzantı paketleri yapı gelen *uzantısı* diğer uzantı paketleri noktaları. Uzantı, bağlı bir menü veya IDE komutların listesini gibi Genişletilebilir alanlarını yer tutucular noktalarıdır. Uzantı paketi, bir düğüm olarak adlandırılan yeni bir menü öğesi ya da yeni bir komut gibi bir uzantı yapılandırılmış verilerin kaydederek bir uzantı noktası oluşturabilirsiniz. Her uzantı noktası uzantıları, belirli bir türdeki gibi kabul bir *komut*, *paneli*, veya *FileTemplate*. Uzantı noktaları içeren bir modül olarak adlandırılan bir *eklentisi konak*gibi diğer uzantı paketleri tarafından genişletilebilir.

Mac için Visual Studio özelleştirmek için yapıları bir uzantı paketi, Mac için Visual Studio'da önceden mevcut olan kitaplıkları içindeki eklenti ana bulunan uzantı noktaları tarafından Aşağıdaki diyagramda gösterildiği gibi oluşturabilirsiniz:

![Eklenti mimarisi](media/extending-visual-studio-mac-addin1.png)

Mac için Visual Studio'dan oluşturmak bir uzantı paketi için sırada Visual Studio'da genişletme noktaları Mac IDE için önceden varolan yapı uzantıları olması gerekir. Uzantı paketinin bir eklenti konak tanımlanmış bir uzantı noktası kullanır, olması bildirilir bir _bağımlılık_ üzerinde bu uzantı paketi.

Bu modüler bir tasarım avantajdır Mac için Visual Studio Genişletilebilir--bağlı özel uzantı paketleri ile oluşturulabilir birçok uzantı noktaları vardır. Geçerli uzantı paketleri örnekler için destek C# ve F#, hata ayıklayıcı, Araçlar ve proje şablonları.

> [!NOTE]
> Eklenti Oluşturucu önce 1.2 oluşturulmuş bir oluşturucu eklenti projesine sahip olmak, projenizi adımlarda belirtildiği gibi geçiş geçmeniz [burada](https://mhut.ch/addinmaker/1.2).

<!---The [Walkthrough](~/extending-visual-studio-mac-walkthrough.md) topic explains how to build an extension package that uses a *Command* to insert the date and time into an open text document.--->

Bu bölümde, eklenti Oluşturucu tarafından üretilen farklı dosyalar bakar ve komut uzantısı verileri gerektirir.

## <a name="attribute-files"></a>Öznitelik dosyaları

Uzantı paketleri C# özniteliklerinde kullanıcının adını, sürüm, bağımlılıklar ve diğer bilgileri hakkındaki meta verileri depolar. Eklenti Oluşturucu iki dosya oluşturur `AddinInfo.cs` ve `AssemblyInfo.cs` depolamak ve bu bilgileri düzenlemek için. Uzantı paketleri benzersiz bir kimliği olması gerekir ve içinde belirtilen namespace kendi  *`Addin` özniteliği*:

```csharp
[assembly:Addin (
   "DateInserter",
   Namespace = "DateInserter",
   Version = "1.0"
)]
```

Uzantı paketleri ayrıca derleme sırasında otomatik olarak başvurulur bunlar, Tak uzantı noktaları kendi uzantı paketleri bağımlılıklarını bildirmeniz gerekir.

Ayrıca, ek başvurular proje çözüm panelinde eklenti referans düğümün aracılığıyla tarafından aşağıdaki görüntüde gösterildiği şekilde eklenebilir:

![Tarih ekran görüntüsü Ekle](media/extending-visual-studio-mac-addin13.png)

Bunlara karşılık gelen aynı zamanda sahiptirler `assembly:AddinDependency` başında eklenen öznitelikleri derleme zamanı. Meta veriler ve bağımlılık bildirimlerini yerinde olduktan sonra uzantı paketinin temel yapı taşlarını üzerinde odaklanabilirsiniz.

## <a name="extensions-and-extension-points"></a>Uzantılar ve uzantı noktaları

(Bir tür), bir veri yapısını tanımlayan yer tutucu bir uzantı noktasıdır istediğiniz uzantıyı noktasınca belirtilen bir yapıya uyan veriler uzantı tanımlar. Ne tür uzantısı kendi bildiriminde kabul edebilir, uzantı noktaları belirtin. Uzantılar, tür adları veya uzantı yolları kullanarak bildirilir. Bkz: [uzantı noktası başvuru](https://github.com/mono/mono-addins/wiki/Extension-Points) ihtiyacınız uzantı noktası oluşturma hakkında daha ayrıntılı bir açıklama için.

Uzantı/uzantı noktası mimarisi, hızlı ve modüler bir Mac için Visual Studio geliştirme tutar.

<!--Since there are a large number of extension types, this article focuses on the ones used in the extension package that was built in the [Walkthrough](~/extending-visual-studio-mac-walkthrough.md).-->

### <a name="command-extensions"></a>Komut uzantıları

<!--[Walkthrough](~/extending-visual-studio-mac-walkthrough.md) uses a Command Extension - an extension that points to methods that are called every time it is executed. -->

Komut uzantıları her zaman yürütülür çağrılan yöntemlere işaret eden uzantılarıdır.

Komut uzantıları girdileri ekleme tarafından tanımlanan `/MonoDevelop/Ide/Commands` uzantı noktası. Bizim uzantısında tanımladığımız `Manifest.addin.xml` aşağıdaki kod ile:

 ```xml
<Extension path="/MonoDevelop/Ide/Commands/Edit">
  <command id="DateInserter.DateInserterCommands.InsertDate"
            _label="Insert Date"
            _description="Insert the current date"
            defaulthandler="DateInserter.InsertDateHandler" />
</Extension>
```

Uzantı düğüm, bu durumda takarak genişletme noktası belirtir bir path özniteliği içeren `/MonoDevelop/Ide/Commands/Edit`. Ayrıca, komutu bir üst düğüme görür. Komut düğümü aşağıdaki özniteliklere sahiptir:

* `id` -Bu komut için tanımlayıcısını belirtir. Komut tanımlayıcıları numaralandırma üyeleri bildirilmesi gerekir ve komutları için Commandıtems'lara bağlanmak için kullanılır.
* `_label` -Menülerde gösterilecek metin.
* `_description` -Araç çubuğu düğmeleri araç ipucu olarak gösterilecek metin.
* `defaultHandler` -Belirtir `CommandHandler` komutu güç katan sınıfı

<!--To invoke the command from the Edit Menu, the walkthrough creates a CommandItem extension that plugs into the `/MonoDevelop/Ide/MainMenu/Edit` extension point:-->

İçine takılan CommandItem uzantısı `/MonoDevelop/Ide/MainMenu/Edit` uzantı noktası, aşağıdaki kod parçacığında gösterilmiştir:

```xml
<Extension path="/MonoDevelop/Ide/MainMenu/Edit">
  <commanditem id="DateInserter.DateInserterCommands.InsertDate" />
</Extension>
```

Belirtilen bir komutu bir CommandItem yerleştirir, `id` menü içine özniteliği. Bu CommandItem genişletme `/MonoDevelop/Ide/MainMenu/Edit` komut etiket görünür kılan uzantı noktası **Düzen menüsünün**. Not kimliği CommandItem komut düğüm Kimliğine karşılık gelen `InsertDate`. CommandItem kaldırırsanız **tarih Ekle** seçeneği Düzenle Menüsü'nden kaybolması.

### <a name="command-handlers"></a>Komut işleyicileri

`InsertDateHandler` Uzantısıdır `CommandHandler` sınıfı. İki yöntem, onu geçersiz kılar `Update` ve `Run`. `Update` Yöntemi sorgulanan her bir komut bir menüde görüntülenen veya tuş bağlamaları yürütülür. Bilgisi nesnesi değiştirerek, komutunu devre dışı bırakmak veya görünmez yapma, dizi komutları ve daha fazlasını doldurun. Bu `Update` yöntemi devre dışı bırakır komut etkin bir bulamazsanız *belge* ile bir *TextEditor* metnine eklemek için:

```csharp
protected override void Update (CommandInfo info)
{
    info.Enabled = IdeApp.Workbench.ActiveDocument?.Editor != null;
}
```

Geçersiz kılmak yeterlidir `Update` etkinleştirme veya komut gizleme için özel bir mantık varsa yöntemi. `Run` Yöntemini yürütür her bir kullanıcı Düzenle Menüsü'nden bir kullanıcı komutu seçtiğinde oluşan bu durumda bir komutu yürütür. Bu yöntem, metin düzenleyici giriş işaretini tarihi ve saati ekler:

```csharp
protected override void Run ()
{
  var editor = IdeApp.Workbench.ActiveDocument.Editor;
  var date = DateTime.Now.ToString ();
  editor.InsertAtCaret (date);
}
```

Komut türü içinde bir sabit listesi üye olarak bildirmek `DateInserterCommands`:

```csharp
public enum DateInserterCommands
{
  InsertDate,
}
```

Komut ve CommandItem artık birlikte bağlıdır - CommandItem seçildiğinde CommandItem komutu çağıran **Düzen menüsünün**.

## <a name="ide-apis"></a>IDE API'leri

<!--The extension package detailed in the [Walkthrough](~/extending-visual-studio-mac-walkthrough.md) deals with the Text Editor in Visual Studio for Mac, but this is only one of many possible areas for customization. -->

Geliştirme için kullanılabilir alanları kapsamı hakkında daha fazla bilgi için bkz: [uzantı ağaç başvurusu](http://monodevelop.com/Developers/Articles/Extension_Tree_Reference) ve [API'sine genel bakış](http://monodevelop.com/Developers/Articles/API_Overview). Ayrıca başvurmak Gelişmiş uzantı paketleri oluştururken [Geliştirici makaleleri](http://monodevelop.com/Developers/Articles). Özelleştirme için alanları kısmi bir listesi aşağıdadır:

* Bölmeleri
* Tuş bağlama şemalarını
* İlkeler
* Kod biçimlendiricileri
* Proje dosya biçimleri
* Tercihler panelleri
* Seçenekleri panelleri
* Hata ayıklayıcı protokolleri
* Hata ayıklama görselleştiricileri
* Çalışma alanı düzeni
* Çözüm paneli ağaç düğümleri
* Kaynak Düzenleyicisi kenar boşlukları
* Birim test altyapıları
* Kod oluşturucuları
* Kod parçacıkları
* Hedef çerçeveler
* Hedef çalışma zamanı
* VC arka uçları
* Yeniden Düzenle
* Yürütme işleyicileri
* Söz dizimi vurgulama

## <a name="extending-the-new-editor"></a>Yeni bir düzenleyici genişletme

Mac için Visual Studio [yeni yerel Cocoa metin düzenleyici UI tanıtır](https://aka.ms/vs/mac/editor/learn-more) Windows üzerinde Visual Studio aynı Düzenleyicisi katmanları üzerinde oluşturulmuş.

Visual Studio Düzenleyicisi'ni hedefleyen kodlarda Mac için Visual Studio çalıştırmak uyarlanabilir Mac için Visual Studio ve Visual Studio arasında Düzenleyicisi paylaşımı birçok yararından biri olan

> [!NOTE]
> Yeni bir düzenleyici destekler yalnızca C# şu anda dosyaları. Diğer diller ve dosya biçimleri eski düzenleyicide açılır. Eski Düzenleyici ancak bazı Visual Studio Düzenleyicisi aşağıda açıklanan API'leri uygulayın.

### <a name="visual-studio-editor-overview"></a>Visual Studio Düzenleyicisi'ne genel bakış

![Visual Studio Düzenleyicisi mimarisi](media/vs-editor-architecture.png)

Mac için Visual Studio'ya özel uzantı ayrıntılarını önce dokunma, paylaşılan Düzenleyici daha iyi anlamanıza yardımcı olur. Aşağıda bu anlayış güçlendirmenizi bazı kaynaklar verilmiştir:

* [Yönetilen Genişletilebilirlik Çerçevesi](https://docs.microsoft.com/dotnet/framework/mef/index)
* [MEF Düzenleyicisi](https://docs.microsoft.com/visualstudio/extensibility/managed-extensibility-framework-in-the-editor)
* [Düzenleyicinin İçinde](https://docs.microsoft.com/visualstudio/extensibility/inside-the-editor)
* [Dil Hizmeti ve Düzenleyici Uzantı Noktaları](https://docs.microsoft.com/visualstudio/extensibility/language-service-and-editor-extension-points)
* [Bir video Giriş Düzenleyicisi mimarisi](https://www.youtube.com/watch?v=PkYVztKjO9A)

Elle bu kaynakları ile aşina olmanız gerekir birincil kavramlardır bir [ `ITextBuffer` ](https://docs.microsoft.com/dotnet/api/microsoft.visualstudio.text.itextbuffer) ve [ `ITextView` ](https://docs.microsoft.com/dotnet/api/microsoft.visualstudio.text.editor.itextview):

* Bir `ITextBuffer` zaman içinde değişebilir metni, bir bellek içi temsilidir. `CurrentSnapshot` Özelliği `ITextBuffer` döndürür bir *değişmez* arabellek örneği geçerli içeriğini gösterimini `ITextSnapshot`. Bir düzenleme arabelleği yapıldığında CurrentSnapshot özelliği en son sürümüne güncelleştirilir. Metin anlık görüntü herhangi bir iş parçacığı üzerinde Çözümleyicileri inceleyebilirsiniz ve içeriğinin asla değiştirmek için garantisi.

* Bir `ITextView` nasıl UI gösterimidir `ITextBuffer` Düzenleyicisi denetim ekranda işlenir. Kendi metin arabelleğini bir başvuru içeriyor olarak `Caret`, `Selection`ve diğer kullanıcı Arabirimi ile ilgili kavramları.

İçin bir verilen [ `MonoDevelop.Ide.Gui.Document` ](http://source.monodevelop.com/#MonoDevelop.Ide/MonoDevelop.Ide.Gui/Document.cs,4e960d4735f089b5), ilişkili temel alabilir `ITextBuffer` ve `ITextView` aracılığıyla `Document.GetContent<ITextBuffer>()` ve `Document.GetContent<ITextView>()` sırasıyla.

## <a name="additional-information"></a>Ek Bilgiler

> [!NOTE]
> Şu anda Mac için Visual Studio genişletilebilirlik senaryoları geliştirmeye çalışıyoruz Uzantıları oluşturma ve Ek Yardım veya bilgi gereksinim veya geri bildirim sağlamak isterseniz, lütfen doldurun [Mac uzantısı geliştirme için Visual Studio](https://aka.ms/vsmac-extensions-survey) formu.

## <a name="see-also"></a>Ayrıca bkz.

- [(Windows üzerinde) Visual Studio uzantıları geliştirme](/visualstudio/extensibility/starting-to-develop-visual-studio-extensions)
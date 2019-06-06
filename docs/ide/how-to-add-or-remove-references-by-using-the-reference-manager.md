---
title: Başvuru Yöneticisi'nde başvurular ekleme
ms.date: 04/11/2018
ms.topic: conceptual
f1_keywords:
- VS.ReferenceManager
helpviewer_keywords:
- C# projects, references
- references [Visual Studio], adding
- assemblies [Visual Studio], references
- Visual Basic projects, references
- project references, adding
- referencing components, adding references
- project references, removing
- referencing assemblies
- referencing components, removing references
- references [Visual Studio], removing
- referencing components, assemblies not listed
author: gewarren
ms.author: gewarren
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 885dee2ca04060042e804ff964636d16e6a725ee
ms.sourcegitcommit: 12f2851c8c9bd36a6ab00bf90a020c620b364076
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/06/2019
ms.locfileid: "66745811"
---
# <a name="how-to-add-or-remove-references-by-using-the-reference-manager"></a>Nasıl yapılır: Başvuru Yöneticisi’ni kullanarak başvuru ekleme veya kaldırma

Kullanabileceğiniz **başvuru Yöneticisi** veya başka bir şirketin geliştirdiği eklemek ve yönetmek için iletişim kutusu sizin Microsoft, bileşenine başvuruyor. Bir evrensel Windows uygulaması geliştiriyorsanız, projeniz otomatik olarak tüm doğru Windows SDK'sı DLL'lerin başvuruyor. Bir .NET uygulaması geliştiriyorsanız projeniz otomatik olarak başvuruda *mscorlib.dll*. Bazı .NET API'ları el ile eklemek zorunda bileşenlerde sunulur. COM bileşenleri veya özel bileşenler başvuruları el ile eklenmesi gerekir.

## <a name="reference-manager-dialog-box"></a>Başvuru Yöneticisi iletişim kutusu

**Başvuru Yöneticisi** iletişim kutusunda, sol taraftaki proje türüne bağlı olarak farklı kategorileri gösterilir:

- **Derlemeleri**, ile **Framework** ve **uzantıları** alt gruplar.

- **COM**, başvuru için kullanılabilen tüm COM bileşenlerini listeler.

- **Çözüm**, ile **projeleri** alt.

- **Windows**, ile **çekirdek** ve **uzantıları** alt gruplar. Windows SDK veya uzantı SDK'sındaki başvuruları kullanarak keşfedebilirsiniz **Nesne Tarayıcısı**.

- **Gözat**, ile **son** alt.

## <a name="add-a-reference"></a>Bir başvuru ekleyin

1. İçinde **Çözüm Gezgini**, sağ **başvuruları** veya **bağımlılıkları** düğüm ve **Başvuru Ekle**. Ayrıca proje düğümüne sağ tıklayın ve seçin **Ekle** > **başvuru**.

   **Başvuru Yöneticisi** açılır ve kullanılabilir başvuruları gruba göre listeler.

2. Başvuruları ekleyin ve ardından belirtin **Tamam**.

## <a name="assemblies-tab"></a>Derlemeler sekmesi

**Derlemeleri** sekmesi, başvuru için kullanılabilen tüm .NET derlemelerini listeler. **Derlemeleri** GAC içindeki derlemeler çalışma zamanı ortamının bir parçası olduğu için sekmesinde herhangi bir derleme genel derleme önbelleğinden (GAC) listelenmiyorsa. Dağıtmak veya GAC'ye kayıtlı bir derlemeye bir başvuru içeren bir uygulama kopyalarsanız, derleme olmaz dağıtılacağını veya bakılmaksızın uygulama ile birlikte kopyalanan **Yereli Kopyala** ayarı. Daha fazla bilgi için [bir projedeki başvuruları yönetme](../ide/managing-references-in-a-project.md).

Başvuru EnvDTE ad alanlarının herhangi birine el ile eklerseniz (<xref:EnvDTE>, <xref:EnvDTE80>, <xref:EnvDTE90>, <xref:EnvDTE90a>, veya <xref:EnvDTE100>) ayarlayın **birlikte çalışma türlerini katıştır** başvuruözelliği**False** içinde **özellikleri** penceresi. Bu özelliği ayarlamak **True** neden sorunları katıştırılamayan belirli EnvDTE özellikleri nedeniyle oluşturabilirsiniz.

Tüm masaüstü projeleri için örtük bir başvuru içeren **mscorlib**. Visual Basic projeleri için örtük bir başvuru içeren <xref:Microsoft.VisualBasic>. Tüm projeleri örtük bir başvuru içeren **System.Core**, başvurular listesinden kaldırılsa bile.

Bir proje türü Derlemeler'i desteklemiyorsa sekmesinde görünmez **başvuru Yöneticisi** iletişim kutusu.

**Derlemeleri** sekmesi iki alt sekmeden oluşur:

1. **Framework** hedef alınan çerçeveyi oluşturan tüm derlemeleri listeler.

   .NET Core veya evrensel Windows platformu hedefleyen olmayan projeler için **Framework** sekmesini hedeflenen çerçeveden derlemeleri numaralandırır. Kullanıcı uygulamanın gerek duyduğu başvuru eklemeniz gerekir.

   Evrensel Windows projeleri, varsayılan olarak hedeflenen çerçevenin içindeki derlemelerin tümüne başvurular içerir. Yönetilen projelerde altındaki bir salt okunur düğüm **başvuruları** klasöründe **Çözüm Gezgini** çerçeve'nin tümüne yönelik başvuruyu belirtir. Buna **Framework** sekmesi çerçeveden derlemelerin hiçbirini numaralandırma değildir ve bunun yerine şu iletiyi görüntüler: "Tüm Framework derlemelerine zaten başvurulmuş. Lütfen Nesne Tarayıcısı Framework'deki başvuruları araştırmak için kullanın".

2. **Uzantıları** bileşen ve denetim dış satıcılarının hedeflenen çerçeveyi genişletmek için geliştirilmiştir tüm derlemeleri listeler. Kullanıcı uygulamasının amacına bağlı olarak, bu derlemelere gerek duyulabilir.

   **Uzantıları** aşağıdaki konumlarda kayıtlı derlemeleri numaralandırmak suretiyle doldurulur:

   32-bit makinedeki:
   - `HKEY_CURRENT_USER\SOFTWARE\Microsoft\[Target Framework Identifier]\v[Target Framework Version]\AssemblyFoldersEx\[UserComponentName]\@default=[Disk location of assemblies]`
   - `HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\[Target Framework Identifier]\v[Target Framework Version]\AssemblyFoldersEx\[UserComponentName]\@default=[Disk location of assemblies]`

   64-bit makinedeki:
   - `HKEY_CURRENT_USER\SOFTWARE\Wow6432Node\Microsoft\[Target Framework Identifier]\v[Target Framework Version]\AssemblyFoldersEx\[UserComponentName]\@default=[Disk location of assemblies]`
   - `HKEY_LOCAL_MACHINE\SOFTWARE\Wow6432Node\Microsoft\[Target Framework Identifier]\v[Target Framework Version]\AssemblyFoldersEx\[UserComponentName]\@default=[Disk location of assemblies]`

   Ve önceki sürümleri [hedef çerçeve tanımlayıcısı]

   Örneğin, bir proje bir 32-bit makinede .NET Framework 4 hedefliyse **uzantıları** altında kayıtlı derlemeleri listeler *\Microsoft\.NETFramework\v4.0\AssemblyFoldersEx*, *\Microsoft\.NETFramework\v3.5\AssemblyFoldersEx*, *\Microsoft\.NETFramework\v3.0\AssemblyFoldersEx*, ve *\ Microsoft\.NETFramework\v2.0\AssemblyFoldersEx*.

Listedeki bazı bileşenler, projenizi framework sürümüne bağlı olarak gösterilmeyebilir. Bu, aşağıdaki koşullarda oluşabilir:

- Yeni bir framework sürümünü kullanan bileşen, daha önceki bir sürümünü hedefleyen bir proje ile uyumlu değil.

   Bir proje için hedef framework sürümünü değiştirme hakkında daha fazla bilgi için bkz: [nasıl yapılır: Hedef framework sürümü](../ide/how-to-target-a-version-of-the-dotnet-framework.md).

- .NET Framework 4 kullanan bileşen, .NET Framework 4.5 hedefleyen bir proje ile uyumlu değil.

Bunun yapılması, derleme hatalarına neden olabilir, başka bir projenin çıktılarına dosya başvuruları aynı çözümde eklemekten kaçının. Bunun yerine, **projeleri** sekmesinde **Başvuru Ekle** projeden projeye başvuru oluşturmak için iletişim kutusu. Bu takım geliştirme projelerinizde oluşturduğunuz sınıf kitaplıklarının daha iyi yönetimine etkinleştirerek kolaylaştırır. Daha fazla bilgi için [başvuruları bozuk sorun giderme](../ide/troubleshooting-broken-references.md).

> [!NOTE]
> Visual Studio 2015 veya sonraki sürümlerde, bir projenin hedef framework sürümü .NET Framework 4.5 veya sonrası ise ve diğer projenin hedef sürümü .NET Framework 2, 3, 3.5 veya 4.0 ise bir proje başvurusu yerine dosya başvurusu oluşturulur.

### <a name="to-display-an-assembly-in-the-add-reference-dialog-box"></a>Bir derlemeyi Başvuru Ekle iletişim kutusunda görüntülemek için

- Taşıma veya derlemeyi aşağıdaki konumlardan birine kopyalayın:

   - Geçerli proje dizini. (Kullanarak bu derlemeleri bulabilirsiniz **Gözat** sekmesini.)

   - Aynı çözüm içindeki diğer proje dizinleri. (Kullanarak bu derlemeleri bulabilirsiniz **projeleri** sekmesini.)

    \- veya -

- Görüntülenecek derlemelerin konumunu belirten bir kayıt defteri anahtarını ayarlayın:

   Bir 32-bit işletim sistemi için aşağıdaki kayıt defteri anahtarlarından birini ekleyin.

   - `[HKEY_CURRENT_USER\SOFTWARE\Microsoft\.NETFramework\<VersionMinimum>\AssemblyFoldersEx\MyAssemblies]@="<AssemblyLocation>"`

   - `[HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\.NETFramework\<VersionMinimum>\AssemblyFoldersEx\MyAssemblies]@="<AssemblyLocation>"`

   Bir 64-bit işletim sistemi için bir 32-bit kayıt defteri kovanında bulunan aşağıdaki kayıt defteri anahtarlarından birini ekleyin.

   - `[HKEY_CURRENT_USER\SOFTWARE\Wow6432Node\Microsoft\.NETFramework\<VersionMinimum>\AssemblyFoldersEx\MyAssemblies]@="<AssemblyLocation>"`

   - `[HKEY_LOCAL_MACHINE\SOFTWARE\Wow6432Node\Microsoft\.NETFramework\<VersionMinimum>\AssemblyFoldersEx\MyAssemblies]@="<AssemblyLocation>"`

   *\<VersionMinimum\>*  geçerli en düşük framework sürümüdür. Varsa *\<VersionMinimum\>* v3.0, belirtilen klasörleri olan *AssemblyFoldersEx* .NET Framework 3.0 ve üstünü hedefleyen projeler için geçerlidir.

   *\<AssemblyLocation\>*  görünmesini istediğiniz derlemelerin dizinidir **Başvuru Ekle** iletişim kutusu *C:\MyAssemblies*.

   Altında kayıt defteri anahtarı oluşturma `HKEY_LOCAL_MACHINE` düğümü, tüm kullanıcıların belirtilen konumda derlemelerde sağlar **Başvuru Ekle** iletişim kutusu. Altında kayıt defteri anahtarı oluşturma `HKEY_CURRENT_USER` düğümü yalnızca geçerli kullanıcı ayarını etkiler.

   Açık **Başvuru Ekle** iletişim kutusunu bir daha. Derlemeleri görünmelidir **.NET** sekmesi. Aksi takdirde, derlemelerin yer olduğundan emin olun belirtilen *AssemblyLocation* dizin, Visual Studio'yu yeniden başlatın ve yeniden deneyin.

## <a name="projects-tab"></a>Projeler sekmesi

**Projeleri** sekmesi içinde geçerli çözüm içindeki tüm uyumlu projeleri listeler **çözüm** alt sekmesi.

Bir proje, farklı framework sürümünü hedefleyen başka bir projeye başvuruda bulunabilir. Örneğin, .NET Framework 4 hedefleyen bir proje oluşturabilirsiniz ancak, .NET Framework 2 için oluşturulmuş bir derlemeye başvurur. Ancak, .NET Framework 2 projesi bir .NET Framework 4 projesi başvuramaz. Daha fazla bilgi için [genel bakışı hedefleyen Framework](../ide/visual-studio-multi-targeting-overview.md).

> [!NOTE]
> .NET Framework 4 hedefleyen bir proje .NET Framework 4 istemci Profili'ni hedefleyen bir proje ile uyumlu değil.

## <a name="universal-windows-tab"></a>Evrensel Windows sekmesi

**Evrensel Windows** sekmesi çalıştırma hangi Windows işletim sistemleri platformlara özgü tüm SDK'ları listeler.
Bu sekme, iki alt gruptan sahiptir: **Çekirdek** ve **uzantıları**.

### <a name="core-subgroup"></a>Çekirdek alt grubu

Evrensel Windows uygulaması projeleri, varsayılan olarak Evrensel Windows SDK'sına bir başvuru sahiptir. Buna **çekirdek** alt gruba **başvuru Yöneticisi** Evrensel Windows SDK'sı derlemelerin hiçbirini numaralandırma değildir.

### <a name="extensions-subgroup"></a>Uzantılar alt grubu

**Uzantıları** kullanıcı hedeflenen Windows platformunu genişleten bir SDK'ları listeler.

SDK, Visual Studio'nun tek bir bileşen olarak kabul ettiği dosyalar topluluğudur. İçinde **uzantıları** sekmesi, proje için geçerli bir SDK'ları **başvuru Yöneticisi** iletişim kutusunun çağrıldığı tek varlıklar halinde listelenir. Bir projeye eklendiğinde SDK içeriğinin tümü kullanılır Visual Studio tarafından kullanıcının IntelliSense, araç kutusu, tasarımcılar, içinde SDK içeriğinden yararlanmak için gereken diğer işlemleri olması gerekmez, nesne tarayıcısı, yapı, dağıtım, hata ayıklama ve paketleme.

SDK'nıza görüntüleme hakkında bilgi için **uzantıları** sekmesinde bkz [yazılım geliştirme seti oluşturma](../extensibility/creating-a-software-development-kit.md).

> [!NOTE]
> Bir proje, başka bir SDK'ya bağımlı bir SDK'ya başvuruda bulunursa, Visual Studio ikinci SDK'sına bir başvuru el ile eklemediğiniz sürece ikinci SDK'yı kullanmaz. Ne zaman bir kullanıcının seçtiği bir SDK'sı üzerinde **uzantıları** sekmesinde **başvuru Yöneticisi** iletişim kutusu, herhangi bir bağımlılığın Ayrıntılar bölmesinde listeleyerek SDK bağımlılıklarını belirlemenize yardımcı olur.

Bu sekme görünür olmayan bir proje türü uzantıları desteklemiyorsa, **başvuru Yöneticisi** iletişim kutusu.

## <a name="com-tab"></a>COM sekmesi

**COM** sekmesi, başvuru için kullanılabilen tüm COM bileşenlerini listeler. Dahili bildirim içeren kayıtlı bir COM DLL öğesine başvuru eklemek isterseniz, önce DLL kaydını silin. Aksi takdirde, Visual Studio, bir ActiveX denetimi yerel bir DLL olarak bütünleştirilmiş kod başvurusu ekler.

Bir proje türü COM'u desteklemiyorsa sekmesinde görünmez **başvuru Yöneticisi** iletişim kutusu.

## <a name="browse-button"></a>Gözat düğmesi

Kullanabileceğiniz **Gözat** düğmesini dosya sistemindeki bir bileşen için göz atın.

Bir proje, farklı framework sürümünü hedefleyen bir bileşene başvuruda bulunabilir. Örneğin, .NET Framework 4.7 hedefler, ancak .NET Framework 4 hedefleyen bir bileşene başvuruda bir uygulama oluşturabilirsiniz. Daha fazla bilgi için [genel bakışı hedefleyen Framework](../ide/visual-studio-multi-targeting-overview.md).

Aynı çözümdeki başka bir projenin çıktılarına dosya başvuruları ekleme kaçının, çünkü bu Taktik derleme hatalarına neden. Bunun yerine, **çözüm** sekmesinde **başvuru Yöneticisi** projeden projeye başvuru oluşturmak için iletişim kutusu. Bu takım geliştirme projelerinizde oluşturduğunuz sınıf kitaplıklarının daha iyi yönetimine etkinleştirerek kolaylaştırır. Daha fazla bilgi için [başvuruları bozuk sorun giderme](../ide/troubleshooting-broken-references.md).

Bir SDK'ye göz atamaz ve projenize ekleyin. Yalnızca bir dosyaya göz atabilirsiniz (örneğin, bir derleme veya *.winmd*) ve projenize ekleyin.

Bir Winmd'ye dosya başvurusu yaparken olan beklenen Düzen  *\<FileName > .winmd*,  *\<FileName > .dll*, ve  *\< Dosya adı > .pri* dosyaları tüm yanı sıra yerleştirilmesidir. Aşağıdaki senaryolarda bir WinMD'ye başvuruda bulunursanız, proje çıkış dizinine eksik bir dosya kümesi kopyalanır ve sonuç olarak, derleme ve çalışma zamanı hataları meydana gelir.

- **Yerel bileşen**: yerel bir proje her kopuk ad alanları kümesi için tek bir WinMD ve uygulamayı içeren bir DLL oluşturur. WinMD'ler ayrı adlara sahip olur. Bu yerel bileşen dosyasına başvururken, benzemeyecek şekilde adlandırılmış Winmd'lerin tek bileşen olun MSBuild tanımaz. Sonuç olarak, yalnızca aynı adlı  *\<FileName > .dll* ve  *\<FileName > .winmd* kopyalanır, ve çalışma zamanı hataları oluşur. Bu sorunu geçici olarak çözmek için uzantı SDK oluşturun. Daha fazla bilgi için [Create a Software Development Kit](../extensibility/creating-a-software-development-kit.md).

- **Denetimleri kullanma**: en az bir XAML denetimi oluşan bir  *\<FileName > .winmd*,  *\<FileName > .dll*,  *\<FileName > .pri*,  *\<XamlName > .xaml*ve bir  *\<IMAGENAME > .jpg*. Proje oluşturulduğunda, dosya başvurusu ile ilişkili kaynak dosyalar projenin çıkış dizinine kopyalanmaz ve yalnızca vermeyeceğiz  *\<FileName > .winmd*,  *\<dosya adı > .dll* ve  *\<FileName > .pri* kopyalanır. Bir yapı hatası kullanıcıya bildirmek için oturum açmış olan kaynakları  *\<XamlName > .xaml* ve  *\<IMAGENAME > .jpg* eksik. Başarılı olması için, kullanıcının bu kaynak dosyaları oluşturma ve hata ayıklama/çalışma zamanı için proje çıkış dizinine el ile kopyalaması gerekir. Bu sorunu geçici olarak çözmek için ya da bir uzantı SDK'sı adımları izleyerek oluşturun, [Create a Software Development Kit](../extensibility/creating-a-software-development-kit.md) veya aşağıdaki özellik eklemek için proje dosyasını düzenleyin:

    ```xml
    <PropertyGroup>
       <GenerateLibraryOutput>True</GenerateLibraryOutput>
    </PropertyGroup>
    ```

    > [!NOTE]
    > Özelliği eklerseniz, yapı daha yavaş çalışabilir.

## <a name="recent"></a>En Son

**Derlemeleri**, **COM**, **Windows**, ve **Gözat** her destek bir **son** listesini numaralandırır sekmesinde projelere yakın zamanda eklenmiş bileşenlerin.

## <a name="search"></a>Ara

Arama çubuğuna **başvuru Yöneticisi** iletişim kutusu'nın, odakta olan sekme üzerinde çalışır. Örneğin, bir kullanıcı sırasında arama çubuğuna "Sistem" yazarsa **çözüm** sekme odağı, arama Çözüm "Sistem" içeren bir proje adından oluşmadığı sürece herhangi bir sonuç döndürmek olmaz.

## <a name="see-also"></a>Ayrıca bkz.

- [Bir projedeki başvuruları yönetme](../ide/managing-references-in-a-project.md)
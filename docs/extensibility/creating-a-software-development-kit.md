---
title: Yazılım geliştirme kiti oluşturma | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
ms.assetid: 8496afb4-1573-4585-ac67-c3d58b568a12
author: madskristensen
ms.author: madsk
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: 042002b6fddb674c0f1c156be2d992cc96cb9f81
ms.sourcegitcommit: a124076dfd6b4e5aecda4d01984fee7b0c034745
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/05/2019
ms.locfileid: "68787665"
---
# <a name="create-a-software-development-kit"></a>Yazılım geliştirme seti oluşturma

Yazılım Geliştirme Seti (SDK), Visual Studio 'da tek bir öğe olarak başvurkabilmeniz için bir API koleksiyonudur. **Başvuru Yöneticisi** iletişim kutusu, projeyle ilgili olan tüm SDK 'ları listeler. Bir projeye SDK eklediğinizde, API 'Ler Visual Studio 'da kullanılabilir.

İki tür SDK vardır:

- Platform SDK 'Ları, bir platform için uygulama geliştirmeye yönelik zorunlu bileşenlerdir. Örneğin, [!INCLUDE[win81](../debugger/includes/win81_md.md)] uygulama geliştirmek [!INCLUDE[win8_appname_long](../debugger/includes/win8_appname_long_md.md)] için SDK gereklidir.

- Uzantı SDK 'Ları, platformu genişleten ancak bu platform için uygulama geliştirmeye yönelik zorunlu olmayan isteğe bağlı bileşenlerdir.

Aşağıdaki bölümlerde SDK 'ların genel altyapısı ve bir platform SDK 'sı ile Uzantı SDK 'Sı oluşturma açıklanır.

## <a name="platform-sdks"></a>Platform SDK 'Ları

Platform SDK 'Ları bir platforma yönelik uygulamalar geliştirmek için gereklidir. Örneğin, [!INCLUDE[win81](../debugger/includes/win81_md.md)] için [!INCLUDE[win81](../debugger/includes/win81_md.md)]uygulama geliştirmek için SDK gerekir.

### <a name="installation"></a>Yükleme

Tüm Platform SDK 'ları, *HKLM\Software\Microsoft\Microsoft\\SDK 'ları [TPI] \v [TPV]\\ @InstallationFolder = [SDK root]* konumunda yüklenecektir. Buna uygun olarak [!INCLUDE[win81](../debugger/includes/win81_md.md)] SDK, *HKLM\Software\Microsoft\Microsoft SDKs\Windows\v8.1*' e yüklenir.

### <a name="layout"></a>Düzen

Platform SDK 'Ları aşağıdaki düzene sahiptir:

```
\[InstallationFolder root]
            SDKManifest.xml
            \References
                  \[config]
                        \[arch]
            \DesignTime
                  \[config]
                        \[arch]
```

| Düğüm | Açıklama |
|------------------------| - |
| *Başvurular* klasörü | İle kodlanması yapabilen API 'Leri içeren ikili dosyaları içerir. Bunlar Windows meta verileri (WinMD) dosyalarını veya derlemelerini içerebilir. |
| *Tasarım zamanı* klasörü | Yalnızca çalıştırma öncesi/hata ayıklama zamanında gereken dosyaları içerir. Bunlar XML docs, kitaplıklar, üst bilgiler, araç kutusu tasarım zamanı ikilileri, MSBuild yapıtları, vb. içerebilir.<br /><br /> XML belgeleri, ideal olarak *\Designtime* klasörüne yerleştirilecektir, ancak başvurular için XML docs, Visual Studio 'daki başvuru dosyası ile birlikte yerleştirilmeye devam edecektir. Örneğin, bir başvurunun XML belgesi<em>\ başvurular\\\\[config] [Arch] \sample.dll</em> *\references\\[config]\\[Arch] \sample.xml*ve bu belge için yerelleştirilmiş sürümü olacaktır *\References\\[config]\\[Arch]\\[locale] \sample.xml*. |
| *Yapılandırma* klasörü | Yalnızca üç klasör olabilir: *Hata ayıklama*, *Perakende* ve *CommonConfiguration*. SDK yazarları, SDK tüketicisinin hedefleyecek yapılandırmadan bağımsız olarak, aynı SDK dosyaları kümesi tüketilmesi gerekiyorsa, dosyalarını *CommonConfiguration* altına yerleştirebilir. |
| *Mimari* klasörü | Desteklenen herhangi bir *mimari* klasörü bulunabilir. Visual Studio şu mimarileri destekler: x86, x64, ARM ve neutral. Not: Win32, x86 ile eşlenir ve eşlemeleri bağımsız olarak eşler.<br /><br /> MSBuild yalnızca Platform SDK 'Ları için *\CommonConfiguration\neutral* ' ın altında görünür. |
| *SDKManifest. xml* | Bu dosya, Visual Studio 'Nun SDK 'Yı nasıl tüketmesi gerektiğini açıklar. İçin [!INCLUDE[win81](../debugger/includes/win81_md.md)]SDK bildirimine bakın:<br /><br /> `<FileList             DisplayName = "Windows"             PlatformIdentity = "Windows, version=8.1"             TargetFramework = ".NET for Windows Store apps, version=v4.5.1; .NET Framework, version=v4.5.1"             MinVSVersion = "14.0">              <File Reference = "Windows.winmd">                <ToolboxItems VSCategory = "Toolbox.Default" />             </File> </FileList>`<br /><br /> **DisplayName** Nesne Tarayıcısı, gezinme listesinde görüntülenen değer.<br /><br /> **Platformıdentity:** Bu özniteliğin varlığı, Visual Studio 'ya ve MSBuild 'in bir platform SDK olduğunu ve bundan eklenen başvuruların yerel olarak kopyalanmayacağını söyler.<br /><br /> **TargetFramework** Bu öznitelik, Visual Studio tarafından yalnızca bu özniteliğin değerinde belirtilen çerçeveleri hedefleyen projelerin SDK 'Yı tükettiği için kullanılır.<br /><br /> **MinVSVersion** Bu öznitelik, Visual Studio tarafından yalnızca buna uygulanan SDK 'Ları kullanmak için kullanılır.<br /><br /> **Başvurunun** Bu özniteliğin yalnızca denetimleri içeren başvurular için belirtilmesi gerekir. Bir başvurunun denetimler içerip içermediğini belirtme hakkında bilgi için aşağıya bakın. |

## <a name="extension-sdks"></a>Uzantı SDK 'Ları

Aşağıdaki bölümlerde Uzantı SDK 'Sı dağıtmak için yapmanız gerekenler açıklanır.

### <a name="installation"></a>Yükleme

Uzantı SDK 'Ları, belirli bir kullanıcı veya bir kayıt defteri anahtarı belirtmeden tüm kullanıcılar için yüklenebilir. Tüm kullanıcılar için bir SDK yüklemek için aşağıdaki yolu kullanın:

*% Program Files%\Microsoft SDK\<'ları hedef\>platform \v < Platform sürüm\>numarası \ extensionsdk 'ları*

Kullanıcıya özgü yükleme için aşağıdaki yolu kullanın:

*%Userprofile%\appdata\local\microsoft SDK\<'ları hedef\>platform \v < Platform sürüm\>numarası \ extensionsdk 'ları*

Farklı bir konum kullanmak istiyorsanız, iki işlemlerden birini yapmanız gerekir:

1. Bunu bir kayıt defteri anahtarında belirtin:

     **HKLM\Software\Microsoft\Microsoft SDK\<'ları hedef platformu > \v < Platform sürüm\>numarası \ extensionsdk\<SDK adı\<> sdkversion >** \

     ve değerine `<path to SDK><SDKName><SDKVersion>`sahip olan bir (default) alt anahtarı ekleyin.

2. MSBuild özelliğini `SDKReferenceDirectoryRoot` proje dosyanıza ekleyin. Bu özelliğin değeri, başvurmak istediğiniz uzantı SDK 'larının bulunduğu, noktalı virgülle ayrılmış dizinlerin bir listesidir.

### <a name="installation-layout"></a>Yükleme düzeni

Uzantı SDK 'Ları aşağıdaki yükleme düzenine sahiptir:

```
\<ExtensionSDKs root>
           \<SDKName>
                 \<SDKVersion>
                        SDKManifest.xml
                        \References
                              \<config>
                                    \<arch>
                        \Redist
                              \<config>
                                    \<arch>
                        \DesignTime
                               \<config>
                                     \<arch>

```

1. \\< SDKName\>\\< sdkversion\>: Uzantı SDK 'sının adı ve sürümü, SDK kökünün yolundaki karşılık gelen klasör adlarından türetilir. MSBuild diskte SDK 'Yı bulmak için bu kimliği kullanır ve Visual Studio bu kimliği **Özellikler** penceresi ve **başvuru Yöneticisi** iletişim kutusunda görüntüler.

2. *Başvurular* klasörü: API 'leri içeren ikili dosyalar. Bunlar Windows meta verileri (WinMD) dosyaları veya derlemeleri olabilir.

3. *Redist* klasörü: çalışma zamanı/hata ayıklama için gereken dosyalar ve kullanıcının uygulamasının bir parçası olarak paketlenmesi gerekir. Tüm ikili dosyalar *\redist\\< config\>\\\>< Arch*altına yerleştirilmelidir ve ikili adların benzersizlik: *]* \<şirket için aşağıdaki biçimde olması gerekir >. \<ürün >. \<amaç >. \<uzantı ><em>. Örneğin, * Microsoft. cpp. Build. dll</em>. Diğer SDK 'lardan dosya adlarıyla çakışelebilecek adlara sahip tüm dosyalar (örneğin, JavaScript, CSS, PRI, XAML, PNG ve jpg dosyaları) \redist <em>\\< config\>\\< Arch\>altınayerleştirilmelidirxaml denetimleriyle ilişkili\> dosyalar hariç, SDKName\* <. \\ Bu dosyalar * \redist\\< config\>\\\\<Arch\\< ComponentName\>altınayerleştirilmelidir</em>.\>

4. *Tasarım zamanı* klasörü: yalnızca ön çalıştırma/hata ayıklama sırasında gerekli olan ve kullanıcının uygulamasının bir parçası olarak paketlenmemelidir. Bunlar XML belgeleri, kitaplıklar, üst bilgiler, araç kutusu tasarım zamanı ikilileri, MSBuild yapıtları vb. olabilir. Yerel bir proje tarafından tüketimine yönelik herhangi bir SDK 'nın bir *SDKName. props* dosyası olması gerekir. Aşağıda bu dosya türünün bir örneği gösterilmektedir.

   ```xml
   <?xml version="1.0" encoding="utf-8"?>
   <Project xmlns="http://schemas.microsoft.com/developer/msbuild/2003">
     <PropertyGroup>
       <ExecutablePath>C:\Temp\ExecutablePath;$(ExecutablePath)</ExecutablePath>
       <IncludePath>$(FrameworkSDKRoot)\..\v8.1\ExtensionSDKs\cppimagingsdk\1.0\DesignTime\CommonConfiguration\Neutral\include;$(IncludePath)</IncludePath>
       <AssemblyReferencePath>C:\Temp\AssemblyReferencePath;(AssemblyReferencePath)</AssemblyReferencePath>
       <LibraryPath>$(FrameworkSDKRoot)\..\v8.1\ExtensionSDKs\cppimagingsdk\1.0\DesignTime\Debug\ARM;$(LibraryPath)</LibraryPath>
       <SourcePath>C:\Temp\SourcePath\X64;$(SourcePath)</SourcePath>
       <ExcludePath>C:\Temp\ExcludePath\X64;$(ExcludePath)</ExcludePath>
       <_PropertySheetDisplayName>DevILSDK, 1.0</_PropertySheetDisplayName>
     </PropertyGroup>
   </Project>

   ```

    XML başvuru belgeleri, başvuru dosyasının yanına yerleştirilir. Örneğin, *\\\references <\>config\\< Arch\>\sample.dll* derlemesi için XML başvuru belgesi *\references\\< config şeklindedir\> \\<\Sample.xmlvebubelgeyeaityerelleştirilmişsürüm,\references<config<mimari<locale\>* *\\\>\\\>\\\>\ Sample.xml*.

5. *Yapılandırma* klasörü: üç alt klasör: *Hata ayıklama*, *Perakende*ve *CommonConfiguration*. SDK yazarları, SDK tüketicisinin hedeflediği yapılandırmadan bağımsız olarak aynı SDK dosyaları kümesi tüketilmesi gerektiğinde dosyalarını *CommonConfiguration* altına yerleştirebilir.

6. *Mimari* klasörü: Şu mimariler desteklenir: x86, x64, ARM, nötr. Win32, x86 ile eşlenir ve eşlemeleri bağımsız olarak eşler.

### <a name="sdkmanifestxml"></a>SDKManifest. xml

*SDKManifest. xml* dosyası, Visual Studio 'nun SDK 'yı nasıl tüketmesi gerektiğini açıklar. Aşağıda bir örnek verilmiştir:

```
<FileList>
DisplayName = "My SDK"
ProductFamilyName = "My SDKs"
TargetFramework = ".NETCore, version=v4.5.1; .NETFramework, version=v4.5.1"
MinVSVersion = "14.0"
MaxPlatformVersion = "8.1"
AppliesTo = "WindowsAppContainer + WindowsXAML"
SupportPrefer32Bit = "True"
SupportedArchitectures = "x86;x64;ARM"
SupportsMultipleVersions = "Error"
CopyRedistToSubDirectory = "."
DependsOn = "SDKB, version=2.0"
MoreInfo = "https://msdn.microsoft.com/MySDK">
<File Reference = "MySDK.Sprint.winmd" Implementation = "XNASprintImpl.dll">
<Registration Type = "Flipper" Implementation = "XNASprintFlipperImpl.dll" />
<Registration Type = "Flexer" Implementation = "XNASprintFlexerImpl.dll" />
<ToolboxItems VSCategory = "Toolbox.Default" />
</File>
</FileList>
```

Aşağıdaki liste, dosyanın öğelerini verir:

1. DisplayName: başvuru Yöneticisi, Çözüm Gezgini, Nesne Tarayıcısı ve Visual Studio için Kullanıcı arabirimindeki diğer konumlarda görünen değer.

2. ProductFamilyName: Genel SDK ürün adı. Örneğin, [!INCLUDE[winjs_long](../debugger/includes/winjs_long_md.md)] SDK "Microsoft. WinJS. 1.0" ve "Microsoft. WinJS. 2.0" olarak adlandırılmıştır. Bu, "Microsoft. WinJS" adlı SDK ürünleri ailesine ait. Bu öznitelik, bu bağlantıyı kurmak için Visual Studio ve MSBuild 'e izin verir. Bu öznitelik yoksa, SDK adı ürün ailesi adı olarak kullanılır.

3. FrameworkIdentity Bir veya daha fazla Windows Bileşen kitaplığı üzerinde bir bağımlılık belirtir. Bu özniteliğin değeri, tüketen uygulamanın bildirimine konur. Bu öznitelik yalnızca Windows bileşen kitaplıkları için geçerlidir.

4. TargetFramework Başvuru Yöneticisi ve araç kutusu 'nda bulunan SDK 'Ları belirtir. Bu, hedef çerçeve adları 'nın noktalı virgülle ayrılmış listesidir, örneğin ".NET Framework, sürüm = v 2.0; .NET Framework, sürüm = v 4.5.1". Aynı hedef Framework 'ün birkaç sürümü belirtilmişse, başvuru Yöneticisi filtreleme amacıyla belirtilen en düşük sürümü kullanır. Örneğin, ".NET Framework, Version = v 2.0; .NET Framework, Version = v 4.5.1" belirtilmişse, başvuru Yöneticisi ".NET Framework, sürüm = v 2.0" öğesini kullanacaktır. Belirli bir hedef çerçeve profili belirtilmişse, yalnızca bu profil başvuru Yöneticisi tarafından filtreleme amacıyla kullanılacaktır. Örneğin, "Silverlight, Version = v 4.0, profile = WindowsPhone" belirtildiğinde, başvuru Yöneticisi yalnızca Windows Phone profilinde filtreler; tam Silverlight 4,0 Framework 'Ü hedefleyen bir proje, başvuru yöneticisinde SDK 'Yı görmez.

5. MinVSVersion En düşük Visual Studio sürümü.

6. MaxPlatformVerson: Uzantı SDK 'sının çalışmayacak platform sürümlerini belirtmek için en fazla hedef platform sürümü kullanılmalıdır. Örneğin, Microsoft Visual C++ Runtime Package v 11.0 'A yalnızca Windows 8 projeleri tarafından başvurulmalıdır. Bu nedenle, Windows 8 projesinin MaxPlatformVersion değeri 8,0 ' dir. Bu, başvuru Yöneticisi bir Windows 8.1 projesi için Microsoft Visual C++ Runtime paketini filtreleyip bir [!INCLUDE[win81](../debugger/includes/win81_md.md)] proje buna başvurduğunda MSBuild bir hata oluşturur. Note: Bu öğe, tarihinde başlayarak [!INCLUDE[vs_dev12](../extensibility/includes/vs_dev12_md.md)]desteklenir.

7. AppliesTo Geçerli Visual Studio proje türlerini belirterek başvuru yöneticisinde bulunan SDK 'Ları belirtir. Dokuz değer tanınır: WindowsAppContainer, VisualC, VB, CSharp, WindowsXAML, JavaScript, Managed ve Native. SDK yazarı ve ("+") veya ("&#124;"), değil ("!") kullanabilir yalnızca SDK için uygulanan proje türlerinin kapsamını belirtmek için işleçler.

    WindowsAppContainer, uygulamalar için [!INCLUDE[win8_appname_long](../debugger/includes/win8_appname_long_md.md)] projeleri tanımlar.

8. SupportPrefer32Bit: Desteklenen değerler "true" ve "false" şeklindedir. Varsayılan değer "true" dır. Değer "false" olarak ayarlanırsa, SDK 'ya başvuruda bulunan projenin Prefer32Bit etkin olması [!INCLUDE[win8_appname_long](../debugger/includes/win8_appname_long_md.md)] halinde MSBuild, projeler (veya masaüstü projeleri için bir uyarı) için bir hata döndürür. Prefer32Bit hakkında daha fazla bilgi için bkz. [derleme sayfası, proje TasarımcısıC#()](../ide/reference/build-page-project-designer-csharp.md) veya [derleme sayfası, proje Tasarımcısı (Visual Basic)](../ide/reference/compile-page-project-designer-visual-basic.md).

9. Supportedmimariler: SDK 'nın desteklediği mimarilerin, noktalı virgülle ayrılmış bir listesi. Tüketim projesindeki hedeflenen SDK mimarisi desteklenmiyorsa MSBuild bir uyarı görüntüler. Bu öznitelik belirtilmemişse, MSBuild hiçbir şekilde bu uyarı türünü görüntülemez.

10. SupportsMultipleVersions: Bu öznitelik **hata** veya **Uyarı**olarak ayarlandıysa, MSBUILD aynı projenin aynı SDK ailesinin birden çok sürümüne başvuramayacağını gösterir. Bu öznitelik yoksa veya **Izin ver**olarak ayarlanırsa, MSBuild bu hata veya uyarı türünü görüntülemez.

11. AppX Diskteki Windows Bileşen kitaplığı için uygulama paketlerinin yolunu belirtir. Bu değer, yerel hata ayıklama sırasında Windows Bileşen kitaplığı 'nın kayıt bileşenine geçirilir. Dosya adı  *\<için adlandırma kuralı Şirket >.\< Ürün >. \<Mimari >. \<Yapılandırma >. Sürüm\<>. appx*. Yapılandırma ve mimari, Windows Bileşen kitaplığı için uygulanamazlar öznitelik adı ve öznitelik değeri için isteğe bağlıdır. Bu değer yalnızca Windows bileşen kitaplıkları için geçerlidir.

12. Copyredisttoaltdizini: *\Redist* klasörü altındaki dosyaların, uygulama paketi köküne (yani, **uygulama paketi oluşturma** Sihirbazı 'nda seçilen **paket konumu** ) ve çalışma zamanı düzen köküne göre kopyalanması gerektiğini belirtir. Varsayılan konum, uygulama paketinin ve **F5** düzeninin köküdür.

13. DependsOn Bu SDK 'nın bağımlı olduğu SDK kimliklerini tanımlayan SDK kimliklerinin bir listesi. Bu öznitelik, başvuru Yöneticisi 'nin Ayrıntılar bölmesinde görünür.

14. Daha fazla bilgi: Yardım ve daha fazla bilgi sağlayan Web sayfasının URL 'SI. Bu değer, başvuru Yöneticisi 'nin sağ bölmesindeki daha fazla bilgi bağlantısında kullanılır.

15. Kayıt türü: Uygulama bildiriminde WinMD kaydını belirtir ve buna karşılık gelen bir uygulama DLL 'SI olan yerel WinMD için gereklidir.

16. Dosya başvurusu: Yalnızca denetimleri içeren veya yerel Wınmds olan başvurular için belirtilir. Bir başvurunun denetimler içerip içermediğini belirtme hakkında bilgi için bkz. aşağıdaki [araç kutusu öğelerinin konumunu belirtme](#ToolboxItems) .

## <a name="ToolboxItems"></a>Araç kutusu öğelerinin konumunu belirtin

*SDKManifest. xml* şemasının **ToolBoxItems** öğesi hem platform hem de Uzantı SDK 'larında araç kutusu öğelerinin kategori ve konumunu belirtir. Aşağıdaki örneklerde farklı konumların nasıl belirtilmesi gösterilmektedir. Bu, WinMD veya DLL başvuruları için geçerlidir.

1. Araç kutusu varsayılan kategorisindeki denetimleri yerleştirin.

    ```xml
    <File Reference = "sample.winmd">
        <ToolboxItems VSCategory = "Toolbox.Default"/>
    </File>
    ```

2. Denetimleri belirli bir kategori adı altına yerleştirin.

    ```xml
    <File Reference = "sample.winmd">
        <ToolboxItems VSCategory= "MyCategoryName"/>
    </File>
    ```

3. Denetimleri belirli kategori adları altına yerleştirin.

    ```xml
    <File Reference = "sample.winmd">
        <ToolboxItems VSCategory = "Graph">
        <ToolboxItems/>
        <ToolboxItems VSCategory = "Data">
        <ToolboxItems />
    </File>
    ```

4. Blend ve Visual Studio 'da farklı kategori adları altına denetimler yerleştirin.

    ```xml
    // Blend accepts a slightly different structure for the category name because it allows a path rather than a single category.
    <File Reference = "sample.winmd">
        <ToolboxItems VSCategory = "Graph" BlendCategory = "Controls/sample/Graph">
        <ToolboxItems />
    </File>
    ```

5. Blend ve Visual Studio 'da belirli denetimleri farklı şekilde numaralandırın.

    ```xml
    <File Reference = "sample.winmd">
        <ToolboxItems VSCategory = "Graph">
        <ToolboxItems/>
        <ToolboxItems BlendCategory = "Controls/sample/Graph">
        <ToolboxItems/>
    </File>
    ```

6. Belirli denetimleri numaralandırın ve Visual Studio ortak yolunun altına veya yalnızca tüm denetimler grubuna yerleştirin.

    ```xml
    <File Reference = "sample.winmd">
        <ToolboxItems VSCategory = "Toolbox.Common">
        <ToolboxItems />
        <ToolboxItems VSCategory = "Toolbox.All">
        <ToolboxItems />
    </File>
    ```

7. Belirli denetimleri numaralandırın ve araç kutusunda olmayan ChooseItems içinde yalnızca belirli bir kümeyi gösterin.

    ```xml
    <File Reference = "sample.winmd">
        <ToolboxItems VSCategory = "Toolbox.ChooseItemsOnly">
        <ToolboxItems />
    </File>
    ```

## <a name="see-also"></a>Ayrıca bkz.

- [İzlenecek yol: Kullanarak SDK oluşturmaC++](../extensibility/walkthrough-creating-an-sdk-using-cpp.md)
- [İzlenecek yol: Veya Visual Basic kullanarak C# SDK oluşturma](../extensibility/walkthrough-creating-an-sdk-using-csharp-or-visual-basic.md)
- [Bir projedeki başvuruları yönetme](../ide/managing-references-in-a-project.md)
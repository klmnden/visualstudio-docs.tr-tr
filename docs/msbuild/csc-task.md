---
title: Csc görevi | Microsoft Docs
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- http://schemas.microsoft.com/developer/msbuild/2003#Csc
dev_langs:
- VB
- CSharp
- C++
- jsharp
helpviewer_keywords:
- Csc task [MSBuild]
- MSBuild, Csc task
ms.assetid: d8c19b36-f5ca-484b-afa6-8ff3b90e103a
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 9df54befff79b82703cb363fea92536285c68232
ms.sourcegitcommit: 4dfe098ac0df294aad63e6b384d6575980798ca3
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/11/2019
ms.locfileid: "70888020"
---
# <a name="csc-task"></a>Csc görevi
*CSC. exe*' yi sarmalayan ve yürütülebilir dosyalar ( *. exe* dosyaları), dinamik bağlantı kitaplıkları ( *. dll* dosyaları) veya kod modülleri ( *. netmodule* dosyaları) oluşturur. *CSC. exe*hakkında daha fazla bilgi için bkz [ C# . derleyici seçenekleri](/dotnet/csharp/language-reference/compiler-options/index).

## <a name="parameters"></a>Parametreler
Aşağıdaki tablo, `Csc` görevin parametrelerini açıklar.

| Parametre | Açıklama |
|------------------------------| - |
| `AdditionalLibPaths` | İsteğe `String[]` bağlı parametre.<br /><br /> Başvuruların aranacağı ek dizinleri belirtir. Daha fazla bilgi için bkz. [-libC# (derleyici seçenekleri)](/dotnet/csharp/language-reference/compiler-options/lib-compiler-option). |
| `AddModules` | İsteğe `String` bağlı parametre.<br /><br /> Derlemenin parçası olacak bir veya daha fazla modül belirtir. Daha fazla bilgi için bkz. [-addmoduleC# (derleyici seçenekleri)](/dotnet/csharp/language-reference/compiler-options/addmodule-compiler-option). |
| `AllowUnsafeBlocks` | İsteğe `Boolean` bağlı parametre.<br /><br /> İse `true`, [unsafe](/dotnet/csharp/language-reference/keywords/unsafe) anahtar sözcüğünü kullanan kodu derler. Daha fazla bilgi için bkz. [-unsafeC# (derleyici seçenekleri)](/dotnet/csharp/language-reference/compiler-options/unsafe-compiler-option). |
| `ApplicationConfiguration` | İsteğe `String` bağlı parametre.<br /><br /> Derleme bağlama ayarlarını içeren uygulama yapılandırma dosyasını belirtir. |
| `BaseAddress` | İsteğe `String` bağlı parametre.<br /><br /> DLL 'nin yükleneceği tercih edilen temel adresi belirtir. Bir DLL için varsayılan temel adres .NET Framework ortak dil çalışma zamanı tarafından ayarlanır. Daha fazla bilgi için bkz. [-BaseAddressC# (derleyici seçenekleri)](/dotnet/csharp/language-reference/compiler-options/baseaddress-compiler-option). |
| `CheckForOverflowUnderflow` | İsteğe `Boolean` bağlı parametre.<br /><br /> Veri türünün sınırlarını aşan tamsayı aritmetiğinin çalışma zamanında bir özel duruma neden olup olmayacağını belirtir. Daha fazla bilgi için bkz. [-CheckedC# (derleyici seçenekleri)](/dotnet/csharp/language-reference/compiler-options/checked-compiler-option). |
| `CodePage` | İsteğe `Int32` bağlı parametre.<br /><br /> Derlemedeki tüm kaynak kodu dosyaları için kullanılacak kod sayfasını belirtir. Daha fazla bilgi için bkz. [-CodePageC# (derleyici seçenekleri)](/dotnet/csharp/language-reference/compiler-options/codepage-compiler-option). |
| `DebugType` | İsteğe `String` bağlı parametre.<br /><br /> Hata ayıklama türünü belirtir. `DebugType``full` veya`pdbonly`olabilir. Varsayılan değer `full`, bir hata ayıklayıcının çalışan bir programa eklenmesini sağlar. Belirleme `pdbonly` , program hata ayıklayıcıda başlatıldığında kaynak kodu hata ayıklamayı sağlar, ancak yalnızca çalışan program hata ayıklayıcıya eklendiğinde assembler 'yi görüntüler.<br /><br /> Bu parametre, `EmitDebugInformation` parametresini geçersiz kılar.<br /><br /> Daha fazla bilgi için bkz. [-DebugC# (derleyici seçenekleri)](/dotnet/csharp/language-reference/compiler-options/debug-compiler-option). |
| `DefineConstants` | İsteğe `String` bağlı parametre.<br /><br /> Önişlemci sembolleri tanımlar. Daha fazla bilgi için bkz. [-defineC# (derleyici seçenekleri)](/dotnet/csharp/language-reference/compiler-options/define-compiler-option). |
| `DelaySign` | İsteğe `Boolean` bağlı parametre.<br /><br /> `true`Yalnızca ortak anahtarı derlemeye yerleştirmek istediğinizi belirtir. `false`, Tam olarak imzalanan bir derleme istediğinizi belirtir<br /><br /> `KeyFile` Ya`KeyContainer` da parametresiyle kullanılmamışsa, bu parametrenin hiçbir etkisi yoktur.<br /><br /> Daha fazla bilgi için bkz. [-delaysignC# (derleyici seçenekleri)](/dotnet/csharp/language-reference/compiler-options/delaysign-compiler-option). |
| `Deterministic` | İsteğe `Boolean` bağlı parametre.<br/><br/> İse `true`, derleyicinin özdeş olması halinde ikili içeriği derlemeler arasında özdeş olan bir derlemeyi çıkışına neden olur.<br/><br/>Daha fazla bilgi için bkz. [-belirleyiciC# (derleyici seçenekleri)](/dotnet/csharp/language-reference/compiler-options/deterministic-compiler-option). |
| `DisabledWarnings` | İsteğe `String` bağlı parametre.<br /><br /> Devre dışı bırakılacak uyarıların listesini belirtir. Daha fazla bilgi için bkz. [-nowarnC# (derleyici seçenekleri)](/dotnet/csharp/language-reference/compiler-options/nowarn-compiler-option). |
| `DocumentationFile` | İsteğe `String` bağlı parametre.<br /><br /> Belge açıklamalarını bir XML dosyasına işler. Daha fazla bilgi için bkz. [-docC# (derleyici seçenekleri)](/dotnet/csharp/language-reference/compiler-options/doc-compiler-option). |
| `EmitDebugInformation` | İsteğe `Boolean` bağlı parametre.<br /><br /> `true`Görev hata ayıklama bilgilerini oluşturur ve bir program veritabanı (. pdb) dosyasına koyar. İse `false`, görev hata ayıklama bilgisi içermez. Varsayılan değer `false`. Daha fazla bilgi için bkz. [-DebugC# (derleyici seçenekleri)](/dotnet/csharp/language-reference/compiler-options/debug-compiler-option). |
| `ErrorReport` | İsteğe `String` bağlı parametre.<br /><br /> , Microsoft 'a bir C# iç hata raporlamak için kullanışlı bir yol sağlar. Bu parametre `prompt`, `send`, veya `none`değerine sahip olabilir. Parametresi olarak `prompt`ayarlandıysa, iç derleyici hatası oluştuğunda bir istem alırsınız. İstem bir hata raporunu Microsoft 'a elektronik olarak göndermenizi sağlar. Parametresi olarak ayarlandıysa `send`, bir hata raporu otomatik olarak gönderilir. Parametresi olarak `none`ayarlandıysa, hata yalnızca derleyicinin metin çıkışında raporlanır. Varsayılan değer `none`. Daha fazla bilgi için bkz. [-errorreportC# (derleyici seçenekleri)](/dotnet/csharp/language-reference/compiler-options/errorreport-compiler-option). |
| `FileAlignment` | İsteğe `Int32` bağlı parametre.<br /><br /> Çıkış dosyasındaki bölümlerin boyutunu belirtir. Daha fazla bilgi için bkz. [-filealignC# (derleyici seçenekleri)](/dotnet/csharp/language-reference/compiler-options/filealign-compiler-option). |
| `GenerateFullPaths` | İsteğe `Boolean` bağlı parametre.<br /><br /> İse `true`, derleyici çıkışında dosyanın mutlak yolunu belirtir. İse `false`, dosyanın adını belirtir. Varsayılan değer `false`. Daha fazla bilgi için bkz. [-fullpathsC# (derleyici seçenekleri)](/dotnet/csharp/language-reference/compiler-options/fullpaths-compiler-option). |
| `KeyContainer` | İsteğe `String` bağlı parametre.<br /><br /> Şifreleme anahtarı kapsayıcısının adını belirtir. Daha fazla bilgi için bkz. [-keycontainerC# (derleyici seçenekleri)](/dotnet/csharp/language-reference/compiler-options/keycontainer-compiler-option). |
| `KeyFile` | İsteğe `String` bağlı parametre.<br /><br /> Şifreleme anahtarını içeren dosya adını belirtir. Daha fazla bilgi için bkz. [-keyfileC# (derleyici seçenekleri)](/dotnet/csharp/language-reference/compiler-options/keyfile-compiler-option). |
| `LangVersion` | İsteğe `String` bağlı parametre.<br /><br /> Kullanılacak dilin sürümünü belirtir. Daha fazla bilgi için bkz. [-langversionC# (derleyici seçenekleri)](/dotnet/csharp/language-reference/compiler-options/langversion-compiler-option). |
| `LinkResources` | İsteğe <xref:Microsoft.Build.Framework.ITaskItem> bağlı`[]` parametre.<br /><br /> Çıkış dosyasında bir .NET Framework kaynağına bağlantı oluşturur; kaynak dosyası çıkış dosyasına yerleştirilmez.<br /><br /> Bu parametreye geçirilen öğeler, ve `LogicalName` `Access`adlı isteğe bağlı meta veri girişlerine sahip olabilir. `LogicalName`anahtarın parametresine karşılık gelir ve `Access` parametreyekarşılıkgelir.`accessibility-modifier` `identifier` `/linkresource` Daha fazla bilgi için bkz. [-linkresourceC# (derleyici seçenekleri)](/dotnet/csharp/language-reference/compiler-options/linkresource-compiler-option). |
| `MainEntryPoint` | İsteğe `String` bağlı parametre.<br /><br /> `Main` Metodun konumunu belirtir. Daha fazla bilgi için bkz. [-MainC# (derleyici seçenekleri)](/dotnet/csharp/language-reference/compiler-options/main-compiler-option). |
| `ModuleAssemblyName` | İsteğe `String` bağlı parametre.<br /><br /> Bu modülün bir parçası olacağı derlemenin adını belirtir. |
| `NoConfig` | İsteğe `Boolean` bağlı parametre.<br /><br /> İse `true`, derleyiciye *CSC. rsp* dosyası ile derlenmeyeceğini söyler. Daha fazla bilgi için bkz. [-noconfigC# (derleyici seçenekleri)](/dotnet/csharp/language-reference/compiler-options/noconfig-compiler-option). |
| `NoLogo` | İsteğe `Boolean` bağlı parametre.<br /><br /> İse `true`, derleyici başlık bilgilerinin görüntülenmesini önler. Daha fazla bilgi için bkz. [-nologoC# (derleyici seçenekleri)](/dotnet/csharp/language-reference/compiler-options/nologo-compiler-option). |
| `NoStandardLib` | İsteğe `Boolean` bağlı parametre.<br /><br /> , Tüm sistem ad alanını tanımlayan *mscorlib. dll*' nin içe aktarımını önler. `true` Kendi sistem ad alanınızı ve nesnelerinizi tanımlamak veya oluşturmak istiyorsanız bu parametreyi kullanın. Daha fazla bilgi için bkz. [-nostdlibC# (derleyici seçenekleri)](/dotnet/csharp/language-reference/compiler-options/nostdlib-compiler-option). |
| `NoWin32Manifest` | İsteğe `Boolean` bağlı parametre.<br /><br /> `true`Varsayılan Win32 bildirimini eklemeyin. |
| `Optimize` | İsteğe `Boolean` bağlı parametre.<br /><br /> İse `true`iyileştirmeleri etkinleştirilir. İse `false`iyileştirmeleri devre dışı bırakır. Daha fazla bilgi için bkz. [-optimizeC# (derleyici seçenekleri)](/dotnet/csharp/language-reference/compiler-options/optimize-compiler-option). |
| `OutputAssembly` | İsteğe `String` bağlı çıkış parametresi.<br /><br /> Çıktı dosyasının adını belirtir. Daha fazla bilgi için bkz. [-OutC# (derleyici seçenekleri)](/dotnet/csharp/language-reference/compiler-options/out-compiler-option). |
| `OutputRefAssembly` | İsteğe `String` bağlı parametre.<br /><br /> Çıkış başvurusu derleme dosyasının adını belirtir. Daha fazla bilgi için bkz. [-refoutC# (derleyici seçenekleri)](/dotnet/csharp/language-reference/compiler-options/refout-compiler-option). |
| `PdbFile` | İsteğe `String` bağlı parametre.<br /><br /> Hata ayıklama bilgi dosyası adını belirtir. Varsayılan ad, *. pdb* uzantılı çıkış dosyası adıdır. |
| `Platform` | İsteğe `String` bağlı parametre.<br /><br /> Çıkış dosyası tarafından hedeflenen işlemci platformunu belirtir. Bu parametre `x86`, `x64`, veya `anycpu`değerine sahip olabilir. Varsayılan değer `anycpu`. Daha fazla bilgi için bkz. [-PlatformC# (derleyici seçenekleri)](/dotnet/csharp/language-reference/compiler-options/platform-compiler-option). |
| `References` | İsteğe <xref:Microsoft.Build.Framework.ITaskItem> bağlı`[]` parametre.<br /><br /> Görevin, belirtilen öğelerden ortak tür bilgilerini geçerli projeye almasına neden olur. Daha fazla bilgi için bkz. [-ReferenceC# (derleyici seçenekleri)](/dotnet/csharp/language-reference/compiler-options/reference-compiler-option).<br /><br /> Özgün "başvuru" [!INCLUDE[csprcs](../data-tools/includes/csprcs_md.md)] öğesine meta verileri `Aliases` ekleyerek [!INCLUDE[vstecmsbuild](../extensibility/internals/includes/vstecmsbuild_md.md)] bir dosyada başvuru diğer adı belirtebilirsiniz. Örneğin, aşağıdaki CSC komut satırında "LS1" diğer adını ayarlamak için:<br /><br /> `CSC /r:LS1=MyCodeLibrary.dll /r:LS2=MyCodeLibrary2.dll *.cs`<br /><br /> Şunu kullanabilirsiniz:<br /><br /> `<Reference Include="MyCodeLibrary"> <Aliases>LS1</Aliases> </Reference>` |
| `Resources` | İsteğe <xref:Microsoft.Build.Framework.ITaskItem> bağlı`[]` parametre.<br /><br /> Bir .NET Framework kaynağını çıkış dosyasına katıştırır.<br /><br /> Bu parametreye geçirilen öğeler, ve `LogicalName` `Access`adlı isteğe bağlı meta veri girişlerine sahip olabilir. `LogicalName`anahtarın parametresine karşılık gelir ve `Access` parametreyekarşılıkgelir.`accessibility-modifier` `identifier` `/resource` Daha fazla bilgi için bkz. [-ResourceC# (derleyici seçenekleri)](/dotnet/csharp/language-reference/compiler-options/resource-compiler-option). |
| `ResponseFiles` | İsteğe `String` bağlı parametre.<br /><br /> Bu görev için komutları içeren yanıt dosyasını belirtir. Daha fazla bilgi için bkz. [@ (yanıt dosyası belirtme)](/dotnet/csharp/language-reference/compiler-options/response-file-compiler-option). |
| `Sources` | İsteğe <xref:Microsoft.Build.Framework.ITaskItem> bağlı`[]` parametre.<br /><br /> Bir veya daha fazla [!INCLUDE[csprcs](../data-tools/includes/csprcs_md.md)] kaynak dosyasını belirtir. |
| `TargetType` | İsteğe `String` bağlı parametre.<br /><br /> Çıktı dosyasının dosya biçimini belirtir. Bu parametre, bir, bir Windows `library`programı oluşturan veya `winexe`bir modül oluşturan bir `exe`konsol uygulaması `module`oluşturan bir ' ' değeri olabilir. Varsayılan değer `library` şeklindedir. Daha fazla bilgi için bkz. [-targetC# (derleyici seçenekleri)](/dotnet/csharp/language-reference/compiler-options/target-compiler-option). |
| `TreatWarningsAsErrors` | İsteğe `Boolean` bağlı parametre.<br /><br /> Varsa `true`, tüm uyarıları hata olarak değerlendirir. Daha fazla bilgi için bkz. [-warnaserrorC# (derleyici seçenekleri)](/dotnet/csharp/language-reference/compiler-options/warnaserror-compiler-option). |
| `UseHostCompilerIfAvailable` | İsteğe `Boolean` bağlı parametre.<br /><br /> Görev, varsa, işlem içi derleyici nesnesini kullanmasını söyler. Yalnızca tarafından [!INCLUDE[vsprvs](../code-quality/includes/vsprvs_md.md)]kullanılır. |
| `Utf8Output` | İsteğe `Boolean` bağlı parametre.<br /><br /> Derleyici çıkışını UTF-8 kodlaması kullanarak günlüğe kaydeder. Daha fazla bilgi için bkz. [-utf8outputC# (derleyici seçenekleri)](/dotnet/csharp/language-reference/compiler-options/utf8output-compiler-option). |
| `WarningLevel` | İsteğe `Int32` bağlı parametre.<br /><br /> Derleyicinin görüntüleyeceği uyarı düzeyini belirtir. Daha fazla bilgi için bkz. [-WarnC# (derleyici seçenekleri)](/dotnet/csharp/language-reference/compiler-options/warn-compiler-option). |
| `WarningsAsErrors` | İsteğe `String` bağlı parametre.<br /><br /> Hata olarak değerlendirmek için uyarıların listesini belirtir. Daha fazla bilgi için bkz. [-warnaserrorC# (derleyici seçenekleri)](/dotnet/csharp/language-reference/compiler-options/warnaserror-compiler-option).<br /><br /> Bu parametre, `TreatWarningsAsErrors` parametresini geçersiz kılar. |
| `WarningsNotAsErrors` | İsteğe `String` bağlı parametre.<br /><br /> Hata olarak değerlendirilmediğini belirten uyarıların bir listesini belirtir. Daha fazla bilgi için bkz. [-warnaserrorC# (derleyici seçenekleri)](/dotnet/csharp/language-reference/compiler-options/warnaserror-compiler-option).<br /><br /> Bu parametre yalnızca `TreatWarningsAsErrors` parametresi olarak `true`ayarlandıysa faydalıdır. |
| `Win32Icon` | İsteğe `String` bağlı parametre.<br /><br /> **Dosya Gezgini**'nde, çıktı dosyasına istenen görünümü sağlayan bir *. ico* dosyasını derlemeye ekler. Daha fazla bilgi için bkz. [-win32iconC# (derleyici seçenekleri)](/dotnet/csharp/language-reference/compiler-options/win32icon-compiler-option). |
| `Win32Manifest` | İsteğe `String` bağlı parametre.<br /><br /> Dahil edilecek Win32 bildirimini belirtir. |
| `Win32Resource` | İsteğe `String` bağlı parametre.<br /><br /> Çıktı dosyasına bir Win32 kaynağı ( *. res*) dosyası ekler. Daha fazla bilgi için bkz. [-win32resC# (derleyici seçenekleri)](/dotnet/csharp/language-reference/compiler-options/win32res-compiler-option). |

## <a name="remarks"></a>Açıklamalar
Yukarıda listelenen parametrelere ek olarak, bu görev sınıfından devralan sınıfından devralan sınıfından parametreleri `Microsoft.Build.Tasks.ManagedCompiler` <xref:Microsoft.Build.Tasks.ToolTaskExtension> <xref:Microsoft.Build.Utilities.ToolTask> devralır. Bu ek parametrelerin ve açıklamalarının listesi için bkz. [ToolTaskExtension temel sınıfı](../msbuild/tooltaskextension-base-class.md).

## <a name="example"></a>Örnek
Aşağıdaki örnek, `Compile` öğe koleksiyonundaki `Csc` kaynak dosyalardan bir yürütülebilir dosya derlemek için görevini kullanır.

```xml
<CSC
    Sources="@(Compile)"
    OutputAssembly="$(AppName).exe"
    EmitDebugInformation="true" />
```

## <a name="see-also"></a>Ayrıca bkz.
- [Görev başvurusu](../msbuild/msbuild-task-reference.md)
- [Görevler](../msbuild/msbuild-tasks.md)

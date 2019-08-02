---
title: Live Unit Testing SSS
ms.date: 10/03/2017
ms.topic: conceptual
helpviewer_keywords:
- Visual Studio ALM
- Live Unit Testing FAQ
author: rpetrusha
ms.author: ronpet
ms.workload:
- dotnet
ms.openlocfilehash: 41d5248106b831accf4d71f97aeaeb72fdbc5018
ms.sourcegitcommit: 044bb54cb4552c8f4651feb11d62e52726117e75
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/30/2019
ms.locfileid: "68662018"
---
# <a name="live-unit-testing-frequently-asked-questions"></a>Live Unit Testing sık sorulan sorular

## <a name="latest-features"></a>En son özellikler

**Live Unit Testing düzenli olarak geliştirilmiştir ve geliştirilmiştir. En son yeni özellikler ve geliştirmeler hakkında nasıl bilgi bulabilirim?**

Live Unit Testing yapılan yeni özellikler ve geliştirmeler hakkında bilgi edinmek için bkz. [Live Unit Testing](live-unit-testing-whats-new.md)yenilikleri.

## <a name="supported-frameworks-and-versions"></a>Desteklenen çerçeveler ve sürümler

**Hangi test çerçeveleri Live Unit Testing destekler ve desteklenen en düşük sürüm nedir?**

Live Unit Testing, aşağıdaki tabloda listelenen üç popüler birim testi çerçevesi ile birlikte kullanılabilir. Desteklenen en düşük sürüm bağdaştırıcılarının ve çerçeveleri de tabloda listelenir. Birim testi çerçevelerini NuGet.org adresinden tüm kullanılabilir.

|Test çerçevesi  |Visual Studio bağdaştırıcısı en düşük sürüm  |Framework en düşük sürüm  |
|---------|---------|---------|
|xUnit.net |xunit.Runner.VisualStudio sürüm 2.2.0-beta3-build1187 |xunit 1.9.2 |
|NUnit |NUnit3TestAdapter sürümü 3.7.0 |NUnit 3.5.0 sürümü |
|MSTest |MSTest.TestAdapter 1.1.4-preview |MSTest.TestFramework 1.0.5-preview |

Başvuruda `Microsoft.VisualStudio.QualityTools.UnitTestFramework` bulunan ve daha yeni MSTest NuGet paketlerine geçmek istemediğiniz daha eski bir test projesi varsa, Visual Studio 2017 sürüm 15,4 veya sonraki bir sürüme yükseltin.

Bazı durumlarda, açıkça için Live Unit Testing çalışmaya sırayla çözümde proje tarafından başvurulan NuGet paketlerini geri yüklemek gerekebilir. Çözümün açık bir derlemesini gerçekleştirerek ( **derleme**, en üst düzey Visual Studio 'dan **çözümü yeniden derle** ) ya da çözüme sağ tıklayıp önce **NuGet paketlerini geri yükle** ' yi seçerek paketleri geri yükleyebilirsiniz Oturma birimi sınamasını etkinleştirme.

## <a name="net-core-support"></a>.NET Core desteği

**Live Unit Testing .NET Core ile çalışıyor mu?**

Evet. Live Unit Testing .NET Core ve .NET Framework ile birlikte kullanılabilir. .NET Core desteği Visual Studio 2017 sürüm 15,3 ' ye eklenmiştir. .NET Core için Live Unit Testing desteğini istiyorsanız, Visual Studio 'nun bu sürümüne veya daha yenisine yükseltin.

## <a name="configuration"></a>Yapılandırma

**Bu öğeyi kapatdığımda neden Live Unit Testing çalışmıyor?**

**Çıkış** penceresi (Live Unit Testing açılan pencere seçildiğinde) Live Unit Testing neden çalışmadığını anlamalıdır. Aşağıdaki nedenlerden biri için Live Unit Testing çalışmayabilir:

- Çözümdeki projeler tarafından başvurulan NuGet paketleri geri yüklenemediğinde Live Unit Testing çalışmaz. Çözümün açık bir derlemesini yapmak veya Live Unit Testing açılmadan önce çözümde NuGet paketlerini geri yüklemek, bu sorunu çözmelidir.

- Projelerinizde MSTest tabanlı testler kullanıyorsanız, başvurusunu `Microsoft.VisualStudio.QualityTools.UnitTestFramework`kaldırdığınızdan ve en son MSTest NuGet `MSTest.TestAdapter` paketlerine başvurular eklediğinizden emin olun (en düşük sürüm 1.1.11 gereklidir) ve `MSTest.TestFramework` (en düşük sürüm) 1.1.11 gerekir). Daha fazla bilgi için, [Visual Studio 'da Live Unit Testing kullanma](live-unit-testing.md#supported-test-frameworks) makalesindeki "desteklenen test çerçeveleri" bölümüne bakın.

- Çözümünüzde en az bir projede bir NuGet başvurusu veya xUnit, NUnit veya MSTest test çerçevesine doğrudan başvuru olmalıdır. Bu proje Ayrıca karşılık gelen bir Visual Studio test bağdaştırıcıları NuGet paketine başvurmalıdır. Visual Studio test bağdaştırıcısına bir *. runsettings* dosyası aracılığıyla da başvurulabilir. *. Runsettings* dosyası aşağıdaki örnekteki gibi bir girdiye sahip olmalıdır:

```xml
<RunSettings>
    <RunConfiguration>
          <TestAdaptersPaths>path-to-your-test-adapter</TestAdaptersPaths>
     </RunConfiguration>
</RunSettings>
```

## <a name="incorrect-coverage-after-upgrade"></a>Yükseltmeden sonra yanlış kapsam

**Visual Studio projelerinizde başvurulan test bağdaştırıcısını desteklenen sürüme yükselttikten sonra neden Live Unit Testing yanlış kapsamı gösteriyor?**

- Çözümdeki birden çok proje NuGet test bağdaştırıcısı paketine başvuruda bulunursa, her birinin desteklenen sürüme yükseltilmesi gerekir.

- Test bağdaştırıcısı paketinden içeri aktarılan MSBuild *. props* dosyasının da doğru şekilde güncelleştirildiğinden emin olun. Genellikle proje dosyasının en üstünde bulunan, aşağıdaki gibi, bir içeri aktarmanın NuGet paketi sürümünü/yolunu denetleyin:

   ```xml
    <Import Project="..\packages\xunit.runner.visualstudio.2.2.0\build\net20\xunit.runner.visualstudio.props" Condition="Exists('..\packages\xunit.runner.visualstudio.2.2.0\build\net20\xunit.runner.visualstudio.props')" />
   ```

## <a name="customize-builds"></a>Derlemeleri Özelleştir

**Live Unit Testing Derlemelerimi özelleştirebilir miyim?**

Çözümünüz, "normal" işaretlenmiş olmayan derleme için gerekli olmayan izleme (Live Unit Testing) için derleme için özel adımlar gerektiriyorsa, projenize veya *. targets* dosyalarına `BuildingForLiveUnitTesting` özelliği denetleyen ve özel ön/sonrası oluşturma adımları gerçekleştirir. Ayrıca, belirli derleme adımlarını (paket yayımlama veya oluşturma gibi) ya da bu proje özelliğine dayalı Live Unit Testing bir yapıya derleme adımları (örneğin, önkoşulları kopyalama) eklemeyi seçebilirsiniz. Bu özelliğe göre yapınızı özelleştirmek, normal derlemenizi herhangi bir şekilde değiştirmez ve yalnızca Live Unit Testing yapıları etkiler.

Örneğin, normal bir derleme sırasında NuGet paketleri üreten bir hedef olabilir. Yaptığınız her Düzenlemeden sonra NuGet paketlerinin oluşturulmasını istemezsiniz. Bu nedenle, aşağıdaki gibi bir şey yaparak Live Unit Testing derlemesinde bu hedefi devre dışı bırakabilirsiniz:  

```xml
<Target Name="GenerateNuGetPackages" BeforeTargets="AfterBuild" Condition="'$(BuildingForLiveUnitTesting)' != 'true'">
    <Exec Command='"$(MSBuildThisFileDirectory)..\tools\GenPac" '/>
</Target>
```

## <a name="error-messages-with-ltoutputpathgt-or-ltoutdirgt"></a>OutputPath &lt;&gt; veya&lt;OutDir ile hata iletileri&gt;

**Live Unit Testing çözümümüzü derlemeyi denediğinde neden aşağıdaki hatayı alıyorum: "... koşulsuz olarak ayarlanan `<OutputPath>` veya `<OutDir>`olarak görünür. Live Unit Testing, çıkış derlemesinden testleri yürütmez "?**

Çözümünüz için derleme işlemi koşulsuz olarak `<OutputPath>` `<BaseOutputPath>`geçersiz kılındığında veya `<OutDir>` bir alt dizini olmaması durumunda bu hatayı alabilirsiniz. Bu gibi durumlarda Live Unit Testing, derleme yapıtlarının altındaki `<BaseOutputPath>`bir klasöre bırakıldığından emin olmak için bu değerleri geçersiz kıldığından çalışmayacaktır. Yapı yapıtlarınızın düzenli bir yapıda kesilmesini istediğiniz konumu geçersiz kılmanız gerekiyorsa, `<OutputPath>` koşullu olarak `<BaseOutputPath>`' yi geçersiz kılın.

Örneğin, derlemeniz aşağıda gösterildiği `<OutputPath>` gibi geçersiz kılar:

```xml 
<Project>
  <PropertyGroup>
    <OutputPath>$(SolutionDir)Artifacts\$(Configuration)\bin\$(MSBuildProjectName)</OutputPath>
  </PropertyGroup>
</Project>
```

ardından, aşağıdaki XML ile değiştirebilirsiniz:

```xml 
<Project>
  <PropertyGroup>
    <BaseOutputPath Condition="'$(BaseOutputPath)' == ''">$(SolutionDir)Artifacts\$(Configuration)\bin\$(MSBuildProjectName)\</BaseOutputPath>
    <OutputPath Condition="'$(OutputPath)' == ''">$(BaseOutputPath)</OutputPath>
  </PropertyGroup>
</Project>
```

Bu, `<OutputPath>` `<BaseOutputPath>` klasörün içinde olmasını sağlar.

Doğrudan derleme sürecinizdeki üzerine `<OutDir>` vermeyin; derleme yapıtlarını belirli bir konuma bırakmak yerine geçersiz kılın. `<OutputPath>`

## <a name="set-the-location-of-build-artifacts"></a>Derleme yapıtlarının konumunu ayarlama

**Live Unit Testing derleme yapıtlarının, *. vs* klasörü altındaki varsayılan konum yerine belirli bir konuma gitmesini istiyorum. Bunu nasıl değiştirebilirim?**

`LiveUnitTesting_BuildRoot` Kullanıcı düzeyi ortam değişkenini Live Unit Testing derleme yapıtlarının kesilmesini istediğiniz yola ayarlayın. 

## <a name="test-explorer-vs-live-unit-testing-test-runs"></a>Test Gezgini ile Test çalıştırmaları Live Unit Testing

**Test Gezgini penceresinden testlerin Live Unit Testing testlerin çalıştırılmasının farkı nasıl çalışır?**

Çeşitli farklılıklar vardır:

- **Test Gezgini** penceresinde testleri çalıştırmak veya hata ayıklamak, düzenli ikili dosyalar çalıştırlarken Live Unit Testing, işaretlenmiş ikililer çalıştırır. Araçlı ikililerin hata ayıklaması yapmak istiyorsanız, [hata ayıklayıcı ekleme.](xref:System.Diagnostics.Debugger.Launch) test yönteinizde başlatma yöntemi çağrısı, bu yöntem yürütüldüğünde hata ayıklayıcının başlatılmasına neden olur (Live Unit Testing tarafından yürütüldüğünde dahil) ve daha sonra ekleyebilirsiniz ve belgelenmiş ikilide hata ayıklayın. Bununla birlikte, umuyoruz çoğu kullanıcı senaryosunda sizin için şeffaf ve işaretlenmiş ikililerin hata ayıklamanıza gerek kalmaz.

- Live Unit Testing testleri çalıştırmak için yeni bir uygulama etki alanı oluşturmaz, ancak **Test Gezgini** penceresinden çalıştırılan testler yeni bir uygulama etki alanı oluşturur.

- Live Unit Testing her bir test derlemesindeki testleri sırayla çalıştırır; **Test Gezgini** penceresinde, paralel olarak birden çok test çalıştırmayı seçebilirsiniz.

- Live Unit Testing testlerin keşfi ve yürütülmesi sürüm 2 `TestPlatform`' yi kullanır, ancak **Test Gezgini** penceresi 1 sürümünü kullanır. Ancak çoğu durumda fark vermezsiniz.

- **Test Gezgini** Şu anda tek iş parçacıklı bir grupta (STA) testleri çalıştırır, Live Unit Testing çoklu iş parçacıklı bir grupta (MTA) testleri çalıştırır. Live Unit Testing 'de STA 'da MSTest testlerini çalıştırmak için, test yöntemini veya içeren sınıfı, `<STATestMethod>` `MSTest.STAExtensions 1.0.3-beta` NuGet paketinde bulunan veya `<STATestClass>` özniteliğiyle süsle birlikte kullanabilirsiniz. NUnit için, `<RequiresThread(ApartmentState.STA)>` özniteliğiyle birlikte test yöntemini ve xUnit için `<STAFact>` özniteliği ile süslemek için.

## <a name="exclude-tests"></a>Testleri hariç tut

**Nasıl yaparım? testlerin Live Unit Testing katılmasını hariç tutsın mı?**

Kullanıcıya özgü ayar için, [Visual Studio 'da Live Unit Testing kullanma](live-unit-testing.md#include-and-exclude-test-projects-and-test-methods) makalesindeki "test projelerini ve test yöntemlerini ekleme ve dışlama" bölümüne bakın. Belirli bir düzenleme oturumu için belirli bir test kümesini çalıştırmak veya kendi kişisel tercihlerinizi sürdürmek istediğinizde, testlerin dahil edilmesi veya dışlanması yararlı olur.

Çözüme özgü ayarlar için, metodu, özellikleri, sınıfları <xref:System.Diagnostics.CodeAnalysis.ExcludeFromCodeCoverageAttribute?displayProperty=fullName> veya yapıları Live Unit Testing tarafından işaretlenmiş olarak hariç tutmak için programlı olarak özniteliği uygulayabilirsiniz. Ayrıca, projenin tamamını işaretlenmiş olarak hariç `<ExcludeFromCodeCoverage>` tutmak için `true` özelliği proje dosyanızda olarak ayarlayabilirsiniz. Live Unit Testing, henüz eklenmemiş testleri çalıştırmaya devam eder, ancak kapsamı görselleştirilecektir.

Ayrıca, geçerli uygulama etki `Microsoft.CodeAnalysis.LiveUnitTesting.Runtime` alanına yüklenip yüklenmediğini denetleyebilir ve Testleri neden temel alarak devre dışı bırakabilirsiniz. Örneğin, xUnit ile aşağıdakine benzer bir şey yapabilirsiniz:

```csharp
[ExcludeFromCodeCoverage]
public class SkipLiveFactAttribute : FactAttribute
{
   private static bool s_lutRuntimeLoaded = AppDomain.CurrentDomain.GetAssemblies().Any(a => a.GetName().Name ==
                                            "Microsoft.CodeAnalysis.LiveUnitTesting.Runtime");
   public override string Skip => s_lutRuntimeLoaded ? "Test excluded from Live Unit Testing" : "";
}

public class Class1
{
   [SkipLiveFact]
   public void F()
   {
      Assert.True(true);
   }
}
```

## <a name="win32-pe-headers"></a>Win32 PE üstbilgileri

**Canlı birim testi tarafından oluşturulan işaretlenmiş derlemelerde Win32 PE üstbilgileri neden farklıdır?**

Bu sorun düzeltildi ve Visual Studio 2017 sürüm 15,3 ve sonraki sürümlerde yok.

Visual Studio 2017 ' nin eski sürümleri için, Live Unit Testing derlemelerin aşağıdaki Win32 PE başlık verilerini ekleyememesi ile sonuçlanabileceğini belirten bilinen bir hata vardır:

- Dosya sürümü (kodda tarafından @System.Reflection.AssemblyFileVersionAttribute belirtilen).

- Win32 simgesi (komut satırında `/win32icon:` tarafından belirtilen).

- Win32 bildirimi (komut satırında `/win32manifest:` tarafından belirtilen).

Bu değerleri kullanan testler, canlı birim testi tarafından yürütüldüğünde başarısız olabilir.

## <a name="continuous-builds"></a>Sürekli derlemeler

**Canlı birim testi neden, hiç bir düzenleme yapmadığım halde çözümümüzü her zaman oluşturmaya devam ediyor?**

Çözümünüzün yapı işlemi çözümün kendisinin parçası olan kaynak kodu oluşturursa ve yapı hedef dosyalarınızda uygun girişler ve çıkışlar belirtilmemişse çözümünüz, düzenleme yapmasanız bile oluşturabilir. MSBuild 'in uygun güncel denetimleri gerçekleştirebilmesi ve yeni bir derleme gerekip gerekmediğini belirleyebilmesi için, hedeflerin bir giriş ve çıkış listesi verilmelidir.

Live Unit Testing, kaynak dosyaların değiştiğini algıladığında bir derlemeyi başlatır. Çözümünüzün derlemesi kaynak dosyalar oluşturduğundan Live Unit Testing sonsuz bir derleme döngüsüne alınacaktır. Ancak, Live Unit Testing ikinci derlemeyi başlattığında hedefin giriş ve çıkışları işaretlenirse (önceki derlemeden yeni oluşturulan kaynak dosyalarını algıladıktan sonra), girişler ve çıkışlar kontrol ettiği için derleme döngüsünün dışına çıkar. Her şeyin güncel olduğunu gösterir.  

## <a name="new-process-coverage"></a>Yeni işlem kapsamı

**Neden bir test tarafından oluşturulan yeni bir işlemden Live Unit Testing neden yakalanmaz?**

Bu bilinen bir sorundur ve sonraki bir sürümde düzeltilmelidir.

## <a name="including-or-excluding-tests-doesnt-work"></a>Testleri ekleme veya hariç tutma çalışmıyor

**Testleri canlı test kümesine dahil ettikten veya hariç tutdığımda neden hiçbir şey olmuyor?**

Bu sorun düzeltildi ve Visual Studio 2017 sürüm 15,3 ve sonraki sürümlerde yok.

Visual Studio 2017 ' nin eski sürümleri için bu bilinen bir sorundur. Bu sorunu geçici olarak çözmek için, testlerinizi dahil ettikten veya hariç tutduktan sonra herhangi bir dosyaya düzenleme yapmanız gerekir.

## <a name="editor-icons"></a>Düzenleyici simgeleri

**Neden, çıkış penceresindeki iletilere göre testlerin çalıştırılmasına rağmen Live Unit Testing düzenleyicide hiç simge görmüyorum?**

Live Unit Testing üzerinde çalışan derlemeler herhangi bir nedenle işaretlenmemişse düzenleyicide simge göremeyebilirsiniz. Örneğin, Live Unit Testing, tarafından ayarlanan `<UseHostCompilerIfAvailable>false</UseHostCompilerIfAvailable>`projelerle uyumlu değildir. Bu durumda, derleme işleminizin bu ayarı kaldırmak veya Live Unit Testing çalışması için olarak `true` değiştirmek üzere güncelleştirilmesi gerekir. 

## <a name="capture-logs"></a>Günlükleri yakala

**Hata raporlarına dosya eklemek için daha ayrıntılı Günlükler mi Nasıl yaparım??**

Daha ayrıntılı Günlükler toplamak için birkaç şey yapabilirsiniz:

- **Araçlar** > **Seçenekler** Live Unit Testing gidin ve günlük seçeneğini Verbose olarak değiştirin. >  Ayrıntılı günlük kaydı, **Çıkış** penceresinde daha ayrıntılı günlüklerin gösterilmesine neden olur.

- `LiveUnitTesting_BuildLog` Kullanıcı ortam değişkenini, MSBuild günlüğünü yakalamak için kullanmak istediğiniz dosyanın adı olarak ayarlayın. Live Unit Testing derlemelerden ayrıntılı MSBuild günlük iletileri daha sonra bu dosyadan alınabilir.

- Test platformu günlüğünü yakalamak için `1` Kullanıcıortamdeğişkeniniolarakayarlayın.`LiveUnitTesting_TestPlatformLog` Live Unit Testing çalıştırmalarının ayrıntılı test platformu günlüğü iletileri daha sonra öğesinden `[Solution Root]\.vs\[Solution Name]\log\[VisualStudio Process ID]`alınabilir.

- Adlı `VS_UTE_DIAGNOSTICS` bir Kullanıcı düzeyi ortam değişkeni oluşturun ve bunu 1 (veya herhangi bir değer) olarak ayarlayın ve Visual Studio 'yu yeniden başlatın. Artık Visual Studio 'daki **çıkış testleri** sekmesinde çok fazla günlük görmeniz gerekir.

## <a name="see-also"></a>Ayrıca bkz.

- [Canlı Birim Testi](live-unit-testing.md)

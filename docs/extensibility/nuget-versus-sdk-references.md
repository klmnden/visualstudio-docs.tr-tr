---
title: Başvuru Eklerken NuGet veya Uzantı SDK Kullanma Karşılaştırması
ms.date: 08/02/2019
ms.topic: conceptual
author: madskristensen
ms.author: madsk
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 372e82f9bb032ac5a81362017d2062ecf0d44e3f
ms.sourcegitcommit: a124076dfd6b4e5aecda4d01984fee7b0c034745
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/05/2019
ms.locfileid: "68795084"
---
# <a name="nuget-versus-sdk-as-a-project-reference"></a>Proje başvurusu olarak NuGet ile SDK karşılaştırması

Bu makale, geliştiricilerin yazılımlarını bir NuGet paketi olarak veya bir yazılım geliştirme seti (SDK) olarak paketleyip paketetkinleştirilmeyeceğini seçmesini sağlamak için tasarlanmıştır. Özellikle, bir Visual Studio projesinde başvurulduklarında ikisi arasındaki farkları ele alır.

- [NuGet](/nuget) , kitaplıkları bir projeye ekleme sürecini kolaylaştıran açık kaynaklı bir paket yönetimi sistemidir. .NET için (.NET Core dahil), NuGet kodu paylaşmak için Microsoft tarafından desteklenen bir mekanizmadır. NuGet, .NET paketlerinin nasıl oluşturulduğunu, barındırıldığını ve kullanıldığını tanımlar ve bu rollerin her biri için araçlar sağlar. Visual Studio 'da, [Paket Yöneticisi](/nuget/consume-packages/install-use-packages-visual-studio) Kullanıcı arabirimini kullanarak NuGet paketlerini bir projeye eklersiniz.

- [SDK](../extensibility/creating-a-software-development-kit.md) , Visual Studio 'nun tek bir başvuru öğesi olarak davrandığı bir dosya koleksiyonudur. Visual Studio 'daki başvuru Yöneticisi iletişim kutusu, **Başvuru Ekle**' yi seçtiğinizde geçerli projeyle Ilgili tüm SDK 'ları listeler. Bir projeye SDK eklediğinizde, bu SDK 'nın tüm içeriğine IntelliSense, araç kutusu penceresi, tasarımcılar, Nesne Tarayıcısı, MSBuild, dağıtım, hata ayıklama ve paketleme aracılığıyla erişebilirsiniz.

## <a name="which-mechanism-should-i-use"></a>Hangi mekanizmayı kullanmalıyım?

Aşağıdaki tablo, bir SDK 'nın başvuru özelliklerini NuGet 'in başvuru özellikleriyle karşılaştırmanıza yardımcı olur.

| Özellik | SDK desteği | SDK notları | NuGet desteği | NuGet notları |
| - | - | - |---------------| - |
| Mekanizma bir varlığa başvurur ve tüm dosya ve işlevler kullanılabilir. | Y | **Başvuru Yöneticisi** iletişim kutusunu kullanarak bir SDK eklersiniz ve geliştirme iş akışı sırasında tüm dosya ve işlevler kullanılabilir. | Y | |
| MSBuild derlemeleri ve Windows meta veri ( *. winmd*) dosyalarını otomatik olarak tüketir. | Y | SDK 'daki başvurular otomatik olarak derleyiciye geçirilir. | Y | |
| MSBuild,. h veya. lib dosyalarını otomatik olarak kullanır. | Y | *SDKName. props* dosyası, Visual Studio 'nun Visual C++ Directory 'yi nasıl ayarlayacağını ve bu nedenle otomatik *. h* veya *. lib* dosya tüketimi için nasıl yapılacağını söyler. | N | |
| MSBuild otomatik olarak *. js* veya *. css* dosyalarını kullanır. | Y | **Çözüm Gezgini**, JavaScript SDK başvuru düğümünü genişleterek tek bir *. js* veya *. css* dosyasını gösterebilir ve ardından bu dosyaları kaynak dosyalarına sürükleyerek `<source include/>` Etiketler oluşturabilirsiniz. SDK, F5 ve otomatik paket kurulumunu destekler. | Y | |
| MSBuild, denetimi **araç kutusuna**otomatik olarak ekler. | Y | **Araç kutusu** SDK 'ları kullanabilir ve belirlediğiniz sekmelerde denetimleri gösterebilir. | N | |
| Mekanizması, uzantılar (VSıX) için Visual Studio Yükleyicisi destekler. | Y | VSıX SDK paketleri oluşturmak için özel bir bildirime ve mantığa sahiptir | Y | VSıX başka bir kurulum programına katıştırılabilir. |
| **Nesne tarayıcısı** , başvuruları numaralandırır. | Y | **Nesne tarayıcısı** SDK 'larda başvuruların listesini otomatik olarak alır ve sıralar. | N | |
| Dosyalar ve bağlantılar otomatik olarak **başvuru Yöneticisi** iletişim kutusuna eklenir (Yardım bağlantıları, vb. otomatik doldurma) | Y | **Başvuru Yöneticisi** iletişim kutusu, yardım BAĞLANTıLARı ve SDK bağımlılıklarının listesi Ile birlikte SDK 'ları otomatik olarak numaralandırır. | N | NuGet kendi **NuGet Paketlerini Yönet** iletişim kutusunu sağlar. |
| Mekanizması birden çok mimariyi destekler. | Y | SDK 'lar birden çok yapılandırma gönderebilir. MSBuild her proje yapılandırması için uygun dosyaları kullanır. | N | |
| Mekanizması birden çok yapılandırmayı destekler. | Y | SDK 'lar birden çok yapılandırma gönderebilir. MSBuild, proje mimarisine bağlı olarak her proje mimarisi için uygun dosyaları kullanır. | N | |
| Mekanizma "kopyalama için değil" belirtebilir. | Y | Dosyaların *\redist* veya *\designtime* klasöründe bırakıldığına bağlı olarak, hangi dosyaların tüketen uygulamanın paketine kopyalanacağını denetleyebilirsiniz. | N | Paket bildiriminde kopyalanacak dosyaları bildirirsiniz. |
| Yerelleştirilmiş dosyalarda içerik görüntülenir. | Y | SDK 'larda yerelleştirilmiş XML belgeleri, daha iyi bir tasarım zamanı deneyimi için otomatik olarak eklenir. | N | |
| MSBuild aynı anda bir SDK 'nın birden çok sürümünü kullanmayı destekler. | Y | SDK birden çok sürümü aynı anda kullanmayı destekler. | N | Bu başvuru değildir. Projenizde aynı anda birden fazla NuGet dosyası sürümü olamaz. |
| Mekanizması, geçerli hedef çerçeveleri, Visual Studio sürümlerini ve proje türlerini belirtmeyi destekler. | Y | **Başvuru Yöneticisi** iletişim kutusu ve **araç kutusu** yalnızca bir projeye uygulanan SDK 'ları gösterir, böylece kullanıcılar uygun SDK 'ları daha kolay seçebilirler. | Y (kısmi) | Özet, hedef çerçevedir. Kullanıcı arabiriminde filtreleme yok. Yükleme sırasında bir hata döndürebilir. |
| Mekanizması yerel Wınmds için kayıt bilgilerini belirtmeyi destekler. | Y | *SDKManifest. xml*dosyasındaki. winmd dosyası ve. dll dosyası arasında bağıntı belirtebilirsiniz. | N | |
| Mekanizması diğer SDK 'larda bağımlılıkları belirtmeyi destekler. | Y | SDK yalnızca kullanıcıya bildirir; Kullanıcı yine de onları yükleyip el ile başvurmalıdır. | Y | NuGet bunları otomatik olarak çeker; Kullanıcı bilgilendirilmez. |
| Mekanizması, uygulama bildirimi [!INCLUDE[win8_appstore_long](../debugger/includes/win8_appstore_long_md.md)] ve çerçeve kimliği gibi kavramlarla tümleştirilir. | Y | SDK, paketleme ve F5 [!INCLUDE[win8_appstore_short](../ide/includes/win8_appstore_short_md.md)] [!INCLUDE[win8_appstore_short](../ide/includes/win8_appstore_short_md.md)]' de bulunan SDK 'lar ile doğru şekilde çalışması için öğesine özgü kavramları iletmelidir. | N | |
| Mekanizması, uygulamalar için [!INCLUDE[win8_appname_long](../debugger/includes/win8_appname_long_md.md)] uygulama hata ayıklama işlem hattı ile tümleşir. | Y | SDK 'nın, [!INCLUDE[win8_appstore_short](../ide/includes/win8_appstore_short_md.md)] [!INCLUDE[win8_appstore_short](../ide/includes/win8_appstore_short_md.md)]paketlenmesi ve F5 'in ' de bulunan SDK 'lar ile düzgün çalışması için özel kavramlara sahip olması gerekir. | Y | NuGet içeriği projenin bir parçası haline gelir. Özel bir F5 değerlendirmesi gerekmez. |
| Mekanizması uygulama bildirimleri ile tümleşir. | Y | SDK 'nın, [!INCLUDE[win8_appstore_short](../ide/includes/win8_appstore_short_md.md)] [!INCLUDE[win8_appstore_short](../ide/includes/win8_appstore_short_md.md)]paketlenmesi ve F5 'in ' de bulunan SDK 'lar ile düzgün çalışması için özel kavramlara sahip olması gerekir. | Y | NuGet içeriği projenin bir parçası haline gelir. Özel bir F5 değerlendirmesi gerekmez. |
| Mekanizma, başvuru olmayan dosyaları dağıtır (örneğin, [!INCLUDE[win8_appname_long](../debugger/includes/win8_appname_long_md.md)] uygulama testlerinin çalıştırılacağı test çerçevesini dağıtın). | Y | Dosyaları *\redist* klasörüne bırakırsanız, dosyalar otomatik olarak dağıtılır. | Y | |
| Mekanizması, Platform SDK 'larını otomatik olarak Visual Studio IDE 'ye ekler. | Y | [!INCLUDE[win8](../debugger/includes/win8_md.md)] SDK 'yı veya Windows Phone SDK 'sını belirli bir düzen ile belirli bir konuma bırakırsanız, SDK otomatik olarak tüm Visual Studio özellikleriyle tümleştirilir. | N | |
| Mekanizması temiz bir geliştirici makinesini destekler. (Yani, yükleme gerekmez ve kaynak kod denetiminden basit alma işlemi çalışacaktır.) | N | Bir SDK 'ya başvursanız, çözümünüzü ve SDK 'yı ayrı ayrı iade etmeniz gerekir. SDK 'Yı, MSBuild 'in SDK 'Sı yineleme (Ayrıntılar için bkz. [yazılım geliştirme seti oluşturma](../extensibility/creating-a-software-development-kit.md)) varsayılan konumlarından farklı konumlardan iade edebilirsiniz. Alternatif olarak, özel bir konum SDK 'Lardan oluşuyorsa, proje dosyasında aşağıdaki kodu belirtebilirsiniz:<br /><br />`<PropertyGroup>`<br />&nbsp;&nbsp;`<SDKReferenceDirectoryRoot>`<br />&nbsp;&nbsp;`C:\MySDKs`<br />&nbsp;&nbsp;`</SDKReferenceDirectoryRoot>`<br />`</PropertyGroup>`<br /><br /> Daha sonra bu konuma SDK 'Ları kontrol edin. | Y | Çözümü kullanıma alabilirsiniz ve Visual Studio dosyaları hemen tanır ve üzerinde davranır. |
| Paket yazarlarının büyük bir topluluğuna katabilirsiniz. | Yok | Topluluk yenidir. | Y | |
| Paket tüketicilerinin büyük bir topluluğunu birleştirebilirsiniz. | Yok | Topluluk yenidir. | Y | |
| İş ortaklarının bir ekosistemine (özel galeriler, depolar vb.) katabilirsiniz. | Yok | Kullanılabilir depolar Visual Studio Market, Microsoft Indirme merkezi ve [!INCLUDE[win8_appstore_long](../debugger/includes/win8_appstore_long_md.md)]' i içerir. | Y | |
| Mekanizması, paket oluşturma ve tüketim için sürekli tümleştirme yapı sunucularıyla tümleştirilir. | Y | SDK, komut satırındaki iade edilme konumunu (SDKReferenceDirectoryRoot özelliği) MSBuild 'e iletmelidir. | Y | |
| Mekanizması hem kararlı hem de yayın öncesi paket sürümlerini destekler. | Y | SDK, birden çok sürüme başvuru eklemeyi destekler. | Y | |
| Mekanizması yüklü paketler için otomatik güncelleştirmeyi destekler. | Y | VSıX olarak veya Visual Studio otomatik güncelleştirme 'nin bir parçası olarak gönderilmemişse, SDK otomatik bildirimler sağlar. | Y | |
| Mekanizması, paket oluşturmak ve kullanmak için tek başına bir *. exe* dosyası içerir. | Y | SDK, *MSBuild. exe*' yi içerir. | Y | |
| Paketler sürüm denetimine iade edilebilir. | Y | Belge düğümü dışında bir şey iade edemeyebilirsiniz, bu da Uzantı SDK 'larının iade yapılmadığı anlamına gelir. Uzantı SDK 'sının boyutu büyük olabilir. | Y | |
| Paketleri oluşturmak ve kullanmak için bir PowerShell arabirimi kullanabilirsiniz. | Y (tüketim), N (oluşturma) | SDK oluşturmak için araç yok. Tüketim, komut satırında MSBuild 'i yürütüyor. | Y | |
| Hata ayıklama desteği için bir sembol paketi kullanabilirsiniz. | Y | *. Pdb* dosyalarını SDK 'ya düşürürsanız dosyalar otomatik olarak alınır. | Y | |
| Mekanizması, Paket Yöneticisi otomatik güncelleştirmelerini destekler. | Yok | SDK, MSBuild ile düzeltilir. | Y | |
| Mekanizması bir hafif bildirim biçimini destekler. | Y | *SDKManifest. xml* pek çok özniteliği destekler, ancak küçük bir alt küme genellikle gereklidir. | Y | |
| Mekanizmaya tüm Visual Studio sürümlerinde ulaşılabilir. | Y | SDK, tüm Visual Studio sürümlerini destekler. | Y | NuGet tüm Visual Studio sürümlerini destekler. |

## <a name="see-also"></a>Ayrıca bkz.

- [Bir projedeki başvuruları yönetme](../ide/managing-references-in-a-project.md)
- [Projedeki başvuruları yönetme (Mac için Visual Studio)](/visualstudio/mac/managing-references-in-a-project)
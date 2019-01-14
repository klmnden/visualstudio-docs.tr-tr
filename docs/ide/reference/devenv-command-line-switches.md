---
title: Devenv komut satırı anahtarları
ms.date: 12/10/2018
ms.prod: visual-studio-dev15
ms.topic: reference
helpviewer_keywords:
- switches, Devenv
- command-line switches, Devenv
- command line [Visual Studio], switches
- Devenv
ms.assetid: e12bc6ed-74fd-4bea-8d7c-89b99c20bad8
author: gewarren
ms.author: gewarren
manager: douge
ms.workload:
- multiple
ms.openlocfilehash: 2c2ea1bfc4cc49378308933dffd5bc3873b25209
ms.sourcegitcommit: 38db86369af19e174b0aba59ba1918a5c4fe4a61
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/14/2019
ms.locfileid: "54269676"
---
# <a name="devenv-command-line-switches"></a>Devenv komut satırı anahtarları

Devenv, IDE için çeşitli seçenekleri, projeleri derlemek, proje hata ayıklama ve projelerini komut satırından dağıtma olanak tanır. Bu anahtarlar, IDE bir betik veya bir .bat dosyasından (örneğin, Gecelik Yapı komut dosyası) çalıştırmak için veya belirli bir yapılandırmada IDE başlatmak için kullanın.

> [!NOTE]
> Derlemeyle ilgili görevler için devenv yerine MSBuild kullanmanız önerilir. Daha fazla bilgi için [MSBuild komut satırı başvurusu](../../msbuild/msbuild-command-line-reference.md).

VSPackage geliştirme ile ilgili anahtarları hakkında daha fazla bilgi için Ayrıca bkz: [VSPackage geliştirme için Devenv komut satırı anahtarları](../../extensibility/devenv-command-line-switches-for-vspackage-development.md).

## <a name="devenv-switch-syntax"></a>Devenv anahtarı sözdizimi

İle başlayan komutlar `devenv` tarafından işlenen `devenv.com` gibi standart sistem akışları çıkışını sunan yardımcı program `stdout` ve `stderr`. Çıktı, örneğin bir .txt dosyasına yakaladığında yardımcı programı uygun g/ç yönlendirmesi belirler.

Alternatif olarak, ile başlayan komutlar `devenv.exe` aynı anahtarlar kullanabilirsiniz ancak `devenv.com` yardımcı programı atlanır. Kullanarak `devenv.exe` doğrudan çıkış konsolda görüntülenmesini engeller.

Sözdizimi kurallarını için `devenv` anahtarları diğer DOS komut satırı yardımcı programları kurallarına benzer. Aşağıdaki sözdizimi kurallarını tümüne uygula `devenv` anahtarlar ve bunların bağımsız değişkenleri:

- İle başlayan komutlar `devenv`.

- Anahtarlar büyük küçük harfe duyarlı değildir.

- Bir kısa çizgi kullanarak bir anahtar belirtebilirsiniz ("-") veya eğik çizgi ("/").

- Bir çözüm veya proje belirtirken, ilk bağımsız değişken çözüm dosyası veya dosya yolu da dahil olmak üzere proje dosyasının adıdır.

- İlk bağımsız değişken bir çözüm veya proje değil bir dosya ise, bu dosyanın uygun düzenleyicide IDE yeni bir örneğini açar.

- Bir proje dosyası adı bir çözüm dosyası adı yerine sağladığında bir `devenv` komut aynı ada sahip bir çözüm dosyası için proje dosyasının üst klasörü arar. Örneğin, komut `devenv myproject1.vbproj /build` üst klasör için adlı bir çözüm dosyası arar `myproject1.sln`.

  > [!NOTE]
  > Bu projeye başvuran bir ve yalnızca bir çözüm dosyası, kendi üst klasörde bulunmalıdır. Üst klasör herhangi bir çözüm dosyası içeriyorsa bu projeye başvuran ya da üst klasör ona başvuran iki veya daha fazla çözüm dosyası içeriyorsa, ardından bir geçici çözüm dosyası oluşturulur.

- Dosya yolları ve dosya adı boşluklar, bunları tırnak içine almalısınız (""). Örneğin: `"c:\project a\"`

- Anahtarlar ve bağımsız değişkenler aynı satırda arasında bir boşluk karakteri Ekle. Örneğin, komut `devenv /log output.txt` IDE açılır ve tüm bilgilerini günlüğe kaydetme oturumu için için çýktý.txt çıkarır.

- Desen eşleştirme sözdizimi kullanamazsınız `devenv` komutları.

## <a name="devenv-switches"></a>Devenv anahtarları

Aşağıdaki komut satırı anahtarları, IDE görüntülemek ve açıklandığı gibi görev yapın.

|Komut satırı anahtarı|Açıklama|
| - |-----------------|
|[/Command](command-devenv-exe.md)|IDE'yi başlatır ve belirtilen komutu yürütür.<br /><br /> `devenv /command "nav https://docs.microsoft.com/"`|
|[/DebugExe](debugexe-devenv-exe.md)|Hata ayıklayıcının denetiminin altında bir C++ yürütülebilir dosyayı yükler. Visual Basic için bu anahtarı kullanılamıyor veya C# yürütülebilir. Daha fazla bilgi için [otomatik olarak hata ayıklayıcıda bir işlem başlatmak](../../debugger/debug-multiple-processes.md#BKMK_Automatically_start_an_process_in_the_debugger).<br /><br /> `devenv /debugexe mysln.exe`|
|[/Diff](diff.md)|İki dosyayı karşılaştırır. Dört parametre alır: *Kaynakdosya*, *TargetFile*, *SourceDisplayName* (isteğe bağlı) ve *TargetDisplayName* (isteğe bağlı).<br /><br /> `devenv /diff File1 File2 Alias1 Alias2`|
|[/Edit](edit-devenv-exe.md)|Belirtilen dosyalar, bu uygulamanın çalışan bir örneğini açar. Varsa çalışan örnek yoksa Basitleştirilmiş pencere düzenini ile yeni bir örneğini başlatır.<br /><br /> `devenv /edit File1 File2`|
|[/ LCID veya/l](lcid-devenv-exe.md)|IDE için varsayılan dili ayarlar. Belirtilen dil Visual Studio yüklemenizde bulunmaz, bu ayar yoksayılır.<br /><br /> `devenv /l 1033`|
|[/Log](log-devenv-exe.md)|Visual Studio başlatılır ve tüm etkinlik günlük dosyasına kaydeder.<br /><br /> `devenv /log mylogfile.xml`|
|[/NoSplash](nosplash-devenv-exe.md)|Karşılama ekranında olmadan IDE açılır.<br /><br /> `devenv /nosplash File1 File2`|
|[/ Run veya /R](run-devenv-exe.md)|Derler ve belirtilen çözüm çalıştırır.<br /><br /> `devenv /run mysln.sln`|
|[/ RunExit](runexit-devenv-exe.md)|Derler ve belirtilen çözüm çalıştırır, çözüm çalıştırılır ve çözüm çalışması bittikten sonra IDE'yi kapatır, IDE'nin en aza indirir.<br /><br /> `devenv /runexit mysln.sln`|
|[/SafeMode](safemode-devenv-exe.md)|Visual Studio güvenli modda başlatır. Bu anahtar yalnızca varsayılan ortama, varsayılan Hizmetleri ve üçüncü taraf paketlerini sevk edilen sürümlerini yükler.<br /><br /> Bu anahtar hiçbir bağımsız değişkeni alır.|
|[/UseEnv](useenv-devenv-exe.md)|C++ için derleme yolu, INCLUDE, LIBPATH ve LIB ortam değişkenlerini kullanmak IDE neden olur. Bu anahtar ile birlikte yüklenir **C++ ile masaüstü geliştirme** iş yükü. Daha fazla bilgi için [komut satırı derlemeleri için yolu ve ortam değişkenlerini ayarlama](/cpp/build/setting-the-path-and-environment-variables-for-command-line-builds).|

Aşağıdaki komut satırı anahtarları IDE gösterme.

|Komut satırı anahtarı|Açıklama|
| - |-----------------|
|[/?](q-devenv-exe.md)|Görüntüler için yardıma `devenv` geçer **komut istemi penceresi**.<br /><br /> Bu anahtar hiçbir bağımsız değişkeni alır.|
|[/Build](build-devenv-exe.md)|Belirtilen çözüm veya projeyi yapılandırmasına göre belirtilen çözümü derler.<br /><br /> `devenv mysln.sln /build`|
|[/Clean](clean-devenv-exe.md)|Kaynak dosyaları etkilemeden oluşturma komutu tarafından oluşturulan tüm dosyaları siler.<br /><br /> `devenv mysln.sln /clean`|
|[/Deploy](deploy-devenv-exe.md)|Çözümün yapılandırma göre bir dağıtım için gerekli dosyaları ile birlikte çözümü derler.<br /><br /> `devenv mysln.sln /deploy`|
|[/Out](out-devenv-exe.md)|Oluşturma sırasında hatalar almak için bir dosya belirtmenizi sağlar.<br /><br /> `devenv mysln.sln /build Debug /out log.txt`|
|[/Project](project-devenv-exe.md)|Projeyi oluşturmak için temizlemek veya dağıtmak. Yalnızca, ayrıca sağlandıysa bu anahtarı kullanabilirsiniz `/Build`, `/Rebuild`, `/Clean`, veya `/Deploy` geçin.<br /><br /> `devenv mysln.sln /build Debug /project proj1`|
|[/ProjectConfig](projectconfig-devenv-exe.md)|Derleme veya dağıtım için proje yapılandırmasını belirtir. Yalnızca, ayrıca sağlandıysa bu anahtarı kullanabilirsiniz `/Project` geçin.<br /><br /> `devenv mysln.sln /build Release /project proj1 /projectconfig Release`|
|[/Rebuild](rebuild-devenv-exe.md)|Temizler ve daha sonra belirtilen çözüm veya projeyi yapılandırmasına göre belirtilen çözümü derler.<br /><br /> `devenv mysln.sln /rebuild`|
|[/ResetSettings](resetsettings-devenv-exe.md)|Visual Studio varsayılan ayarlarına geri yükler. İsteğe bağlı olarak belirtilen ayarları sıfırlar `.vssettings` dosya.<br /><br /> `devenv /resetsettings mysettings.vssettings`|
|[/Upgrade](upgrade-devenv-exe.md)|Bu dosyalar için geçerli Visual Studio biçimlerinde belirtilen çözüm dosyasını ve tüm proje dosyaları ya da belirtilen proje dosyasını yükseltir.<br /><br /> `devenv mysln.sln /upgrade`|

## <a name="see-also"></a>Ayrıca bkz.

- [Genel, Ortam, Seçenekler İletişim Kutusu](general-environment-options-dialog-box.md)
- [VSPackage geliştirme için Devenv komut satırı anahtarları](../../extensibility/devenv-command-line-switches-for-vspackage-development.md)

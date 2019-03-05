---
title: Visual Studio 2017 genişletilebilirlikteki yeni değişiklikler
titleSuffix: ''
ms.date: 11/09/2016
ms.topic: conceptual
ms.assetid: 54d5af60-0b44-4ae1-aa57-45aa03f89f3d
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
monikerRange: vs-2017
ms.openlocfilehash: e7363a0779721e4fb36106d6ee77324c341517ba
ms.sourcegitcommit: 11337745c1aaef450fd33e150664656d45fe5bc5
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/04/2019
ms.locfileid: "57324201"
---
# <a name="changes-in-visual-studio-2017-extensibility"></a>Visual Studio 2017 genişletilebilirlik değişiklikleri

Visual Studio 2017 sağlar bir [daha hızlı, daha basit Visual Studio yükleme deneyimi](https://devblogs.microsoft.com/visualstudio/faster-leaner-visual-studio-installer) özellikler ve iş yükleri üzerinde daha fazla seçeneğin kullanıcılar sağlarken kullanıcı sistemlerinde Visual Studio etkisini azaltacak yüklü. Bu geliştirmeler desteklemek için değişiklikler, bazı önemli değişiklikler dahil olmak üzere genişletilebilirlik modeline yaptık. Bu makalede, bu değişiklikleri ve hangi onları adreslemek üzere yapılabilir teknik ayrıntılarını açıklar.

> [!NOTE]
> Bazı bilgiler zaman içinde nokta uygulamasının Ayrıntılar ve daha sonra değiştirilebilir.

## <a name="changes-affecting-vsix-format-and-installation"></a>VSIX biçimi ve yükleme etkileyen değişiklikler

Tanıtılan VSIX v3 Visual Studio 2017 (sürüm 3) basit bir yükleme deneyimini destekleyecek biçimde.

VSIX biçimi değişiklikler şunlardır:

* Kurulum Önkoşulları bildirimi. Visual Studio, hızlı yükleme basit, ' promise üzerinde sunmak için yükleyici artık kullanıcılara daha fazla yapılandırma seçeneği sunar. Sonuç olarak, özellik ve uzantı tarafından gerekli bileşenleri yüklü olduğundan emin olun, uzantıları bağımlılıklarını bildirmeniz gerekir.

  * Visual Studio 2017 yükleyicisi almak ve kullanıcı için gerekli olan bileşenler uzantınızı yüklemenin bir parçası olarak yüklemek otomatik olarak sunar.
  * Kullanıcılar ayrıca, bildirimde 15.0 sürümünü hedefleyen olarak işaretlenmiş olsa bile yeni VSIX v3 biçimi kullanılarak oluşturulmamış bir uzantıyı yüklemeye çalıştığında bir uyarı alırsınız.

* Gelişmiş özellikler için VSIX biçimi. Üzerinde teslim etmek için bir [low Impact yükleme](https://devblogs.microsoft.com/visualstudio/anatomy-of-a-low-impact-visual-studio-install) yan yana yüklemeleri de destekleyen Visual Studio, biz artık çoğu yapılandırma verileri, sistem kayıt defterine kaydetmek ve Visual Studio özel derlemeler GAC dışına taşındı. Biz de VSIX yükleme altyapısı ve VSIX biçimi yeteneklerini bazı yükleme türleri, uzantıları yüklemek için bunun yerine bir MSI veya EXE kullanmanıza olanak sağlayan artırdık.

Yeni özellikler şunları içerir:

* Belirtilen Visual Studio örneğinin içinde kayıt.
* Yükleme dışında [uzantıları klasörüne](set-install-root.md).
* İşlemci mimarisi algılanması.
* Dil Ayrılmış dil paketlerini bağımlılığa.
* Yükleme işlemine [NGEN desteği](ngen-support.md).

## <a name="build-an-extension-for-visual-studio-2017"></a>Bir uzantıyı Visual Studio 2017 için derleme

Tasarımcı yeni yazma araçları VSIX v3 bildirim biçimi Visual Studio 2017'de kullanılabilir. Eşlik eden belgesine bakın [nasıl yapılır: Genişletilebilirlik projeleri Visual Studio 2017'ye geçirme](how-to-migrate-extensibility-projects-to-visual-studio-2017.md) Tasarımcı araçlarını kullanarak veya projeye el ile güncelleştirmeler yapma hakkında bilgi ve VSIX v3 uzantılar geliştirmek için bildirimi.

## <a name="change-visual-studio-user-data-path"></a>Değiştir: Visual Studio kullanıcı veri yolu

Daha önce Visual Studio'nun her ana sürümüne tek bir yükleme, her bir makinede var olabilir. Visual Studio 2017'in yan yana yüklemeleri desteklemek için Visual Studio için birden çok kullanıcı veri yollarını kullanıcının makinesinde mevcut olmayabilir.

Visual Studio işlemi içinde çalışan kod, Visual Studio ayarları Yöneticisi'ni güncelleştirilmelidir. Visual Studio işlemin dışında çalışan kod, belirli bir Visual Studio yüklemesini kullanıcı yolunu bulabilirsiniz [Buradaki yönergeleri izleyerek](locating-visual-studio.md).

## <a name="change-global-assembly-cache-gac"></a>Değiştir: Genel Derleme Önbelleği (GAC)

Çoğu Visual Studio çekirdek derlemeler GAC içine artık yüklenir. Visual Studio işlemde çalışan kod hala gerekli derlemeleri çalışma zamanında bulabilmesi için aşağıdaki değişiklikler yapılmıştır.

> [!NOTE]
> [INSTALLDİR] Visual Studio yükleme kök dizini aşağıda gösterir. *VSIXInstaller.exe* Otomatik Doldur ancak özel dağıtım kod yazmak için lütfen okuma [Visual Studio'yu bulma](locating-visual-studio.md).

* Yalnızca GAC içine yüklenen derlemeler:

   Bu derlemeleri artık altında yüklü <em>[INSTALLDIR] \Common7\IDE\*, * [INSTALLDIR] \Common7\IDE\PublicAssemblies</em> veya *[INSTALLDIR] \Common7\IDE\PrivateAssemblies*. Bu klasör, Visual Studio işlemin algılama yolları bir parçasıdır.

* Yoklama olmayan bir yol ve GAC'ye yüklenmiş derlemeleri:

   * GAC içindeki kopyalama Kurulum'dan kaldırıldı.
   * A *.pkgdef* dosyası, derleme için bir kod temel giriş belirtmek için eklenmiştir.

      Örneğin:

      ```xml
      [$RootKey$\RuntimeConfiguration\dependentAssembly\codeBase\{UniqueGUID}]
      "name"="AssemblyName" "codeBase"="$PackageFolder$\AssemblyName.dll"
      "publicKeyToken"="Public Key Token"
      "culture"="neutral"
      "version"=15.0.0.0
      ```

      Çalışma zamanında, Visual Studio pkgdef alt bu girişleri Visual Studio işlemin çalışma zamanı yapılandırma dosyasına birleştirir. (altında *[VSAPPDATA]\devenv.exe.config*) olarak [ `<codeBase>` ](/dotnet/framework/configure-apps/file-schema/runtime/codebase-element) öğeleri. Arama yolları yoklama aracılığıyla önlediği için derleme bulunamadı Visual Studio işlemini izin vermek için önerilen yöntem budur.

### <a name="reacting-to-this-breaking-change"></a>Bu bozucu bir değişiklik tepki verme

* Visual Studio işlemi içinde uzantınızın çalışıyorsa:

   * Kodunuzu Visual Studio çekirdek derlemeleri bulmak mümkün olacaktır.
   * Kullanmayı bir *.pkgdef* gerekirse derlemelerinizin bir yol belirtmek için dosya.

* Visual Studio işlemi dışında uzantınızı çalışıyorsa:

   Visual Studio çekirdek derlemeler aranıyor göz önünde bulundurun <em>[INSTALLDIR] \Common7\IDE\*, * [INSTALLDIR] \Common7\IDE\PublicAssemblies</em> veya *[INSTALLDIR] \Common7\IDE\PrivateAssemblies*yapılandırma dosyası veya bütünleştirilmiş kod çözücü kullanma.

## <a name="change-reduce-registry-impact"></a>Değiştir: Kayıt defteri etkiyi azaltmak

### <a name="global-com-registration"></a>Genel bir COM kayıt

* Daha önce Visual Studio, birçok kayıt defteri anahtarlarını yerel COM kaydını desteklemek için HKEY_CLASSES_ROOT ve HKEY_LOCAL_MACHINE yığınlar yüklü. Bu etkiyi ortadan kaldırmak için Visual Studio artık kullanır [kayıtsız etkinleştirme için COM bileşenlerini](https://msdn.microsoft.com/library/ms973913.aspx).
* Sonuç olarak, çoğu TLB / OLB / DLL dosyaları % ProgramFiles (x86) %\Common Files\Microsoft Shared\MSEnv altında artık Visual Studio tarafından varsayılan olarak yüklenir. Bu dosyalar Visual Studio ana bilgisayar işlemi tarafından kullanılan karşılık gelen Registration-Free COM bildirimleri ile [INSTALLDIR] altında artık yüklüdür.
* Sonuç olarak, Visual Studio COM arabirimleri için genel bir COM kayıt dayanan dış kod artık bu kayıtları bulur. Visual Studio işlemi içinde çalışan kod, bir fark görmezsiniz.

### <a name="visual-studio-registry"></a>Visual Studio kayıt defteri

* Daha önce Visual Studio sisteme ait çok sayıda kayıt defteri anahtarlarını yüklü **HKEY_LOCAL_MACHINE** ve **HKEY_CURRENT_USER** yığınlarını Visual Studio özel anahtarı altında:

  * **HKLM\Software\Microsoft\VisualStudio\{sürüm}**: MSI yükleyiciler ve makine başına uzantılar tarafından oluşturulan kayıt defteri anahtarları.
  * **HKCU\Software\Microsoft\VisualStudio\{sürüm}**: Kullanıcıya özel ayarları depolamak için Visual Studio tarafından oluşturulan kayıt defteri anahtarları.
  * **HKCU\Software\Microsoft\VisualStudio\{sürüm} _Config**: Visual Studio HKLM anahtar yukarıdaki yanı sıra, kayıt defteri anahtarlarını bir kopyasını birleştirme kaynağı *.pkgdef* uzantıları dosyaları.

* Kayıt defteri üzerindeki etkiyi azaltmak için Visual Studio artık kullanır [RegLoadAppKey](/windows/desktop/api/winreg/nf-winreg-regloadappkeya) kayıt defteri anahtarları altında özel ikili dosyaları depolamak için işlev *[VSAPPDATA]\privateregistry.bin*. Visual Studio özel anahtarlar yalnızca çok az sayıda sistem kayıt defterinde kalır.
* Visual Studio işlemi içinde çalışan mevcut kod etkilenmez. Visual Studio, özel kayıt defterine HKCU Visual Studio özel anahtarı altındaki tüm kayıt defteri işlemlerini yönlendirir. Diğer kayıt defteri konumlara yazma ve okuma sistem kayıt defterine kullanmaya devam eder.
* Dış kod yükleme ve bu dosyayı Visual Studio kayıt defteri girişleri için okuma gerekecektir.

### <a name="react-to-this-breaking-change"></a>Bu bozucu bir değişiklik tepki

* Kayıtsız etkinleştirme için COM bileşenlerini de kullanmak için dış kod dönüştürülmesi.
* Dış bileşenler, Visual Studio konumu bulabilir [Buradaki yönergeleri izleyerek](https://devblogs.microsoft.com/setup/changes-to-visual-studio-15-setup).
* Dış bileşenler kullanmanızı öneririz [dış ayarları Yöneticisi](/dotnet/api/microsoft.visualstudio.settings.externalsettingsmanager) yerine doğrudan Visual Studio kayıt defteri anahtarları için okuma/yazma.
* Uzantınızı kullanarak bileşenlerini kaydı için başka bir teknik uyguladınız mı denetleyin. Örneğin, hata ayıklayıcı uzantılarını yeni yararlanmak çözebileceğiniz [msvsmon JSON dosyası COM kayıt](migrate-debugger-COM-registration.md).

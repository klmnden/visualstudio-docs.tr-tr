---
title: C# Proje özelliklerinin uygulama sayfası
ms.date: 10/30/2018
ms.topic: reference
f1_keywords:
- cs.ProjectPropertiesApplicationWPF
- cs.ProjectPropertiesApplication
helpviewer_keywords:
- Project Designer, Application page
- Application page in Project Designer
author: gewarren
ms.author: gewarren
manager: jillfra
ms.workload:
- dotnet
ms.openlocfilehash: 04a130528edbe8ab3aae0a24d69315b934b19d54
ms.sourcegitcommit: 209ed0fcbb8daa1685e8d6b9a97f3857a4ce1152
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/16/2019
ms.locfileid: "69551435"
---
# <a name="application-page-project-designer-c"></a>Uygulama Sayfası, Proje Tasarımcısı (C#)

Projenin uygulama ayarlarını ve özelliklerini belirtmek için **Proje Tasarımcısı** ' nın **uygulama** sayfasını kullanın.

**Uygulama** sayfasına erişmek için **Çözüm Gezgini**' de bir proje düğümü ( **çözüm** düğümünü değil) seçin. Ardından, menü çubuğunda **Proje** > **özellikleri** ' ni seçin. **Proje Tasarımcısı** göründüğünde **uygulama** sekmesine tıklayın.

[!INCLUDE[note_settings_general](../../data-tools/includes/note_settings_general_md.md)]

## <a name="general-application-settings"></a>Genel uygulama ayarları

Aşağıdaki seçenekler, uygulamanın genel ayarlarını yapılandırmanızı sağlar.

**Bütünleştirilmiş kod adı**

Derleme bildirimini tutacak çıkış dosyasının adını belirtir. Bu özelliğin değiştirilmesi, **Çıkış adı** özelliğini de değiştirir.

Ayrıca, [/Out (C# derleyici seçenekleri)](/dotnet/csharp/language-reference/compiler-options/out-compiler-option)kullanarak komut satırından da bu değişikliği yapabilirsiniz.

Programlı olarak bu özelliğe erişmek için bkz <xref:VSLangProj.ProjectProperties.AssemblyName%2A>.

**Varsayılan ad alanı**

Projeye eklenen dosyalar için temel ad alanını belirtir.

Kodunuzda ad alanları oluşturma hakkında daha fazla bilgi için bkz. [ad alanı](/dotnet/csharp/language-reference/keywords/namespace) .

Programlı olarak bu özelliğe erişmek için bkz <xref:VSLangProj.ProjectProperties.RootNamespace%2A>.

**Hedef Çerçeve**

Uygulamanın hedeflediği .NET sürümünü belirtir. Bu seçenek, bilgisayarınızda hangi .NET sürümlerinin yüklü olduğuna bağlı olarak farklı değerlere sahip olabilir.

.NET Framework projeleri için, varsayılan değer projeyi oluştururken belirttiğiniz hedef Framework ile eşleşir.

.NET Core 'u hedefleyen bir proje için, kullanılabilir sürümler şu şekilde görünebilir:

![.NET Core projesi için hedef çerçeve sürümleri](../media/application-target-framework.png)

> [!NOTE]
> [Önkoşullar Iletişim kutusunda](../../ide/reference/prerequisites-dialog-box.md) listelenen önkoşul paketleri, iletişim kutusunu ilk açışınızda otomatik olarak ayarlanır. Projenin hedef çerçevesini daha sonra değiştirirseniz, yeni hedef Framework 'ü eşleştirmek için önkoşulları el ile seçmeniz gerekir.

Daha fazla bilgi için bkz. [Çerçeve hedefleme genel bakış](../../ide/visual-studio-multi-targeting-overview.md).

**Çıkış türü**

Oluşturulacak uygulamanın türünü belirtir. Değerler proje türüne göre farklılık açmış. Örneğin, bir **konsol uygulaması** projesi için, çıkış türü olarak **Windows uygulaması**, **konsol uygulaması**veya **sınıf kitaplığı** belirtebilirsiniz.

Bir Web uygulaması projesi için **sınıf kitaplığı**belirtmeniz gerekir.

**Çıktı türü** özelliği hakkında daha fazla bilgi için bkz. [/target (C# derleyici seçenekleri)](/dotnet/csharp/language-reference/compiler-options/target-compiler-option).

Bu özelliğe programlı bir şekilde erişme hakkında daha fazla bilgi için <xref:VSLangProj.ProjectProperties.OutputType%2A>bkz.

**Bağlama yeniden yönlendirmelerini otomatik oluştur**

Uygulamanız veya bileşenleri aynı derlemenin birden fazla sürümüne başvurduğu takdirde bağlama yeniden yönlendirmeleri projenize eklenir. Proje dosyasında bağlama yeniden yönlendirmelerini el ile tanımlamak istiyorsanız **bağlama yeniden yönlendirmelerini otomatik oluştur**seçimini kaldırın.

Yeniden yönlendirme hakkında daha fazla bilgi için bkz. [derleme sürümlerini yeniden yönlendirme](/dotnet/framework/configure-apps/redirect-assembly-versions).

**Başlangıç nesnesi**

Uygulama yüklenirken çağrılacak giriş noktasını tanımlar. Genellikle bu, uygulamanızdaki ana forma veya `Main` uygulama başladığında çalışması gereken yordama ayarlanır. Sınıf kitaplıklarının bir giriş noktası olmadığından, bu özellik için yalnızca seçeneği **(ayarlanmamış)** olur.

Varsayılan olarak, bir WPF uygulama projesinde, bu seçenek **(ayarlanmamış)** olarak ayarlanır. Diğer seçenek ProjectName] \[. App ' dir. Bir WPF projesinde, uygulama başladığında bir UI kaynağı yüklemek için başlangıç URI 'sini ayarlamanız gerekir. Bunu yapmak için, projenizdeki *Application. xaml* dosyasını açın ve `StartupUri` özelliğini projenizdeki *. xaml* dosyasına (örneğin, *Window1. xaml*) ayarlayın. Kabul edilebilir kök öğelerinin bir listesi için bkz <xref:System.Windows.Application.StartupUri%2A>. Ayrıca, projedeki bir sınıfta `public static void Main()` bir yöntemi tanımlamanız gerekir. Bu sınıf, **Başlangıç nesnesi** listesinde *ProjectName. ClassName*olarak görünür. Ardından, başlangıç nesnesi olarak sınıfını seçebilirsiniz.

Daha fazla bilgi için bkz. [/Main (C# derleyici seçenekleri)](/dotnet/csharp/language-reference/compiler-options/main-compiler-option) . Programlı olarak bu özelliğe erişmek için bkz <xref:VSLangProj.ProjectProperties.StartupObject%2A>.

**Derleme bilgileri**

Bu düğme, [derleme bilgileri](../../ide/reference/assembly-information-dialog-box.md) iletişim kutusunu açar.

## <a name="resources"></a>Kaynaklar

Kaynak seçenekleri, uygulamanız için kaynak ayarlarını yapılandırmanıza yardımcı olur.

**Simge ve bildirim**

Varsayılan olarak, bu radyo düğmesi seçilidir ve **simge** ve **bildirim** seçenekleri etkindir. Bu, kendi simgenizi seçmenizi veya farklı bildirim oluşturma seçeneklerini seçmenizi sağlar. Proje için bir kaynak dosyası sağlamadığınız takdirde bu radyo düğmesini seçili bırakın.

**Simg**

Program simgenizin olarak kullanmak istediğiniz *. ico* dosyasını ayarlar. Var olan bir grafiğe gitmek için, **Araştır** ' a tıklayın veya istediğiniz dosyanın adını yazın. Daha fazla bilgi için bkz. [/Win32Icon (C# derleyici seçenekleri)](/dotnet/csharp/language-reference/compiler-options/win32icon-compiler-option) .

Programlı olarak bu özelliğe erişmek için bkz <xref:VSLangProj.ProjectProperties.ApplicationIcon%2A>.

Simge oluşturma hakkında daha fazla bilgi için bkz. [simgeler Için görüntü düzenleyici](/cpp/windows/image-editor-for-icons).

**Bildirimi**

Uygulama Windows Vista 'da Kullanıcı hesabı denetimi (UAC) altında çalışırken bir bildirim oluşturma seçeneği belirler. Bu seçenek aşağıdaki değerlere sahip olabilir:

- **Bildirimi varsayılan ayarlarla ekleyin**. , Uygulamanın yürütülebilir dosyasında güvenlik bilgilerini eklemek ve bunu belirtmek `requestedExecutionLevel` `AsInvoker`için olan Windows Vista 'da Visual Studio 'nun çalıştığı tipik şekilde desteklenir. Bu varsayılan seçenektir.

- **Bildirim olmadan uygulama oluşturun**. Bu yöntem *sanallaştırma*olarak bilinir. Önceki uygulamalarla uyumluluk için bu seçeneği kullanın.

- **Properties\app.manifest**. Bu seçenek, ClickOnce veya kayıtsız COM tarafından dağıtılan uygulamalar için gereklidir. ClickOnce dağıtımını kullanarak bir uygulamayı yayımlarsanız, **bildirim** otomatik olarak bu seçeneğe ayarlanır.

**Kaynak dosyası**

Proje için bir kaynak dosyası sağlıyorsanız bu radyo düğmesini seçin. Bu seçenek belirlendiğinde, **simge** ve **bildirim** seçenekleri devre dışı bırakılır.

Bir yol adı girin veya projeye bir Win32 kaynak dosyası eklemek için ( **...** ) düğmesini kullanın.

Daha fazla bilgi için bkz. [.NET uygulamaları için kaynak dosyaları oluşturma](/dotnet/framework/resources/creating-resource-files-for-desktop-apps).

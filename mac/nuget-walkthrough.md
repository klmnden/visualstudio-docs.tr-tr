---
title: Projenize bir NuGet paketi dahil etme
description: Bu belge, Mac için Visual Studio kullanarak bir projeye NuGet paketinin nasıl ekleneceğini kapsar. Bir paketi bulmayı ve indirmeyi, Ayrıca IDE tümleştirme özelliklerini tanıtmayı da açıklar.
author: jmatthiesen
ms.author: jomatthi
ms.date: 09/18/2019
ms.assetid: 5C800815-0B13-4B27-B017-95FCEF1A0EA2
ms.custom: conceptual
ms.openlocfilehash: 55b4691a7adb03d4ee8fd5e05e7bd9d7daa28f13
ms.sourcegitcommit: ea182703e922c74725045afc251bcebac305068a
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/24/2019
ms.locfileid: "71213694"
---
# <a name="install-and-manage-nuget-packages-in-visual-studio-for-mac"></a>Mac için Visual Studio NuGet paketlerini yükleyip yönetme

Mac için Visual Studio 'daki NuGet Paket Yöneticisi Kullanıcı arabirimi, projelerde ve çözümlerde NuGet paketlerini kolayca yüklemenize, kaldırmanıza ve güncelleştirmenize olanak tanır. Paketleri arayıp .NET Core, ASP.NET Core ve Xamarin projelerinize ekleyebilirsiniz.

Bu makalede, bir projeye NuGet paketinin nasıl dahil edileceğini ve işlemin sorunsuz hale getiren araç zincirini nasıl gösterdiği açıklanmaktadır.

Mac için Visual Studio 'de NuGet kullanma girişi için bkz [. hızlı başlangıç: Mac için Visual Studio bir paketi yükleyip kullanma](/nuget/quickstart/install-and-use-a-package-in-visual-studio-mac)

## <a name="find-and-install-a-package"></a>Paket bulma ve yüklemeyi

1. Mac için Visual Studio bir proje açıkken, **çözüm bölmesi** **Bağımlılıklar** klasörüne (Xamarin projesi kullanılıyorsa**paketler** klasörü) sağ tıklayın ve **NuGet Paketlerini Yönet..** . seçeneğini belirleyin.

    ![Yeni NuGet paketi bağlam eylemi Ekle](media/nuget-walkthrough-packages-menu.png)

2. Bu, **NuGet Paketlerini Yönet** penceresi başlatılır. İletişim kutusunun sol üst köşesindeki kaynak açılan kutusunun olarak `nuget.org`ayarlandığından emin olun.

    ![NuGet paketlerini listeleme](media/nuget-walkthrough-add-packages1.png)

3. Belirli bir paketi bulmak için sağ üst köşedeki arama kutusunu kullanın (örneğin `EntityFramework`,). Kullanmak istediğiniz bir paket bulduğunuz zaman, yüklemeyi başlatmak için paketi seçin ve **paket Ekle** düğmesine tıklayın.

    ![EntityFramework NuGet paketi Ekle](media/nuget-walkthrough-add-packages2.png)

4. Paket indirildikten sonra projenize eklenir. Bu çözüm, düzenlemekte olduğunuz projenin türüne bağlı olarak değişir:

    **Xamarin projeleri**
    * **Başvurular** düğümü, bir NuGet paketinin parçası olan tüm derlemelerin bir listesini içerir.
    * **Paketler** düğümü, Indirdiğiniz her NuGet paketini görüntüler. Bu listeden bir paketi güncelleştirebilir veya kaldırabilirsiniz.
    
    **.NET Core projeleri**

    * **NuGet düğümü > bağımlılıklar** , Indirdiğiniz her NuGet paketini görüntüler. Bu listeden bir paketi güncelleştirebilir veya kaldırabilirsiniz.

## <a name="using-nuget-packages"></a>NuGet paketlerini kullanma

NuGet paketi eklendikten ve proje güncelleştirildikten sonra, herhangi bir proje başvurusunda yaptığınız gibi API 'Lerle programlama yapabilirsiniz.

Dosyanızın en üstüne gerekli `using` yönergeleri eklemediğinizden emin olun:

```csharp
using Newtonsoft.Json;
```

<a name="Package_Updates" class="injected"></a>

## <a name="updating-packages"></a>Paketler güncelleştiriliyor

Paket güncelleştirmeleri, **Bağımlılıklar** düğümüne sağ tıklanarak (Xamarin projeleri için**paketler** düğümü) veya her bir pakette ayrı ayrı tek bir şekilde yapılabilir. NuGet paketinin yeni bir sürümü kullanılabilir olduğunda, bir güncelleştirme simgesi, daireyle ![](media/nuget-walkthrough-update-icon.png)birlikte görüntülenir.

Bağlam menüsüne erişmek için **Bağımlılıklar** ' a sağ tıklayın ve tüm paketleri güncelleştirmek için **Güncelleştir** ' i seçin:

![Paketler menüsü](media/nuget-walkthrough-packages-menu-update.png)

* **NuGet Paketlerini Yönet** -projeye daha fazla paket eklemek için pencereyi açar.
* **Güncelleştir** -kaynak sunucuyu her bir paket için denetler ve daha yeni sürümleri indirir.
* **Restore** -eksik paketleri indirir (var olan paketleri yeni sürümlere güncelleştirmeden önce).

Güncelleştirme ve geri yükleme seçenekleri de çözüm düzeyinde bulunur ve Çözümdeki tüm projeleri etkiler.

Çözüm panelinden, bir paketin hangi sürümünün yüklü olduğunu görüntüleyebilir ve güncelleştirilecek pakete sağ tıklamakta tıklayabilirsiniz.

![Güncelleştirme, kaldırma, yenileme seçeneklerini içeren paketler menüsü](media/nuget-walkthrough-PackageMenu.png)

Ayrıca, paketin yeni bir sürümü kullanılabilir olduğunda paket adının yanında bir bildirim görürsünüz. bu sayede, güncelleştirmeyi güncelleştirmek isteyebilir karar verebilirsiniz.

![Yeni bir paket sürümü kullanılabilir olduğunda bildirim gösteriliyor](media/nuget-walkthrough-package-update-available.png)

Gösterilen menüde iki seçeneğiniz vardır:

* **Güncelleştir** -kaynak sunucuyu denetler ve daha yeni bir sürümü indirir (varsa).
* **Remove** -paketi bu projeden kaldırır ve ilgili derlemeleri projenin başvurularından kaldırır.

## <a name="adding-package-sources"></a>Paket kaynakları ekleniyor

Yükleme için kullanılabilen paketler başlangıçta nuget.org adresinden alınır. Bununla birlikte, Mac için Visual Studio başka paket konumları da ekleyebilirsiniz. Bu, geliştirme aşamasındaki kendi NuGet paketlerinizi test etmek veya şirketinizin veya kuruluşunuzun içinde özel bir NuGet sunucusu kullanmak için yararlı olabilir.

Mac için Visual Studio, paket kaynakları listesini görüntülemek ve düzenlemek için **Visual Studio > tercihler > NuGet > kaynakları** ' na gidin. Kaynakların uzak bir sunucu (bir URL ile belirtilir) veya yerel bir dizin olabileceğini unutmayın.

![Paket kaynakları](media/nuget-walkthrough-PackageSource.png)

Yeni bir kaynak kurmak için **Ekle** ' ye tıklayın. Paket kaynağına kolay bir ad ve URL (ya da dosya yolu) girin. Kaynak güvenli bir Web sunucusu ise, Kullanıcı adını ve parolayı da girin, aksi takdirde bu girdileri boş bırakın:

![Paket kaynakları ekle](media/nuget-walkthrough-PackageSource2.png)

Paketler aranırken farklı kaynaklar seçilebilir:

![Paket kaynakları ekle](media/nuget-walkthrough-PackageSource3.png)

## <a name="version-control"></a>Sürüm Denetimi

NuGet belgeleri, [kaynak denetimine paket Işlemeden NuGet kullanarak](/nuget/consume-packages/packages-and-source-control)açıklanır. İkili dosyaları ve kullanılmayan bilgileri kaynak denetiminde depolamamayı tercih ediyorsanız, paketleri sunucudan otomatik olarak geri yüklemek için Mac için Visual Studio yapılandırabilirsiniz. Bu, bir geliştirici projeyi kaynak denetiminden ilk kez aldığında Mac için Visual Studio gerekli paketleri otomatik olarak indirecek ve yükleymeyeceği anlamına gelir.

![Paketleri otomatik olarak geri yükle](media/nuget-walkthrough-AutoRestore.png)

Dizinin izlenmesini nasıl dışlayacak hakkında daha fazla bilgi için, `packages` belirli kaynak denetimi belgelerinize bakın.

## <a name="related-video"></a>İlgili video

> [!Video https://channel9.msdn.com/Shows/Visual-Studio-Toolbox/Visual-Studio-for-Mac-Using-NuGet/player]

## <a name="see-also"></a>Ayrıca bkz.

* [Visual Studio 'da bir paketi (Windows 'da) yükleyip kullanma](/nuget/quickstart/install-and-use-a-package-in-visual-studio)

---
title: Projeler ve çözümler oluşturma
ms.date: 02/06/2018
ms.topic: conceptual
f1_keywords:
- vs.openprojectfromweb
- VS.ToolsOptionsPages.Projects.General
- SolutionItemsProject
helpviewer_keywords:
- solutions [Visual Studio], creating
- projects [Visual Studio], creating
author: gewarren
ms.author: gewarren
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: f6f6bd03a47500c127360afd2d2a6ae6b62ee2e5
ms.sourcegitcommit: 5af29226aef0a3b4a506b69a08a97cfd21049521
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/20/2019
ms.locfileid: "58268567"
---
# <a name="create-solutions-and-projects"></a>Projeler ve çözümler oluşturma

*Projeleri* kaynak kodu dosyaları, bit eşlemler, simgeler gibi Visual Studio'da, uygulamanızı oluşturmak için gereken öğeleri ve bileşen ve hizmet başvuruları tutun. Yeni bir proje oluşturduğunuzda, Visual Studio oluşturur bir *çözüm* proje içerecek. İsterseniz, diğer yeni veya mevcut projeleri çözüme sonra ekleyebilirsiniz. Çözümleri Ayrıca belirli hiçbir projeye bağlı olmayan dosyalar içerebilir.

![Çözüm/proje hiyerarşisi](./media/vside-proj-soln.png)

> [!NOTE]
> Bu konu, Windows üzerinde Visual Studio için geçerlidir. Mac için Visual Studio için bkz: [oluşturma projeleri Visual Studio'da Mac için](/visualstudio/mac/create-new-projects).

Projeler ve çözümler adlı bir araç penceresinde görüntüleyebilirsiniz **Çözüm Gezgini**. Bir örnek çözümde aşağıdaki ekran görüntüsünde gösterilmektedir **Çözüm Gezgini** (**BikeSharing.Xamarin UWP**), iki proje içerir: **BikeSharing.Clients.Core** ve **BikeSharing.Clients.Windows**. Her proje birden fazla dosyaları, klasörleri ve başvurular içerir. Proje adı kalın *başlangıç projesi*; diğer bir deyişle, uygulamayı çalıştırdığınızda başlatan proje. Projeyi başlangıç projesi olduğunu belirtebilirsiniz.

![Çözüm Gezgini projeleri](./media/vside-solution-explorer-projects.png)

Gerekli dosyaları ekleyerek kendiniz bir proje oluşturabilirsiniz, ancak Visual Studio size avantajlı bir başlangıç projesi şablonlar sunar. Bir şablondan yeni bir proje oluşturma, şu temel bir proje bu proje türü için sunar ve dosyaları yeniden adlandırmak veya yeni veya mevcut koda ve diğer kaynakları gerektiği gibi ekleyin.

Başka bir deyişle, çözümler ve projeler Visual Studio'da uygulamaları geliştirmek için gerekli değildir. Git'ten kopyaladığınız veya başka bir yerde indirilen kod yalnızca açabilirsiniz. Daha fazla bilgi için [kod Visual Studio'da projeler veya çözümler olmadan geliştirme](../ide/develop-code-in-visual-studio-without-projects-or-solutions.md).

## <a name="create-a-project-from-a-project-template"></a>Bir proje şablonundan bir proje oluşturun

Bir şablondan yeni bir proje oluşturma hakkında daha fazla bilgi için bkz: [Visual Studio'da yeni proje oluşturma](create-new-project.md).

## <a name="create-a-project-from-existing-code-files"></a>Varolan kod dosyalarından proje oluşturma

Bir kod kaynak dosyaları koleksiyonunu varsa, bunları projeye bir kolayca ekleyebilirsiniz.

1. Menüsünde **dosya** > **yeni** > **varolan koddan proje**.

1. İçinde **varolan kod dosyalarından proje oluşturma** Sihirbazı, istediğiniz proje türünü seçin **ne tür bir proje oluşturmak istersiniz?** aşağı açılan liste kutusunu ve ardından **İleri**  düğmesi.

1. Sihirbazı'nda, dosyaların konumuna göz atın ve ardından yeni proje için bir ad girin **adı** kutusu. İşiniz bittiğinde seçin **son** düğmesi.

> [!NOTE]
> Bu seçenek, dosyaları görece basit koleksiyonu en iyi şekilde çalışır. Şu anda yalnızca Visual C++, Apache Cordova, Visual Basic ve C# proje türleri desteklenir.

## <a name="add-files-to-a-solution"></a>Çözüme dosyaları ekleme

Çözüm için bir benioku dosyası gibi birden çok proje için geçerli bir dosya veya belirli bir proje altında daha sonra bunları çözüme ekleyebilirsiniz yerine mantıksal olarak çözüm düzeyinde ait diğer dosyaları varsa. Çözüm düğümünün (sağ tıklama) bağlam menüsünde bir çözüme bir öğe eklemek için **Çözüm Gezgini**, seçin **Ekle** > **yeni öğe**, veya **Ekleme** > **var olan öğe**.

## <a name="create-a-net-project-that-targets-a-specific-version-of-the-net-framework"></a>Belirli bir .NET Framework sürümünü hedefleyen bir .NET projesi oluşturma

Bir proje oluşturduğunuzda, projeyi kullanacak şekilde istediğiniz .NET Framework'ün belirli bir sürümünü belirtebilirsiniz.

::: moniker range="vs-2017"

Bir .NET framework sürümünü belirtmek için **Framework** açılan menüde **yeni proje** iletişim kutusu.

![Framework açılan yeni proje iletişim kutusunda](./media/vside-newproject-framework.png)

> [!NOTE]
> .NET Framework sürümlerini .NET Framework 4'den önceki erişmek için .NET Framework 3.5 yüklü olmalıdır.

::: moniker-end

::: moniker range=">=vs-2019"

Bir .NET framework sürümünü belirtmek için **Framework** açılan menüsünde **yeni bir proje oluşturma** sayfası.

![Framework seçicide yeni proje yapılandırma](media/vs-2019/configure-new-project-framework.png)

::: moniker-end

## <a name="create-empty-solutions"></a>Boş Çözüm oluşturma

Projeleri olmayan boş çözümleri oluşturabilirsiniz. Bu durumda, çözümünüzü ve projelerinizi sıfırdan oluşturmak için istediğiniz tercih edilebilir.

### <a name="to-create-an-empty-solution"></a>Boş bir çözüm oluşturmak için

1. Menü çubuğunda, **dosya** > **yeni** > **proje**.

::: moniker range="vs-2017"

2. Sol (**şablonları**) bölmesinde seçin **diğer proje türleri** > **Visual Studio çözümleri** genişletilmiş listeden.

3. Orta bölmede seçin **boş çözüm**.

4. Girin **adı** ve **konumu** çözümünüz için değerleri ve ardından **Tamam**.

::: moniker-end

::: moniker range=">=vs-2019"

2. Üzerinde **yeni bir proje oluşturma** sayfasında **çözüm** kartındaki arama kutusuna.

3. Seçin **boş çözüm** şablonu ve ardından **sonraki**.

4. Girin **adı** ve **konumu** çözümünüz için değerleri ve ardından **Oluştur**.

::: moniker-end

Boş bir çözüm oluşturduğunuzda, yeni veya var olan proje veya öğe için seçerek ekleyebileceğiniz **Yeni Öğe Ekle** veya **varolan öğeyi Ekle** üzerinde **proje** menüsü.

Daha önce bahsedildiği gibi bir proje veya çözüm gerek kalmadan kod dosyaları da açabilirsiniz. Bu şekilde kod geliştirme hakkında bilgi edinmek için [kod Visual Studio'da projeler veya çözümler olmadan geliştirme](../ide/develop-code-in-visual-studio-without-projects-or-solutions.md).

::: moniker range="vs-2017"

## <a name="create-a-temporary-project"></a>Geçici bir proje oluşturun

(C# ve yalnızca Visual Basic)

Oluşturursanız, bir. AĞ tabanlı proje bir disk konumu belirtmeden geçici bir proje olan. Geçici projeler .NET projeleriyle denemeler olanak sağlar. Geçici bir projeyle çalışırken herhangi bir zamanda kaydetmek veya atmak seçebilirsiniz.

Geçici bir proje oluşturmak için ilk Git **Araçları** > **seçenekleri** > **projeler ve çözümler**  >   **Genel**, kaldırın **oluşturulduğunda yeni projeleri Kaydet** onay kutusu. Açılacağını **yeni proje** iletişim kutusunda her zaman olduğu gibi.

::: moniker-end

## <a name="delete-a-solution-project-or-item"></a>Çözüm, proje veya öğe silme

Çözümler ve bunların içeriğini kalıcı olarak silebilirsiniz ancak Visual Studio IDE kullanarak değil. Visual Studio içindeki öğeleri silme yalnızca bunları geçerli çözüm veya proje kaldırır. Bir çözüm ya da başka bir bileşen sisteminizden kalıcı olarak silmek için içeren klasörü silmek için dosya Gezgini'ni kullanın *.sln* ve *.suo* çözüm dosyaları. Ancak, bir çözüm kalıcı olarak silinmeden önce yeniden gerektiği durumlarda tüm projeleri veya dosyaları yedekleme önerilir.

> [!NOTE]
> *.Suo* varsayılan dosya Gezgini Ayarları altında görüntülenmez gizli bir dosya dosyasıdır. Gizli dosyaları göstermek için **görünümü** dosya Gezgini'nde, seçim menüsünde **gizli öğeleri** onay kutusu.

### <a name="permanently-delete-a-solution"></a>Bir çözümü kalıcı olarak sil

1. İçinde **Çözüm Gezgini**, sağ tıklama menüsünde silmek istediğiniz çözüm (bağlam menüsü), **klasörü dosya Gezgini'nde Aç**.

1. Dosya Gezgini'nde, bir düzey yukarı gidin.

1. Çözümü içeren klasörü seçin ve sonra basın **Sil** anahtarı.

## <a name="see-also"></a>Ayrıca bkz.

- [Projeler ve çözümler](../ide/solutions-and-projects-in-visual-studio.md)
- [Github'da Microsoft'un açık kaynak depolar](https://github.com/Microsoft)
- [Geliştirici kodu örnekleri](https://code.msdn.microsoft.com/)
- [Projeleri (Mac için Visual Studio) oluşturma](/visualstudio/mac/create-new-projects)
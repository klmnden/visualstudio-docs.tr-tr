---
title: Yeni bir proje oluşturma
ms.date: 03/19/2019
ms.topic: conceptual
f1_keywords:
- vs.newproject
helpviewer_keywords:
- projects [Visual Studio], creating
author: gewarren
ms.author: gewarren
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 9f5d48ee97e1e0d92237fe5836c8bd9c1888c3a4
ms.sourcegitcommit: 3201da3499051768ab59f492699a9049cbc5c3c6
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/22/2019
ms.locfileid: "58355253"
---
# <a name="create-a-new-project-in-visual-studio"></a>Visual Studio'da yeni proje oluşturma

::: moniker range="vs-2017"

## <a name="open-the-new-project-dialog"></a>Yeni Proje iletişim kutusunu aç

Visual Studio 2017'de yeni bir proje oluşturmak için birden çok yolu vardır. Başlangıç sayfasında, bir proje şablonunda adını yazabilirsiniz **arama proje şablonları** kutusuna veya tercih **yeni proje oluştur** açmak için bağlantıyı **yeni proje** iletişim bir kutu. Başlangıç sayfası tarafından da seçebilirsiniz **dosya** > **yeni** > **proje** tıklayın ya da menü çubuğu üzerinde **yeni proje**  araç çubuğunda.

![Başlangıç sayfası ve Dosya > Yeni > Proje](./media/vside-newproject1.png)

## <a name="select-a-template-type"></a>Şablon türünü seçin

İçinde **yeni proje** iletişim kutusu, kullanılabilir proje şablonları görünür altında bir listede **şablonları** kategorisi. Şablonları Visual gibi dil ve proje türü programlama tarafından düzenlenir C#, JavaScript ve Azure Data Lake.

![Yeni Proje iletişim kutusu](./media/vside-newproject-templates-list.png)

> [!NOTE]
> Görüntülenen listeden kullanılabilir diller ve proje şablonları, kullanmakta olduğunuz Visual Studio ve yüklü iş yükleri sürümüne bağlıdır. Ek iş yüklerinin yükleme hakkında bilgi edinmek için [iş yükleri ve bileşenleri ekleyerek veya kaldırarak tarafından Visual Studio değiştirme](../install/modify-visual-studio.md).

Dil adının yanındaki üçgeni tıklayarak ve sonra bir proje kategorisi (örneğin, Windows Masaüstü) seçerek kullanmak istediğiniz programlama dili için şablonları listesini gösterir.

Kullanılabilir proje şablonları aşağıdaki resimde gösterilmektedir görsel için C# .NET Core projeleri:

![Proje şablonları](./media/new-project-dialog-net-core.png)

## <a name="configure-your-project"></a>Projenizi yapılandırın

Yeni proje için bir ad girin **adı** kutusu. Proje bilgisayar ya da'a tıklayın varsayılan konumda kaydedebilirsiniz **Gözat** başka bir konum bulmak için düğme. Ayrıca bir çözüm adı seçin veya yeni proje için Git deposu ekleme (seçerek **kaynak denetimine Ekle**).

Tıklayın **Tamam** proje ve çözüm oluşturmak için.

::: moniker-end

::: moniker range=">=vs-2019"

## <a name="open-the-create-a-new-project-page"></a>Yeni Proje sayfası oluşturma açın

Visual Studio 2019 içinde yeni bir proje oluşturmak için birden çok yolu vardır. Visual Studio'yu ilk kez açın, başlangıç penceresi görüntülenir ve burada, seçtiğiniz **yeni bir proje oluşturma**.

![VS 2019 ' Başlangıç penceresinden yeni bir proje oluşturun](media/vs-2019/start-window-create-new-project.png)

Visual Studio geliştirme ortamı zaten açıksa, seçerek yeni bir proje oluşturabilirsiniz **dosya** > **yeni** > **proje** üzerinde menü çubuğu veya tıklayarak **yeni proje** araç çubuğunda.

![Visual Studio 2019 içinde yeni proje düğmesi](media/vs-2019/new-project-button.png)

## <a name="select-a-template-type"></a>Şablon türünü seçin

Üzerinde **yeni bir proje oluşturma** sayfasında, sol tarafta, son seçilen şablonları listesi görüntülenir. Şablonları göre sıralanır *en son kullanılan*.

Son kullanılan şablonlardan seçeneğini belirliyoruz değil, tüm kullanılabilir proje şablonları tarafından filtreleyebilirsiniz **dil** (örneğin, C# veya C++), **Platform** (örneğin, Windows veya Azure) ve **Proje türü** (örneğin, masaüstü veya Web). Aranacak metin şablonları, örneğin, daha fazla filtrelemek için arama kutusuna girebilirsiniz **asp.net**.

![Visual Studio 2019 proje şablonu filtreleri](media/vs-2019/create-new-project-filters.png)

Her şablon altında görünen etiketlerin üç açılan filtreleri (dil, Platform ve proje türü) karşılık gelir.

> [!TIP]
> Aradığınız şablon görmüyorsanız, bir iş yükü için Visual Studio eksik olabilir. Ek yükleri yüklemek için **Azure geliştirme** veya **.NET ile Mobil Geliştirme**, tıklayın **daha fazla araçları ve özellikleri yükleme** görseli açmak için bağlantı Studio yükleyicisi. Buradan yükleyin ve ardından istediğiniz iş yüklerini seçin **Değiştir**. Bundan sonra ek proje şablonları arasından seçim kullanılabilir.
>
> ![Daha fazla araçlarına ve özelliklerine bağlantı, VS 2019 yükleyin](media/vs-2019/install-more-tools-features.png)

Bir şablon seçin ve ardından **sonraki**.

## <a name="configure-your-project"></a>Projenizi yapılandırın

**Yeni projenizi yapılandırın** sayfası, proje (ve çözüm) adı, bir disk konumu seçin ve bir Framework sürümünü (seçtiğiniz şablona varsa) seçin. seçeneği vardır.

![VS 2019 ', yeni proje sayfası yapılandırma](media/vs-2019/configure-new-project.png)

> [!NOTE]
> Bir proje veya çözüm Visual Studio'da Aç zaten varsa, yeni bir proje oluşturursanız, ek bir yapılandırma seçeneği kullanılabilir. Yeni bir çözüm oluşturabilir veya zaten açık olan çözüme yeni projeyi eklemek isteyebilirsiniz.
>
> ![Yeni çözüm oluşturma veya mevcut çözümde VS 2019 ekleyin](media/vs-2019/configure-new-project-solution.png)

Tıklayın **Oluştur** yeni projeyi oluşturmak için.

::: moniker-end

## <a name="add-additional-projects-to-a-solution"></a>Ek projeleri çözüme ekleme

Bir çözüm için ek bir proje eklemek istiyorsanız, ndeki çözüm düğümüne sağ **Çözüm Gezgini** ve **Ekle** > **yeni proje**.

## <a name="see-also"></a>Ayrıca bkz.

- [Projeler ve çözümler oluşturma](creating-solutions-and-projects.md)

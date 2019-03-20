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
ms.openlocfilehash: 61d995f2d625e1f10cafc681e799060b5a439196
ms.sourcegitcommit: 5af29226aef0a3b4a506b69a08a97cfd21049521
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/20/2019
ms.locfileid: "58268839"
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

Üzerinde **yeni bir proje oluşturma** sayfasında, kullanılabilir proje şablonları tarafından filtreleyebilirsiniz **dil** (örneğin, C# veya C++), **Platform** (örneğin, Windows veya Azure için), ve **proje türü** (örneğin, masaüstü veya Web). Aranacak metin şablonları, örneğin, daha fazla filtrelemek için arama kutusuna girebilirsiniz **asp.net**.

![Visual Studio 2019 proje şablonu filtreleri](media/vs-2019/create-new-project-filters.png)

Bir şablon seçin ve ardından **sonraki**.

## <a name="configure-your-project"></a>Projenizi yapılandırın

**Yeni projenizi yapılandırın** sayfası, proje (ve çözüm) adı, bir konuma kaydedin ve bir Framework sürümünü (seçtiğiniz şablona varsa) yeri seçme seçenekleri içerir.

![VS 2019 ', yeni proje sayfası yapılandırma](media/vs-2019/configure-new-project.png)

Tıklayın **Oluştur** yeni projeyi oluşturmak için.

::: moniker-end

## <a name="add-additional-projects-to-a-solution"></a>Ek projeleri çözüme ekleme

Bir çözüme ek bir proje eklemek istiyorsanız çözüm düğümü seçin **Çözüm Gezgini**ve ardından menü çubuğunda, **proje** > **Add New Item**.

## <a name="see-also"></a>Ayrıca bkz.

- [Projeler ve çözümler oluşturma](creating-solutions-and-projects.md)

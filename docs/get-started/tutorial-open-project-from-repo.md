---
title: 'Öğretici: Bir depodan proje açma'
description: Visual Studio kullanarak bir Git veya Azure DevOps deposunda bir projeyi açmayı öğrenin.
ms.custom: get-started
ms.date: 03/13/2019
ms.technology: vs-ide-general
ms.prod: visual-studio-windows
ms.topic: tutorial
author: TerryGLee
ms.author: tglee
manager: jillfra
dev_langs:
- CSharp
ms.workload:
- dotnet
- dotnetcore
ms.openlocfilehash: f017e0ef3d7b76ba4d5de18ecab614f030b07501
ms.sourcegitcommit: 4ffb7be5384ad566ce46538032bf8561754c61a4
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/15/2019
ms.locfileid: "58070080"
---
# <a name="tutorial-open-a-project-from-a-repo"></a>Öğretici: Bir depodan proje açma

Bu öğreticide, Visual Studio'yu ilk kez bir depoya bağlanmak ve buradan bir proje açmak için kullanacaksınız.

::: moniker range="vs-2017"

Visual Studio henüz yüklemediyseniz, Git [Visual Studio indirmeleri](https://visualstudio.microsoft.com/downloads/?utm_medium=microsoft&utm_source=docs.microsoft.com&utm_campaign=inline+link&utm_content=download+vs2017) ücretsiz yüklemek için sayfa.

::: moniker-end

::: moniker range="vs-2019"

Visual Studio henüz yüklemediyseniz, Git [Visual Studio indirmeleri](https://visualstudio.microsoft.com/downloads/?utm_medium=microsoft&utm_source=docs.microsoft.com&utm_campaign=inline+link&utm_content=download+vs2019+rc) ücretsiz yüklemek için sayfa.

::: moniker-end

## <a name="open-a-project-from-a-github-repo"></a>Bir GitHub deposundan proje açma

1. Visual Studio 2017'yi açın.

1. Üstteki menü çubuğundan seçin **dosya** > **açık** > **kaynak denetiminden Aç**.

   **Takım Gezgini - Bağlan** bölmesi açılır.

    ![Visual Studio IDE içinde Takım Gezgini penceresi](./media/open-proj-repo-team-explorer.png)

1. İçinde **yerel Git depoları** bölümünde, seçin **kopya**.

    ![Yerel Git depoları bölümünde Kopyala öğesini seçin](./media/open-proj-repo-local-git-repo-clone.png)

1. İfadesini içeren kutuya ***kopyalamak için bir Git deposunun URL'sini girin***yazın veya deponuz için URL'yi yapıştırın ve sonra basın **Enter**. (Bu durumda, bunu; Github'da oturum açmak için bir istem alabilirsiniz.)

   Deponuzu Visual Studio klonlar sonra Takım Gezgini kapatır ve Çözüm Gezgini açılır. Bildiren bir ileti görünür *çözümler ve klasörler yukarıdaki çözümlerinin bir listesini görüntülemek için tıklatın*. Seçin **çözümler ve klasörler**.

   ![Çözüm Gezgini'nden "Çözümler ve klasörler" seçin](./media/open-proj-repo-github-solutions-folders.png)

1. Kullanılabilir bir çözüm dosyası varsa, "Çözümler ve klasörler" açılan menüsünde görünür. Bu dosyayı seçin ve Visual Studio çözümünüzü açar.

   ![Çözüm Gezgini aşağı açılan listeden açmak istediğiniz seçin](./media/open-proj-repo-github-solutions-folders-picker.png)

   Deponuzdaki bir çözüm dosyası (özellikle bir .sln dosyası) yoksa açılan menüsü "Hiçbir çözüm bulunamadı." Yazar Ancak, herhangi bir dosyadan klasör menüsü, Visual Studio Kod Düzenleyicisi'nde açmak için çift tıklayabilirsiniz.

### <a name="review-your-work"></a>Çalışmanızı gözden geçirin

Önceki bölümde tamamlanan iş denetlemek için aşağıdaki animasyon görüntüleyin.

   ![Visual Studio kullanarak bir GitHub deposunda bir projeyi açma animasyon](./media/open-project-from-github.gif)

## <a name="open-a-project-from-an-azure-devops-repo"></a>Azure DevOps bir depodan proje açma

1. Visual Studio 2017'yi açın.

1. Üstteki menü çubuğundan seçin **dosya** > **açık** > **kaynak denetiminden Aç**.

   **Takım Gezgini - Bağlan** bölmesi açılır.

    ![Visual Studio IDE içinde Takım Gezgini penceresi](./media/open-proj-repo-team-explorer.png)

1. Azure DevOps deponuza bağlamak için iki yolu vardır:

      - İçinde **barındırılan hizmet sağlayıcıları** bölümünde, seçin **Bağlan...** .

        ![Barındırılan hizmet sağlayıcıları bölümünde Visual Studio IDE içinde Takım Gezgini penceresi](./media/open-proj-repo-azure-devops.png)

      - İçinde **bağlantıları Yönet** aşağı açılan listesinde **projeye bağlan...** .

        ![Bağlantıları Yönet bölümünün Visual Studio IDE içinde Takım Gezgini penceresi](./media/open-proj-repo-azuredevops-manage-connections.png)

1. İçinde **projeye bağlan** iletişim kutusunda, bağlanmak ve ardından istediğiniz depoyu seçin **kopya**.

      ![Visual Studio'dan oluşturulan "Bir proje Bağlan" iletişim kutusu](./media/open-proj-azure-devops-connect-cloud-clone.png)

    > [!NOTE]
    > Liste kutusunda gördüğünüz erişiminiz Azure DevOps depolar bağlıdır.

1. Deponuzu Visual Studio klonlar sonra Takım Gezgini kapatır ve Çözüm Gezgini açılır. Bildiren bir ileti görünür *çözümler ve klasörler yukarıdaki çözümlerinin bir listesini görüntülemek için tıklatın*. Seçin **çözümler ve klasörler**.

      ![Visual Studio'da Takım Gezgini'nden "Çözümler ve klasörler" bildirimi](./media/open-proj-repo-solutions-folders.png)

   Bir çözüm dosyası (özellikle bir .sln dosyası), "Çözümler ve klasörler" açılan menüsünün görünür. Bu dosyayı seçin ve Visual Studio çözümünüzü açar.

   Deponuzdaki bir çözüm dosyası yoksa, açılan menüsü "Hiçbir çözüm bulunamadı" varsayalım. Ancak, herhangi bir dosyadan klasör menüsü, Visual Studio Kod Düzenleyicisi'nde açmak için çift tıklayabilirsiniz.
  
## <a name="next-steps"></a>Sonraki adımlar

Visual Studio ile kod için hazır olduğunuzda aşağıdaki dile özgü öğreticileri hiçbirine inceleyin:

- [Visual Studio öğreticiler |**C#**](./csharp/index.yml)
- [Visual Studio öğreticiler | **Visual Basic**](./visual-basic/index.yml)
- [Visual Studio öğreticiler | **C++**](/cpp/get-started/)
- [Visual Studio öğreticiler | **Python**](/visualstudio/python/)
- [Visual Studio öğreticiler | **JavaScript**, **TypeScript**, ve **Node.js**](/visualstudio/javascript/)

## <a name="see-also"></a>Ayrıca bkz.

- [Azure DevOps Hizmetleri: Azure depoları ve Visual Studio ile çalışmaya başlama](/azure/devops/repos/git/gitquickstart/)
- [Microsoft bilgi edinin: Azure DevOps ile çalışmaya başlama](/learn/modules/get-started-with-devops/)
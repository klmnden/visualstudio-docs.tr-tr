---
title: Unity için Visual Studio Araçları ile çalışmaya başlama | Microsoft Docs
ms.custom: ''
ms.date: 07/03/2018
ms.technology: vs-unity-tools
ms.topic: conceptual
ms.assetid: 66b5b4eb-13b5-4071-98d2-87fafa4598a8
author: conceptdev
ms.author: crdun
manager: crdun
ms.workload:
- unity
ms.openlocfilehash: 9d924ee92258e348d5ffee1551fcde7707d711cf
ms.sourcegitcommit: 240c8b34e80952d00e90c52dcb1a077b9aff47f6
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/23/2018
ms.locfileid: "49855215"
---
# <a name="get-started-with-visual-studio-tools-for-unity"></a>Unity için Visual Studio Araçları ile çalışmaya başlama

## <a name="install-visual-studio"></a>Visual Studio'yu yükleme

### <a name="unity-bundled-installation"></a>Unity paket yükleme

Unity 2018.1 ile başlayarak, Visual Studio, C# betik için varsayılan düzenleyici Unity olduğu ve Unity indirme Yardımcısı, yanı sıra Unity hub'ı yükleme aracı dahil edilir.

- Unity'de indirme [store.unity.com](https://store.unity.com/).

Yükleme sırasında Visual Studio ile Unity yüklenecek bileşenlerin listesini işaretlendiğinden emin olun:

#### <a name="unity-hub"></a>Unity Hub

![Unity hub'ı yükleme](media/vstu_unity-hub.png)

#### <a name="unity-download-assistant"></a>Unity Yükleme Yardımcısı

![Unity Yükleme Yardımcısı'nı yükleme](media/vstu_download-assistant.png)

#### <a name="check-for-updates-to-visual-studio"></a>Visual Studio Güncelleştirmeleri denetle

Unity yüklemenizle dahil Visual Studio sürümü, en son olmayabilir. En son araçları ve özelliklere erişiminiz olduğundan emin olmak güncelleştirmeleri denetlemek için önerilir.

- [Visual Studio’yu güncelleştirme](../install/update-visual-studio.md)

### <a name="manual-installation"></a>El ile yükleme

Zaten Visual Studio 2017'in yüklü veya el ile yüklemeyi tercih ederseniz, Visual Studio Yükleyicisi'ni çalıştırın.

1. [Visual Studio yükleyicisini indirin](/visualstudio/install/install-visual-studio), veya zaten yüklü değilse açın.

1. Tıklayın **Değiştir** (zaten yüklü değilse) veya **yükleme** (yeni yüklemeler için) istenen Visual Studio sürümünüz için.

1. Üzerinde **iş yükleri** sekmesinde, kaydırma **mobil ve oyun** seçin ve bölüm **Unity ile oyun geliştirme** iş yükü.

    ![Unity iş yükü](media/vstu_unity-workload.png)

1. Tıklayın **Değiştir** (zaten yüklü değilse) veya **yükleme** (yeni yüklemeler için) Yükleyici penceresinde sağ alt köşesindeki.

## <a name="configure-unity-for-use-with-visual-studio"></a>Unity Visual Studio ile kullanılacak şekilde yapılandırma

Visual Studio ile Unity 2018.1 başlayarak, varsayılan harici kod Düzenleyicisi'nde Unity olmalıdır. Dış betik Düzenleyicisi Visual Studio'nun belirli bir sürüme değiştirmek ya da bu onaylayın:

1. Seçin **tercihleri** gelen **Düzenle** menüsü.

   ![Tercihler seçin](media/vstu_unity-preferences.png)

2. Tercihler iletişim kutusunda, seçmek **dış Araçlar** sekmesi.

3. Gelen **dış betik Düzenleyicisi** açılan listesinde, istediğiniz Visual Studio sürümünüze listelenmişse seçin, aksi takdirde **Gözat...** .

   ![Visual Studio seçin](media/vstu_unity-external-tools.png)

4. Varsa **Gözat...**  olan seçili gidin **Common7/IDE** seçin ve Visual Studio yükleme dizini içinde dizin **devenv.exe**. Ardından **açık**.

   ![Aç'ı seçin](media/vstu_browse-for-application.png)

5. Visual Studio içinde seçildikten sonra **dış betik Düzenleyicisi** listesinde, onaylayın **Düzenleyici ekleme** onay kutusunun seçili.

6. Kapat **tercihleri** yapılandırma işlemini tamamlamak için iletişim.

## <a name="support-for-older-versions"></a>Eski sürümleri için destek

 İndirip Unity için Visual Studio Araçları, Visual Studio Market'ten yükleyebilirsiniz. Visual Studio sürümünüz için doğru paketi yüklemeniz gerekir.

- Visual Studio 2015 Community, Visual Studio 2015 Professional veya Visual Studio 2015 Enterprise için:

   [Unity için Visual Studio 2015 Araçları'nı indirin](https://marketplace.visualstudio.com/items?itemName=SebastienLebreton.VisualStudio2015ToolsforUnity)

> [!NOTE]
> Unity için Visual Studio Araçları Unity 5.2 gerektirir ve yukarıdaki Visual Studio'nun sürümü yanı sıra Visual Studio Community, Professional, Premium veya Enterprise gibi uzantıları destekleyen. Unity için Visual Studio Araçları Unity yüklemenizde etkinleştirildiğini doğrulamak için **hakkında Unity** gelen **yardımcı** menü metni ara "Microsoft Visual Studio Araçları ve Unity için etkin" olarak sol alt iletişim.
> ![Unity hakkında](media/vstu_about-unity.png)

## <a name="next-steps"></a>Sonraki adımlar

 Çalışmak ve Unity projenizde Visual Studio hata ayıklama hakkında bilgi edinmek için [Unity için Visual Studio Araçları](../cross-platform/using-visual-studio-tools-for-unity.md).

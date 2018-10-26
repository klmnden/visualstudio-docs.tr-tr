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

### <a name="unity-bundled-installation"></a>Unity'le birlikte yükleme

Unity 2018.1 ile başlayarak, Visual Studio, Unity için varsayılan C# kod düzenleyicisidir ve Unity Yükleme Yardımcısı'nın yanı sıra Unity Hub yükleme aracında bulunabilir.

- Unity'i [store.unity.com](https://store.unity.com/)den indirin.

Yükleme sırasında Visual Studio'nun Unity ile yüklenecek bileşenlerin listesinde işaretlendiğinden emin olun:

#### <a name="unity-hub"></a>Unity Hub

![Unity hub'ı yükleme](media/vstu_unity-hub.png)

#### <a name="unity-download-assistant"></a>Unity Yükleme Yardımcısı

![Unity Yükleme Yardımcısı'nı yükleme](media/vstu_download-assistant.png)

#### <a name="check-for-updates-to-visual-studio"></a>Visual Studio için güncelleştirmeleri denetle

Unity yüklemenize dahil olan Visual Studio sürümü, en son sürüm olmayabilir. En son araçlara ve özelliklere erişiminiz olduğundan emin olmak için güncelleştirmeleri denetlemeniz önerilir.

- [Visual Studio’yu güncelleştirme](../install/update-visual-studio.md)

### <a name="manual-installation"></a>El ile yükleme

Zaten Visual Studio 2017'niz yüklüyse veya el ile yüklemeyi tercih ederseniz, Visual Studio yükleyicisini çalıştırın.

1. [Visual Studio yükleyicisini indirin](/visualstudio/install/install-visual-studio), veya zaten yüklüyse açın.

2. İstediğiniz Visual Studio sürümü için **Değiştir**e (zaten yüklüyse) veya **Yükle**ye (yeni yüklemeler için) tıklayın.

3. **İşlemler** sekmesinden, **Mobil ve Oyun**a geçin ve **Unity ile oyun geliştirme** işlemini seçin.

    ![Unity işlemi](media/vstu_unity-workload.png)

4. Yükleyici penceresinin sağ alt köşesindeki **Değiştir**e (zaten yüklüyse) veya **Yükle**ye (yeni yüklemeler için) tıklayın.

## <a name="configure-unity-for-use-with-visual-studio"></a>Unity'i Visual Studio ile kullanılacak şekilde yapılandırma

 Unity 2018.1 ile başlayarak Visual Studio, Unity'de varsayılan harici kod düzenleyicisi olmalıdır. Bunu onaylayın ya da kod düzenleyicisini Visual Studio'nun belirli bir sürümüne değiştirin:

1. **Tercihler**den gelen **Düzenle** menüsünü seçin.

   ![Tercihleri seçin](media/vstu_unity-preferences.png)

2. Tercihler iletişim kutusunda **Dış Araçlar** sekmesini seçin.

3. Gelen **Harici Kod Düzenleyicisi** listesinden, istediğiniz Visual Studio sürümü listelenmişse seçin, aksi takdirde **Gözat...** .

   ![Visual Studio'yu seçin](media/vstu_unity-external-tools.png)

4. **Gözat...** seçildiyse Visual Studio yükleme dizininin içindeki **Common7/IDE** klasörüne gidin ve **devenv.exe**yi seçin. Ardından **Aç**a tıklayın.

   ![Aç'ı seçin](media/vstu_browse-for-application.png)

5. Visual Studio **Harici Kod Düzenleyicisi** listesinde seçildikten sonra, **Düzenleyici Ekleme** onay kutusunun seçili olduğundan emin olun.

6. Yapılandırma işlemini tamamlamak için **Tercihler** penceresini kapatın.

## <a name="support-for-older-versions"></a>Eski sürümler için destek

 Unity için Visual Studio Araçları'nı Visual Studio Market'ten indirip yükleyin. Visual Studio sürümünüz için doğru paketi yüklemeniz gerekir.

- Visual Studio 2015 Community, Visual Studio 2015 Professional veya Visual Studio 2015 Enterprise için:

   [Unity için Visual Studio 2015 Araçları'nı indirin](https://marketplace.visualstudio.com/items?itemName=SebastienLebreton.VisualStudio2015ToolsforUnity)

> [!NOT]
> Unity için Visual Studio Araçları Unity 5.2 ve üstünü, ayrıca Visual Studio Community, Professional, Premium veya Enterprise gibi uzantıları destekleyen bir Visual Studio sürmünü gerektirir. Unity için Visual Studio Araçları'nın Unity yüklemenizde etkinleştirildiğini doğrulamak için **Yardım** menüsünde **Unity Hakkında**yı seçin ve pencerenin sol alt kısmında "Microsoft Visual Studio Araçları ve Unity için etkin" metninin varlığını kontrol edin.
> ![Unity hakkında](media/vstu_about-unity.png)

## <a name="next-steps"></a>Sonraki adımlar

 Unity projenizde Visual Studio ile nasıl çalışabileceğiniz ve hata ayıklayabileceğiniz hakkında bilgi edinmek için [Unity için Visual Studio Araçları](../cross-platform/using-visual-studio-tools-for-unity.md)na bakın.

---
title: Visual Studio’yu değiştirme
titleSuffix: ''
description: Visual Studio, adım adım değiştirme hakkında bilgi edinin.
ms.custom: H1Hack27Feb2017,seodec18
ms.date: 07/31/2019
ms.topic: conceptual
helpviewer_keywords:
- modify Visual Studio
- change visual studio
- changing Visual Studio
- customize Visual Studio
ms.assetid: 3399ea7b-a291-4a9e-80a1-b861a21afa1d
author: TerryGLee
ms.author: tglee
manager: jillfra
ms.workload:
- multiple
ms.prod: visual-studio-windows
ms.technology: vs-installation
ms.openlocfilehash: ad5b8a0c261ed967710480b0abd3a2b9d34f01ce
ms.sourcegitcommit: 5694c5236fa32ba7f5bc1236a853f725ec7557e9
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/31/2019
ms.locfileid: "68681382"
---
# <a name="modify-visual-studio-by-adding-or-removing-workloads-and-components"></a>İş yüklerini ve bileşenleri ekleyerek veya kaldırarak Visual Studio 'Yu değiştirme

::: moniker range="vs-2019"

Visual Studio 'Yu, istediğinizde yalnızca istediğiniz şeyi içerecek şekilde değiştirmek kolaydır. Bunu yapmak için, iş yüklerini ve bileşenleri eklemek veya kaldırmak üzere Visual Studio Yükleyicisi açın.

::: moniker-end

::: moniker range="vs-2017"

Sadece biz bunu daha da kolaylaştırdık gerçekleştirmek istediğiniz görevleri eşleştirmek için Visual Studio kişiselleştirmek için Ayrıca, Visual Studio, çok özelleştirmek daha kolay hale getirdik. Bunu yapmak için yeni Visual Studio Yükleyicisi'ni başlatın ve istediğiniz değişiklikleri yapın.

::: moniker-end

İşte nasıl.

## <a name="modify-workloads"></a>İş yüklerini değiştirme

 İş yükleri, kullanmakta olduğunuz programlama dili veya platformu için gereken özellikleri içerir. Bunu yapmak istediğiniz zaman, istediğiniz iş destekler, böylece Visual Studio değiştirmek için iş yüklerini kullanın.

>[!IMPORTANT]
>Yüklemek, güncelleştirmek veya Visual Studio değiştirmek için yönetici izinleri olan bir hesapla oturum açmalısınız. Daha fazla bilgi için bkz. [Kullanıcı izinleri ve Visual Studio](../ide/user-permissions-and-visual-studio.md).

>[!TIP]
> Aşağıdaki yordamda bir internet bağlantınız olduğunu varsaymaktadır. Daha önce oluşturulan ve Visual Studio 'nun [çevrimdışı yüklemesinin](create-an-offline-installation-of-visual-studio.md) nasıl değiştirileceği hakkında daha fazla bilgi için bkz. [ağ tabanlı Visual Studio dağıtımları için güncelleştirmeleri denetleme](controlling-updates-to-visual-studio-deployments.md) sayfası.

::: moniker range="vs-2017"

1. Bilgisayarınızda Visual Studio yükleyicisi bulun.

     Örneğin, Windows 10 çalıştıran bir bilgisayarda seçin **Başlat**ve harfi kaydırın **V**, olarak listelenen burada **Visual Studio yükleyicisi**.

     ![Visual Studio yükleyicisi](media/vs2017-locate-the-visual-studio-installer.PNG "Microsoft Visual Studio yükleyicisi bulunamıyor")

     >[!NOTE]
     >Bazı bilgisayarlarda, Visual Studio yükleyicisi harfi altında listelenebilir **"M"** olarak **Microsoft Visual Studio yükleyicisi**.<br/><br/> Alternatif olarak, Visual Studio yükleyicisi şu konumda bulabilirsiniz: `C:\Program Files (x86)\Microsoft Visual Studio\Installer\vs_installer.exe`

1. ' A tıklayın veya yükleyiciyi başlatmak için dokunun ve ardından **Değiştir**.

     ![Başlatma veya Visual Studio'yu değiştirme](media/modify-visual-studio.png "değiştirmek, Visual Studio 2017")

     Bekleyen bir güncelleştirme varsa, Değiştir düğmesine içinde farklı bir yerdir. Bu şekilde, Visual Studio, güncelleştirmeden Bunu yapmak seçmelidir değiştirebilirsiniz. Tıklayın **daha fazla**ve ardından **Değiştir**.

     ![Visual Studio'yu değiştirme veya güncelleştirme](media/modify-or-update-visual-studio.png "güncelleştirme veya Visual Studio 2017 değiştirme")

1. Gelen **iş yükleri** ekran seçin veya yüklemek veya kaldırmak istediğiniz iş yüklerini seçimini kaldırın.

    ![Visual Studio 2017 Kurulum iletişim](media/vs2017-modify-workloads.PNG "Visual Studio 2017'de bir iş yükünü seçin")

1. Seçin **Değiştir** yeniden.

1. Yeni iş yükleri ve bileşenler yüklendikten sonra seçin **başlatma**.

::: moniker-end

::: moniker range="vs-2019"

1. Bilgisayarınızda Visual Studio yükleyicisi bulun.

     Örneğin, Windows 10 çalıştıran bir bilgisayarda seçin **Başlat**ve harfi kaydırın **V**, olarak listelenen burada **Visual Studio yükleyicisi**.

     ![Visual Studio yükleyicisi Windows 'Tan açın](media/vs-2019/vs-installer-windows-start.png "Visual Studio yükleyicisi açın")

     > [!NOTE]
     > Aşağıdaki konumda Visual Studio Yükleyicisi de bulabilirsiniz:
     >
     > `C:\Program Files (x86)\Microsoft Visual Studio\Installer\vs_installer.exe`

    Devam etmeden önce yükleyiciyi güncelleştirmeniz gerekebilir. Bu durumda, istemleri izleyin.

1. Yükleyicide, yüklediğiniz Visual Studio sürümünü bulun ve ardından **Değiştir**' i seçin.

     ![Visual Studio 'Yu güncelleştirme veya değiştirme](media/vs-2019/vs-installer-modify.png "Visual Studio 2019 'Yi güncelleştirme veya değiştirme")

1. **Iş yükleri** sekmesinde, yüklemek veya kaldırmak istediğiniz iş yüklerini seçin veya seçimini kaldırın.

    ![Visual Studio 2019 kurulum iletişim kutusu](media/vs-2019/vs-installer-modify-workloads.png "Visual Studio 2019 'de iş yükü seçme")

1. **İndirme sırasında varsayılan yüklemeyi** kabul etmek mi yoksa **Tümünü indir ve yükle** seçeneğini belirleyin.

    ![Visual Studio 2019 kurulum seçenekleri](media/vs-2019/vs-installer-choose-install-or-download.png "İlk kez karşıdan yükleme veya indirme sırasında yüklemeyi seçin ve daha sonra yükleyin")

    Önce indirmek ve sonra yüklemek istiyorsanız "tümünü Indir ve Yükle" seçeneği kullanışlıdır.

1. **Değiştir**'i seçin.

1. Yeni iş yükleri ve bileşenler yüklendikten sonra Visual Studio Yükleyicisi **Başlat** ' ı seçin.

::: moniker-end

## <a name="modify-individual-components"></a>Tek tek bileşenler değiştirme

Visual Studio yüklemenizi özelleştirmek için iş yüklerini yüklemek istemiyorsanız, Visual Studio Yükleyicisi **bireysel bileşenler** sekmesini seçin, istediğiniz öğeleri seçin ve ardından istemleri izleyin.

[!INCLUDE[install_get_support_md](includes/install_get_support_md.md)]

## <a name="see-also"></a>Ayrıca bkz.

* [Visual Studio’yu güncelleştirme](update-visual-studio.md)
* [Visual Studio’nun ağ tabanlı yüklemesini güncelleştirme](update-a-network-installation-of-visual-studio.md)
* [Bakım temeliyle Visual Studio 'Yu güncelleştirme](update-servicing-baseline.md)
* [Ağ tabanlı Visual Studio dağıtımlarına yönelik güncelleştirmeleri denetleme](controlling-updates-to-visual-studio-deployments.md)
* [Visual Studio'yu kaldırma](uninstall-visual-studio.md)

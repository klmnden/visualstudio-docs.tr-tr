---
title: Visual Studio’yu değiştirme
titleSuffix: ''
description: Visual Studio, adım adım değiştirme hakkında bilgi edinin.
ms.custom: H1Hack27Feb2017,seodec18
ms.date: 03/30/2018
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
ms.openlocfilehash: a08a14d8d07248efdcac759852a38777745e9a51
ms.sourcegitcommit: d4bea2867a4f0c3b044fd334a54407c0fe87f9e8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/01/2019
ms.locfileid: "58789724"
---
# <a name="modify-visual-studio-by-adding-or-removing-workloads-and-components"></a>Visual Studio ekleyerek veya iş yüklerinin ve bileşenlerin kaldırarak değiştirme

::: moniker range="vs-2019"

İstediğiniz zaman yalnızca, istediğiniz içerir, böylece Visual Studio değiştirmek kolay bir işlemdir. Bunu yapmak için iş yükleri ve bileşenleri eklemek veya kaldırmak için Visual Studio Yükleyicisi'ni açın.

::: moniker-end

::: moniker range="vs-2017"

Sadece biz bunu daha da kolaylaştırdık gerçekleştirmek istediğiniz görevleri eşleştirmek için Visual Studio kişiselleştirmek için Ayrıca, Visual Studio, çok özelleştirmek daha kolay hale getirdik. Bunu yapmak için yeni Visual Studio Yükleyicisi'ni başlatın ve istediğiniz değişiklikleri yapın.

::: moniker-end

İşte nasıl.

## <a name="modify-workloads"></a>İş yüklerini değiştirme

 İş yükleri programlama dili veya kullanmakta olduğunuz platform için ihtiyacınız olan özellikleri içerir. Bunu yapmak istediğiniz zaman, istediğiniz iş destekler, böylece Visual Studio değiştirmek için iş yüklerini kullanın.

>[!IMPORTANT]
>Yüklemek, güncelleştirmek veya Visual Studio değiştirmek için yönetici izinleri olan bir hesapla oturum açmalısınız. Daha fazla bilgi için [kullanıcı izinleri ve Visual Studio](../ide/user-permissions-and-visual-studio.md).

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

     ![Visual Studio yükleyicisini açın](media/vs2019-visual-studio-installer.png "Visual Studio Yükleyicisi'ni açın")

     > [!NOTE]
     > Ayrıca, Visual Studio yükleyicisi şu konumda bulabilirsiniz:
     >
     > `C:\Program Files (x86)\Microsoft Visual Studio\Installer\vs_installer.exe`

    Yükleyici, devam etmeden önce güncelleştirmesi gerekebilir. Bu durumda, yönergeleri izleyin.

1. Yükleyici, yüklediğiniz Visual Studio sürümü için arayın ve ardından **Değiştir**.

     ![Visual Studio'yu değiştirme veya güncelleştirme](media/vs-2019/vs-installer-modify.png "güncelleştirme veya Visual Studio 2017 değiştirme")

1. İçinde **iş yükleri** sekmesinde seçin veya yüklemek veya kaldırmak istediğiniz iş yüklerini seçimini kaldırın.

    ![Visual Studio 2019 Kurulum iletişim kutusu](media/vs-2019/vs-installer-modify-workloads.png "Visual Studio 2019 içinde bir iş yükünü seçin")

1. Varsayılanı kabul etmek isteyip istemediğinizi seçin **indirilirken Yükle** seçeneği veya **tümünü indir ve Yükle** seçeneği.

    ![Visual Studio 2019 Kurulum Seçenekleri](media/vs-2019/vs-installer-choose-install-or-download.png "indirilirken yükle veya indirmeniz ve daha sonra yüklemek seçin")

    "Tümünü indir ve Yükle" seçenek indirmeniz ve daha sonra yüklemek istiyorsanız yararlı olur.

1. Seçin **değiştirme**.

1. Yeni iş yükleri ve bileşenler yüklendikten sonra seçin **başlatma** Visual Studio Yükleyicisi'nden.

::: moniker-end

## <a name="modify-individual-components"></a>Tek tek bileşenler değiştirme

Öğesini Visual Studio yüklemenizi özelleştirmek için iş yüklerini yüklemek istemiyorsanız **tek tek bileşenler** sekmesinde Visual Studio Yükleyicisi'nden, neleri istediğiniz ve daha sonra izleyin seçin yönergeleri.

[!INCLUDE[install_get_support_md](includes/install_get_support_md.md)]

## <a name="see-also"></a>Ayrıca bkz.

* [Visual Studio’yu güncelleştirme](update-visual-studio.md)
* [Visual Studio’nun ağ tabanlı yüklemesini güncelleştirme](update-a-network-installation-of-visual-studio.md)
* [Visual Studio'yu kaldırma](uninstall-visual-studio.md)

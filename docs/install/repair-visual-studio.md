---
title: Visual Studio’yu onarın
titleSuffix: ''
description: Visual Studio 2017 yüklemesini onarmak hakkında bilgi edinin
ms.date: 03/30/2019
ms.custom: seodec18
ms.topic: conceptual
author: TerryGLee
ms.author: tglee
manager: jillfra
ms.workload:
- multiple
ms.prod: visual-studio-windows
ms.technology: vs-installation
ms.openlocfilehash: 690fe29373e80d9dfc560a616d0e914731d9b6cf
ms.sourcegitcommit: 0a2fdc23faee77187e10a1c19665ba5a1ac68e72
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/10/2019
ms.locfileid: "59477532"
---
# <a name="repair-visual-studio"></a>Visual Studio’yu onarın

::: moniker range="vs-2017"

Bazı durumlarda Visual Studio yüklemenizin zarar görmüş veya bozulmuş olur. Bir onarım bunu düzeltebilirsiniz.

1. Bulma **Visual Studio yükleyicisi** bilgisayarınızda.

     Örneğin, Windows 10 Yıldönümü güncelleştirmesi bir bilgisayarda çalışan veya daha sonra **Başlat**ve harfi kaydırın **V**, olarak listelenen burada **Visual Studio yükleyicisi**.

   > [!NOTE]
   > Bazı bilgisayarlarda, Visual Studio yükleyicisi harfi altında listelenebilir **"M"** olarak **Microsoft Visual Studio yükleyicisi**.
   >
   > Alternatif olarak, Visual Studio yükleyicisi şu konumda bulabilirsiniz: `C:\Program Files (x86)\Microsoft Visual Studio\Installer\vs_installer.exe`

1. Yükleyici açın, **daha fazla**ve ardından **onarım**.

    ![Visual Studio Yükleyicisi'nden Visual Studio onarma](media/repair-visual-studio.png "Visual Studio Yükleyicisi'nden Visual Studio'yu onarma")
    
   > [!NOTE]
   > Visual Studio onarılırsa ortam sıfırlanır. Kullanıcı başına uzantılar yüklü yükseltme, kullanıcı ayarlarını yerel özelleştirmeler ister ve profilleri kaldırılır. Temalar, renkler, tuş bağlamaları eşitlenen ayarlarınız geri yüklenir.
   >

   > [!TIP]
   > **Onarım** seçeneği yalnızca Visual Studio'nun yüklü örnekleri için görünür. Görmüyorsanız, **onarım** seçeneği, büyük olasılıkla olan, seçtiğiniz **daha fazla** Visual Studio Yükleyicisi'nde "Yüklü" yerine "Kullanılabilir" listelenen sürüm.

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

1. Yükleyicide, yüklediğiniz Visual Studio sürümü için bakın. Ardından, **daha fazla**ve ardından **onarım**.

     ![Visual Studio 2019 onarım](media/vs-2019/vs-installer-repair.png "Visual Studio 2019 onarın")

   > [!NOTE]
   > Visual Studio onarılırsa ortam sıfırlanır. Kullanıcı başına uzantılar yüklü yükseltme, kullanıcı ayarlarını yerel özelleştirmeler ister ve profilleri kaldırılır. Temalar, renkler, tuş bağlamaları eşitlenen ayarlarınız geri yüklenir.
   >

   > [!TIP]
   > **Onarım** seçeneği yalnızca Visual Studio'nun yüklü örnekleri için görünür. Görmüyorsanız, **onarım** seçeneği, büyük olasılıkla olan, seçtiğiniz **daha fazla** Visual Studio Yükleyicisi'nde "Yüklü" yerine "Kullanılabilir" listelenen sürüm.

::: moniker-end


[!INCLUDE[install_get_support_md](includes/install_get_support_md.md)]

## <a name="see-also"></a>Ayrıca bkz.

* [Visual Studio'yu yükleme](install-visual-studio.md)
* [Visual Studio’yu güncelleştirme](update-visual-studio.md)
* [Visual Studio'yu kaldırma](uninstall-visual-studio.md)
* [Visual Studio yükleme ve yükseltme sorunlarını giderme](troubleshooting-installation-issues.md)

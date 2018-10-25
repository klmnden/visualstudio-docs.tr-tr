---
title: Visual Studio örneklerini algılamaya ve yönetmeye yönelik araçlar
description: Algılama ve Visual Studio yüklemeleri istemci makinelerinde yönetmek için kullanabileceğiniz araçları hakkında bilgi edinin.
ms.date: 08/14/2017
ms.technology: vs-acquisition
ms.prod: visual-studio-dev15
ms.topic: conceptual
helpviewer_keywords:
- '{{PLACEHOLDER}}'
- '{{PLACEHOLDER}}'
ms.assetid: 85686707-14C0-4860-9B7A-66485D43D241
author: TerryGLee
ms.author: tglee
manager: douge
ms.workload:
- multiple
ms.openlocfilehash: 9f7696018ec191e851c0d5864ad36e3eeb31b599
ms.sourcegitcommit: 240c8b34e80952d00e90c52dcb1a077b9aff47f6
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/23/2018
ms.locfileid: "49941743"
---
# <a name="tools-for-detecting-and-managing-visual-studio-instances"></a>Visual Studio örneklerini algılamaya ve yönetmeye yönelik araçlar

Visual Studio yüklemeleri istemci makinelerinde algılamaya ve yüklemelerini çok yönetmek için kullanabileceğiniz birçok araç vardır.

## <a name="detecting-existing-visual-studio-instances"></a>Var olan algılama Visual Studio Örnekleri

Kullanılabilir algılamak ve istemci makinelerde yüklü Visual Studio örneklerini yönetmenize yardımcı olacak birkaç araç yaptık:

* [VSWhere](https://github.com/microsoft/vswhere): Visual Studio yerleşik veya yardımcı olan ayrı bir dağıtım için kullanılabilir bir yürütülebilir dosya belirli bir makinedeki tüm Visual Studio Örnekleri konumunu bulun.
* [VSSetup.PowerShell](https://github.com/microsoft/vssetup.powershell): PowerShell betikleri, Visual Studio'nun yüklü örnekleri belirlemek için Kurulum yapılandırması API'yi kullanın.
* [VS ayarlama örnekleri](https://github.com/microsoft/vs-setup-samples): Kurulum yapılandırma API'si var olan bir yüklemesini sorgulamak için nasıl kullanılacağını gösteren C# ve C++ örnekleri.

Ayrıca, [kurulum yapılandırma API'si](https://msdn.microsoft.com/en-us/library/microsoft.visualstudio.setup.configuration.aspx) interrogating Visual Studio örnekleri için kendi yardımcı programlar oluşturmak isteyen geliştiriciler için arabirim sağlar.

## <a name="using-vswhereexe"></a>Vswhere.exe kullanma

`vswhere.exe` otomatik olarak dahil Visual Studio 2017 sürüm 15.2 veya üzeri ya da buradan indirebilirsiniz [sürümler sayfasından](https://github.com/Microsoft/vswhere/releases). Kullanım `vswhere -?` aracı hakkında Yardım bilgilerini almak için. Örneğin, bu komut tüm ürünlerinizin ve prereleases, eski sürümleri dahil olmak üzere Visual Studio sürümlerini gösterir ve sonuçları JSON biçiminde çıkarır:

```cmd
C:\Program Files (x86)\Microsoft Visual Studio\Installer> vswhere.exe -legacy -prerelease -format json
```

>[!TIP]
>Visual Studio 2017'yi yükleme hakkında daha fazla bilgi için bkz: [sistem durumu Ilgaz'ın blog makaleleri](https://blogs.msdn.microsoft.com/heaths/tag/vs2017/).


## <a name="editing-the-registry-for-a-visual-studio-instance"></a>Visual Studio örneği için kayıt defterini düzenleme

Visual Studio 2017'de kayıt defteri ayarları, Visual Studio'nun aynı sürümü aynı bilgisayarda yan yana örneklerini sağlayan özel bir konumda depolanır.

Bu girişler genel kayıt defterinde depolanmaz gibi kayıt defteri ayarlarında değişiklik yapmak için Kayıt Defteri Düzenleyicisi'ni kullanarak yönelik özel yönergeler vardır:

1. Visual Studio 2017 açık örneği varsa, kapatın.
2. Başlangıç `regedit.exe`.
3. Seçin `HKEY_LOCAL_MACHINE` düğümü.
4. Regedit ana menüden **Dosya -> Yığını Yükle...**  ve depolanan özel kayıt defteri dosyasını seçip **AppData\Local** klasör. Örneğin:
   ```
   %localappdata%\Microsoft\VisualStudio\<config>\privateregistry.bin
   ```

   > [!NOTE]
   > `<config>` gözatmak istediğiniz Visual Studio örneğine karşılık gelir.

Yalıtılmış, hive adı haline gelir bir hive adı sağlamanız istenir. Bunu yaptıktan sonra oluşturduğunuz yalıtılmış hive altındaki kayıt defterine Gözat olmalıdır.

> [!IMPORTANT]
> Visual Studio yeniden başlamadan önce sizin oluşturduğunuz yalıtılmış kovanını gerekir. Bunu yapmak için dosyayı seçin yığın Regedit ana menüden ->. (Bunu yapmazsanız, dosyanın kilitli kalır ve Visual Studio başlatmanız mümkün olmayacaktır.)

[!INCLUDE[install_get_support_md](includes/install_get_support_md.md)]

## <a name="see-also"></a>Ayrıca bkz.

* [Visual Studio Yöneticiler Kılavuzu](visual-studio-administrator-guide.md)

---
title: Visual Studio Kaldır
titleSuffix: ''
description: Tamamen Visual Studio, adım adım bilgisayarınızdan öğrenin.
ms.date: 03/30/2019
ms.custom: seodec18
ms.topic: conceptual
f1_keywords:
- uninstall
- uninstall Visual Studio
- remove
- remove Visual Studio
- cleanup
- cleanup Visual Studio
- clean up
- clean up Visual Studio
ms.assetid: 9c81a777-9c95-4934-b517-c60c6dc78799
author: heaths
ms.author: tglee
manager: jillfra
ms.workload:
- multiple
ms.prod: visual-studio-windows
ms.technology: vs-installation
ms.openlocfilehash: 779771c51299239814f7ddd6a9cdbfbed017ac72
ms.sourcegitcommit: d4bea2867a4f0c3b044fd334a54407c0fe87f9e8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/01/2019
ms.locfileid: "58790127"
---
# <a name="remove-visual-studio"></a>Visual Studio Kaldır

Siz işlemi yıkıcı hatayla karşılaşırsanız ve onarmak ya da Visual Studio'yu kaldırın, çalıştırabileceğiniz `InstallCleanup.exe` aracı yükleme dosyalarını ve ürün bilgileri için Visual Studio 2017 veya Visual Studio 2019 yüklü tüm örneklerini kaldırın. Bu aracı çalıştırma yapılmalıdır son çare, onarma veya kaldırma işlemi başarısız oldu ve özellikler, diğer Visual Studio yüklemeleri veya daha sonra da onarılması için gerek duyabileceğiniz diğer ürünleri kaldırabilirsiniz.

Aşağıdaki yönergelerde aşağıdaki davranış farklı komut satırı anahtarları ile aracını çalıştırabilirsiniz:

| Anahtar | Davranış |
| ------ | -------- |
| `-i`   | Diğer bir anahtara geçirilir ve yalnızca ana yükleme dizini ve ürün bilgilerini kaldırır. Bu anahtar varsayılandır. Bu çalıştırdıktan sonra aynı sürümü yeniden yüklemek istiyorsanız, tercih, davranıştır `InstallCleanup.exe` aracı. |
| `-f`   | Bu anahtarın belirtilmesi, ana yükleme dizini, ürün bilgileri ve diğer Visual Studio yüklemeleri veya diğer ürünleri ile paylaşılan yükleme dizininin dışına yüklü çoğu özelliği kaldırır. Bu davranış, Visual Studio, daha sonra yeniden yüklemeden kaldırmak istiyorsanız, tercih edilir. |

1. Visual Studio Yükleyicisi’ni kapatın.
2. Bir yönetici komut istemi açın. Bir yönetici komut istemi açmak için şu adımları izleyin:
   * Tür **cmd** "aramak için buraya yazın" kutusunda.
   * **Komut İstemi**'ne sağ tıklayın ve ardından **Yönetici olarak çalıştır**'a tıklayın.
3. Tam yolunu yazın `InstallCleanup.exe` yardımcı programı ve istediğiniz herhangi bir komut satırı anahtarı geçirin. Varsayılan olarak, yardımcı program yolu aşağıdaki gibidir:
   ```
   C:\Program Files (x86)\Microsoft Visual Studio\Installer\resources\app\layout\InstallCleanup.exe
   ```

Bulunamadı, `InstallCleanup.exe` - Visual Studio yükleyicisi dizini altında bulunan her zaman `%ProgramFiles(x86)%\Microsoft Visual Studio` -yönergelerini izleyin [Visual Studio yükleme](install-visual-studio.md) ve iş yükü seçimi ekran görüntülendiğinde, Kapat Pencere ve önceki adımları tekrar uygulayın.

[!INCLUDE[install_get_support_md](includes/install_get_support_md.md)]

## <a name="see-also"></a>Ayrıca bkz.

* [Visual Studio'yu yükleyin](install-visual-studio.md)
* [Visual Studio’yu güncelleştirme](update-visual-studio.md)
* [Visual Studio’yu değiştirme](modify-visual-studio.md)
* [Visual Studio'yu kaldırma](uninstall-visual-studio.md)

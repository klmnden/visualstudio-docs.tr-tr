---
title: Ayarları İçeri ve Dışarı Aktar komutu
ms.date: 11/21/2018
ms.topic: reference
f1_keywords:
- Tools.ImportandExportSettings
helpviewer_keywords:
- Tools.ImportandExportSettings
- Import and Export Settings command
ms.assetid: 94a06468-a44d-403d-a931-77bbc9d06e56
author: gewarren
ms.author: gewarren
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: b9be5826edf0d7220d30ce5c4a99f333c2ab8b67
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62953224"
---
# <a name="import-and-export-settings-command"></a>Ayarları İçeri ve Dışarı Aktar komutu

Visual Studio ayarlarını sıfırlar veya verir veya içeri aktarır.

## <a name="syntax"></a>Sözdizimi

```cmd
Tools.ImportandExportSettings [/export:filename | /import:filename | /reset]
```

## <a name="switches"></a>Anahtarlar

/ Export:`filename`

İsteğe bağlı. Geçerli ayarları, belirtilen dosyaya dışarı aktarır.

/ import:`filename`

İsteğe bağlı. Belirtilen dosyasındaki ayarlar içeri aktarır.

Reset

İsteğe bağlı. Geçerli ayarları sıfırlar.

## <a name="remarks"></a>Açıklamalar

Açılır anahtarları olmadan bu komutu çalıştırmak **içeri ve dışarı aktarma ayarları** Sihirbazı. Daha fazla bilgi için [ayarlarınızı eşitlemek](../synchronized-settings-in-visual-studio.md) ve [ortam ayarları](../environment-settings.md).

## <a name="example"></a>Örnek

Aşağıdaki komut, geçerli ayarları dosyasına aktarır. `MyFile.vssettings`:

```cmd
Tools.ImportandExportSettings /export:"c:\Files\MyFile.vssettings"
```

## <a name="see-also"></a>Ayrıca bkz.

- [Ortam ayarları](../../ide/environment-settings.md)
- [Ayarlarınızı eşitleyin](../../ide/synchronized-settings-in-visual-studio.md)
- [Visual Studio IDE'yi kişiselleştirme](../../ide/personalizing-the-visual-studio-ide.md)
- [Visual Studio komutları](../../ide/reference/visual-studio-commands.md)
---
title: Ayarları İçeri ve Dışarı Aktar komutu
ms.date: 11/21/2018
ms.prod: visual-studio-dev15
ms.topic: reference
f1_keywords:
- Tools.ImportandExportSettings
helpviewer_keywords:
- Tools.ImportandExportSettings
- Import and Export Settings command
ms.assetid: 94a06468-a44d-403d-a931-77bbc9d06e56
author: gewarren
ms.author: gewarren
manager: douge
ms.workload:
- multiple
ms.openlocfilehash: 38144381520002e1e3e9f9c7b440d6b87b90cb6d
ms.sourcegitcommit: 37fb7075b0a65d2add3b137a5230767aa3266c74
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/02/2019
ms.locfileid: "53943333"
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
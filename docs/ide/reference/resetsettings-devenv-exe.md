---
title: -ResetSettings (devenv.exe)
ms.date: 11/16/2018
ms.prod: visual-studio-dev15
ms.topic: reference
helpviewer_keywords:
- Devenv, /ResetSettings switch
- ResetSettings switch
- /ResetSettings Devenv switch
ms.assetid: 1d41021c-6f58-4bd5-b122-d1c995812192
author: gewarren
ms.author: gewarren
manager: douge
ms.workload:
- multiple
ms.openlocfilehash: 160cbf93cee8ff778a4f84ee833c7fac3d7f26b1
ms.sourcegitcommit: 37fb7075b0a65d2add3b137a5230767aa3266c74
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/02/2019
ms.locfileid: "53830670"
---
# <a name="resetsettings-devenvexe"></a>/ResetSettings (devenv.exe)

Visual Studio varsayılan ayarlarına geri yükler ve Visual Studio IDE otomatik olarak başlatır. İsteğe bağlı olarak belirtilen bir ayarları sıfırlar *vssettings* dosya.

Varsayılan ayarlar, Visual Studio ilk başlatıldığında seçilen profili tarafından belirlenir.

> [!TIP]
> Tümleşik geliştirme ortamı (IDE) kullanarak ayarlarını sıfırlama hakkında bilgi edinmek için [ayarlarına](../environment-settings.md#reset-settings).

## <a name="syntax"></a>Sözdizimi

```cmd
Devenv /ResetSettings SettingsFile
```

## <a name="arguments"></a>Arguments

`SettingsFile`

Dosyanın tam yolunu ve adını *vssettings* Visual Studio'ya uygulamak için dosya.

Genel Geliştirme Ayarları profilini geri yüklemek için kullanın `General`.

## <a name="remarks"></a>Açıklamalar

Hayır ise `SettingsFile` belirtilirse, ayar varsayılan koleksiyonunu seçmek için istenirse sonraki Visual Studio'yu başlatın.

## <a name="example"></a>Örnek

Aşağıdaki komut satırını dosyasında depolanan ayarları uygular `MySettings.vssettings`.

```cmd
Devenv.exe /ResetSettings "C:\My Files\MySettings.vssettings"
```

## <a name="see-also"></a>Ayrıca bkz.

- [Ortam ayarları](../environment-settings.md)
- [Visual Studio IDE'yi kişiselleştirme](../../ide/personalizing-the-visual-studio-ide.md)
- [Devenv komut satırı anahtarları](../../ide/reference/devenv-command-line-switches.md)
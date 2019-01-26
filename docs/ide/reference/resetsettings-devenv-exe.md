---
title: -ResetSettings (devenv.exe)
ms.date: 12/10/2018
ms.prod: visual-studio-dev15
ms.topic: reference
helpviewer_keywords:
- Devenv, /ResetSettings switch
- ResetSettings switch
- /ResetSettings Devenv switch
- settings [Visual Studio], resetting
ms.assetid: 1d41021c-6f58-4bd5-b122-d1c995812192
author: gewarren
ms.author: gewarren
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 50b5d977776a754a03bb8cba232369f5823ed770
ms.sourcegitcommit: 2193323efc608118e0ce6f6b2ff532f158245d56
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/25/2019
ms.locfileid: "54990244"
---
# <a name="resetsettings-devenvexe"></a>/ResetSettings (devenv.exe)

Visual Studio varsayılan ayarlarına geri yükler ve Visual Studio IDE otomatik olarak başlatır. Bu anahtar, isteğe bağlı olarak belirtilen ayarları dosyasına ayarlarını sıfırlar.

Varsayılan ayarlar, Visual Studio ilk başlatıldığında seçilen profili gelir.

> [!TIP]
> Tümleşik geliştirme ortamı (IDE) kullanarak ayarlarını sıfırlama hakkında bilgi edinmek için [ayarlarına](../environment-settings.md#reset-settings).

## <a name="syntax"></a>Sözdizimi

```shell
devenv /ResetSettings [SettingsFile|DefaultCollectionSpecifier]
```

## <a name="arguments"></a>Arguments

- *SettingsFile*

  İsteğe bağlı. Visual Studio için uygulanacak ayarları dosyasının adını ve tam yolu.

- *DefaultCollectionSpecifier*

  İsteğe bağlı. Geri yüklemek için ayar varsayılan koleksiyonunu temsil eden bir tanımlayıcı. Tabloda listelenen varsayılan koleksiyon tanımlayıcıları birini seçin.

  | Varsayılan koleksiyon adı | Koleksiyon tanımlayıcısı |
  | --- | --- |
  | **Genel** | `General` |
  | **JavaScript** | `JavaScript` |
  | **Visual Basic** | `VB` |
  | **Visual C#** | `CSharp` |
  | **Visual C++** | `VC` |
  | **Web geliştirme** | `Web` |
  | **Web geliştirme (yalnızca kod)** | `WebCode` |

## <a name="remarks"></a>Açıklamalar

Hayır ise *SettingsFile* belirtilirse, IDE mevcut ayarları kullanarak açılır.

## <a name="example"></a>Örnek

İlk örnek dosyasında depolanan ayarları uygular `MySettings.vssettings`.

İkinci örnek görsel yükler C# varsayılan profili.

```shell
devenv /resetsettings "%USERPROFILE%\MySettings.vssettings"

devenv /resetsettings CSharp
```

## <a name="see-also"></a>Ayrıca bkz.

- [Ortam ayarları](../environment-settings.md)
- [Visual Studio IDE'yi kişiselleştirme](../../ide/personalizing-the-visual-studio-ide.md)
- [Devenv komut satırı anahtarları](../../ide/reference/devenv-command-line-switches.md)
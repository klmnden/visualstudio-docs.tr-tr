---
title: -Log (devenv.exe)
ms.date: 12/12/2018
ms.topic: reference
helpviewer_keywords:
- Devenv, /Log switch
- Log switch [devenv.exe]
- /Log Devenv switch
ms.assetid: ae23c4ae-2376-4fe3-b8d2-81d34e61c8ba
author: gewarren
ms.author: gewarren
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 4b2e11cb36176aec94528019cdd19bb5fa86c92b
ms.sourcegitcommit: 21d667104199c2493accec20c2388cf674b195c3
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/08/2019
ms.locfileid: "55907223"
---
# <a name="log-devenvexe"></a>/Log (devenv.exe)

Tüm etkinliği, sorun giderme amacıyla günlük dosyasına kaydeder. Bu dosya çağırdıktan sonra görünür `devenv /log` en az bir kez. Varsayılan olarak, günlük dosyası şuradan ulaşabilirsiniz:

**% APPDATA %\\Microsoft\\VisualStudio\\**\<sürüm\>**\\ActivityLog.xml**

Burada \<sürüm\> Visual Studio sürümüdür. Ancak, farklı bir yol ve dosya adı belirtebilirsiniz.

## <a name="syntax"></a>Sözdizimi

```shell
devenv /Log NameOfLogFile
```

## <a name="arguments"></a>Arguments

- *NameOfLogFile*

  Gerekli. Tam yol ve kaydetmek için günlük dosyasının adı.

## <a name="remarks"></a>Açıklamalar

Bu anahtar, diğer tüm anahtarlardan sonra komut satırının en sonunda görünmelidir.

Günlük ile açtığınız tüm örnekleri Visual Studio için yazılır `/Log` geçin.

## <a name="example"></a>Örnek

Bu örnek için günlük yönlendirir `MyVSLog.xml` kullanıcının ana dizini dosyasında.

```shell
devenv /log "%USERPROFILE%\MyVSLog.xml"
```

## <a name="see-also"></a>Ayrıca bkz.

- [Devenv komut satırı anahtarları](../../ide/reference/devenv-command-line-switches.md)
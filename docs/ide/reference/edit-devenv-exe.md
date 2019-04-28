---
title: -Edit (devenv.exe)
ms.date: 12/10/2018
ms.topic: reference
helpviewer_keywords:
- Edit Devenv switch
- Devenv, /Edit switch
- /Edit Devenv switch
ms.assetid: 02b3d6e7-a2b1-4d83-a747-aa8c2fb758b7
author: gewarren
ms.author: gewarren
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 26433d62a68b28450a56eee1282376733acfe55c
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62838808"
---
# <a name="edit-devenvexe"></a>/Edit (devenv.exe)

Belirtilen dosya mevcut bir Visual Studio örneğini açar.

## <a name="syntax"></a>Sözdizimi

```shell
devenv /Edit [File1[ FileN]...]
```

## <a name="arguments"></a>Arguments

- *Fıle1'de*

  İsteğe bağlı. Mevcut bir Visual Studio örneğini dosyayı açın. Visual Studio örneği varsa, yeni bir örneği bir Basitleştirilmiş pencere düzeni ile oluşturulur ve aracı açılır *dosya1* yeni örneğinde.

- *Dosyan*

  İsteğe bağlı. Visual Studio'nun var olan örnekte açmak için bir veya daha fazla ek dosyalar.

## <a name="remarks"></a>Açıklamalar

Bir dosya belirtilmediğinde, mevcut bir Visual Studio örneği odağı alır. Visual Studio örneği hiçbir dosya belirtilir ve varsa aracı ile Basitleştirilmiş pencere düzenini örneği oluşturur.

Var olan bir Visual Studio örneğini kalıcı bir durumda ise, Visual Studio kalıcı çıktığında dosya var olan örnekte açılır. Örneğin, bu durum ortaya çıkabilir, [Seçenekler iletişim kutusu](../../ide/reference/options-dialog-box-visual-studio.md) açıktır.

## <a name="example"></a>Örnek

İlk örnek dosyayı açar `MyFile.cs` varolan bir Visual Studio örneğinde. Visual Studio örneği mevcut değilse, araç dosyayı yeni bir örneğinde açar. İkinci örnek, üç dosyayı yerine yalnızca bir dosya açılır dışında benzerdir.

```shell
devenv /edit MyFile.cs

devenv /edit MyFile1.cs MyFile2.cs MyFile3.cs
```

## <a name="see-also"></a>Ayrıca bkz.

- [Devenv komut satırı anahtarları](../../ide/reference/devenv-command-line-switches.md)
---
title: -LCID (devenv.exe)
ms.date: 12/10/2018
ms.topic: reference
helpviewer_keywords:
- language default
- locale IDs, setting for IDE
- Devenv, /L switch
- Devenv, /LCID switch
- locale IDs
- L Devenv switch
- /L Devenv switch
- LCID devenv switch
- /LCID Devenv switch
ms.assetid: 3a3f4e70-ea66-4351-9d62-acb1dec30e8e
author: gewarren
ms.author: gewarren
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: deb2ce5eba108127dce82bab77fe7ed4fb78fb14
ms.sourcegitcommit: 21d667104199c2493accec20c2388cf674b195c3
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/08/2019
ms.locfileid: "55947048"
---
# <a name="lcid-devenvexe"></a>/LCID (devenv.exe)

Metin, para birimi ve diğer değerleri IDE içinde kullanılan varsayılan dili ayarlar.

## <a name="syntax"></a>Sözdizimi

```shell
devenv {/LCID|/L} LocaleID
```

## <a name="arguments"></a>Arguments

- *LocaleID*

  Gerekli. Belirttiğiniz dil yerel ayar tanımlayıcısını (LCID).

## <a name="remarks"></a>Açıklamalar

IDE yükler ve ortam için varsayılan doğal dili ayarlar. Bu değişiklik oturumları arasında kalıcıdır ve bu değişikliği IDE gösterir **Araçları** > **seçenekleri** > **ortam**  >  **Uluslararası ayarlar** > **dil** kutusu.

Belirtilen dil, sisteminizde mevcut değilse `/LCID` anahtarı yok sayıldı.

Aşağıdaki tabloda LCID'ler Visual Studio tarafından desteklenen dilleri listeler.

|Dil|LCID|
|--------------|----------|
|ve|2052|
|seçenekleri yerine|1028|
|İngilizce|1033|
|Fransızca|1036|
|Almanca|1031|
|İtalyanca|1040|
|Japonca|1041|
|Korece|1042|
|İspanyolca|3082|

## <a name="example"></a>Örnek

Bu örnekte, İngilizce kaynak dizelerini IDE'ye yükler.

```shell
devenv /LCID 1033
```

## <a name="see-also"></a>Ayrıca bkz.

- [Devenv komut satırı anahtarları](../../ide/reference/devenv-command-line-switches.md)
- [Uluslararası Ayarlar, Ortam, Seçenekler İletişim Kutusu](../../ide/reference/international-settings-environment-options-dialog-box.md)
- [Pencere düzenlerini özelleştirme](../../ide/customizing-window-layouts-in-visual-studio.md)
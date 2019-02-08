---
title: -Clean (devenv.exe)
ms.date: 12/10/2018
ms.topic: reference
helpviewer_keywords:
- builds [Team System], cleaning files
- Clean Devenv switch
- /Clean Devenv switch
- Devenv, /Clean switch
ms.assetid: 79929dfd-22c9-4cec-a0d0-a16f15b8f7e4
author: gewarren
ms.author: gewarren
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 810f05b0838f27004bee983dc0acf7a3009e22a0
ms.sourcegitcommit: 21d667104199c2493accec20c2388cf674b195c3
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/08/2019
ms.locfileid: "55954016"
---
# <a name="clean-devenvexe"></a>/Clean (devenv.exe)

Tüm ara dosyaları temizler ve çıkış dizinleri.

## <a name="syntax"></a>Sözdizimi

```shell
devenv SolutionName /Clean [Config [/Project ProjName [/ProjectConfig ProjConfigName]] [/Out OutputFilename]]
```

## <a name="arguments"></a>Arguments

- *SolutionName*

  Gerekli. Çözüm dosyasının adını ve tam yolu.

- *yapılandırma*

  İsteğe bağlı. Yapılandırma (gibi `Debug` veya `Release`) adlı çözüm için Ara dosyaları temizlemek için *SolutionName*. Çözüm birden fazla platformu varsa, platform de belirtmeniz gerekir (örneğin, `Debug|Win32`). Bu bağımsız değişken belirtilmezse, ya da boş bir dize (`""`), çözümün etkin Yapılandırma Aracı'nı kullanır.

- `/Project` *ProjName*

  İsteğe bağlı. Çözüm içindeki bir proje dosyasının adı ve yolu. Projenin görünen adını veya göreli bir yol girebilirsiniz *SolutionName* proje dosyasını klasör. Ayrıca, proje dosyasının adını ve tam yolunu da girebilirsiniz.

- `/ProjectConfig` *ProjConfigName*

  İsteğe bağlı. Projenin yapı yapılandırması adı (gibi `Debug` veya `Release`) temizlenirken kullanılacak `/Project` adlı. Çözüm birden fazla platformu varsa, platform de belirtmeniz gerekir (örneğin, `Debug|Win32`). Bu anahtar belirtilirse, onu geçersiz kılar *Config* bağımsız değişken.

- `/Out` *OutputFilename*

  İsteğe bağlı. Aracı göndermek istediğiniz bir dosya adı için çıkış. Dosya zaten varsa, aracı çıkış dosyasının sonuna ekler.

## <a name="remarks"></a>Açıklamalar

Bu anahtar ile aynı işlevi mu **çözümü Temizle** IDE içinden menü komutu.

Çift tırnak içine boşluk dizeleri alın.

Temizleme ve derleme, hata da dahil olmak üzere Özet bilgileri görüntülenebilir **komut** penceresinde veya belirtilen herhangi bir günlük dosyasını [/Out](out-devenv-exe.md) geçin.

Varsa `/Project` anahtarı belirtilmediyse, Çözümdeki tüm projeleri üzerinde gerçekleştirilen bir temizleme eylem bile *FileName* bir proje dosyası olarak belirtildi.

## <a name="example"></a>Örnek

İlk örnek temizler `MySolution` çözüm dosyasında belirtilen varsayılan yapılandırma kullanarak çözümü.

İkinci örnek proje temizler `CSharpWinApp`kullanarak `Debug` içinde proje yapı yapılandırmasını `MySolution`.

```shell
devenv "%USERPROFILE%\source\repos\MySolution\MySolution.sln" /Clean

devenv "%USERPROFILE%\source\repos\MySolution\MySolution.sln" /Clean "Debug" /project "CSharpWinApp\CSharpWinApp.csproj" /projectconfig "Debug"
```

## <a name="see-also"></a>Ayrıca bkz.

- [Devenv komut satırı anahtarları](../../ide/reference/devenv-command-line-switches.md)
- [/ Derleme (devenv.exe)](../../ide/reference/build-devenv-exe.md)
- [/ Rebuild (devenv.exe)](../../ide/reference/rebuild-devenv-exe.md)
- [/ (Devenv.exe out)](../../ide/reference/out-devenv-exe.md)
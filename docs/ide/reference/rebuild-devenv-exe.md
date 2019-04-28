---
title: -Rebuild (devenv.exe)
ms.date: 12/10/2018
ms.topic: reference
helpviewer_keywords:
- Devenv, /rebuild switch
- Rebuild Devenv switch (/Rebuild)
- projects [Visual Studio], rebuilding
- /Rebuild Devenv switch
- applications [Visual Studio], rebuilding
ms.assetid: c5a8a4bf-0e2b-46eb-a44a-8aeb29b92c32
author: gewarren
ms.author: gewarren
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 44e8675b0a913873ce9b89d9d9c4ceb431dffa0d
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62945548"
---
# <a name="rebuild-devenvexe"></a>/Rebuild (devenv.exe)

Temizler ve ardından belirtilen çözüm yapılandırması oluşturur.

## <a name="syntax"></a>Sözdizimi

```shell
devenv SolutionName /Rebuild [SolnConfigName [/Project ProjName [/ProjectConfig ProjConfigName]] [/Out OutputFilename]]
```

## <a name="arguments"></a>Arguments

- *SolutionName*

  Gerekli. Çözüm dosyasının adını ve tam yolu.

- *SolnConfigName*

  İsteğe bağlı. Çözüm Yapılandırması adı (gibi `Debug` veya `Release`) adlı çözüm yeniden oluşturmak için kullanılacak *SolutionName*. Çözüm birden fazla platformu varsa, platform de belirtmeniz gerekir (örneğin, `Debug|Win32`). Bu bağımsız değişken belirtilmezse, ya da boş bir dize (`""`), çözümün etkin Yapılandırma Aracı'nı kullanır.

- `/Project` *ProjName*

  İsteğe bağlı. Çözüm içindeki bir proje dosyasının adı ve yolu. Projenin görünen adını veya göreli bir yol girebilirsiniz *SolutionName* proje dosyasını klasör. Ayrıca, proje dosyasının adını ve tam yolunu da girebilirsiniz.

- `/ProjectConfig` *ProjConfigName*

  İsteğe bağlı. Projenin yapı yapılandırması adı (gibi `Debug` veya `Release`) yeniden oluştururken kullanılacak `/Project` adlı. Çözüm birden fazla platformu varsa, platform de belirtmeniz gerekir (örneğin, `Debug|Win32`). Bu anahtar belirtilirse, onu geçersiz kılar *SolnConfigName* bağımsız değişken.

- `/Out` *OutputFilename*

  İsteğe bağlı. Aracı göndermek istediğiniz bir dosya adı için çıkış. Dosya zaten varsa, aracı çıkış dosyasının sonuna ekler.

## <a name="remarks"></a>Açıklamalar

- Bu anahtar ile aynı şeyi yapar **çözümü yeniden derle** IDE içinden menü komutu.

- Çift tırnak içine boşluk dizeleri alın.

- Temizleme ve hataları dahil olmak üzere, derleme için Özet bilgiler görüntülenebilir **komut** penceresinde veya belirtilen herhangi bir günlük dosyasını [/Out](out-devenv-exe.md) geçin.

## <a name="example"></a>Örnek

Bu örnekte, temizler ve projeyi oluşturur `CSharpWinApp`kullanarak `Debug` içinde proje yapı yapılandırmasını `MySolution`.

```shell
devenv "%USERPROFILE%\source\repos\MySolution\MySolution.sln" /rebuild Debug /project "CSharpWinApp\CSharpWinApp.csproj" /projectconfig Debug
```

## <a name="see-also"></a>Ayrıca bkz.

- [Devenv komut satırı anahtarları](../../ide/reference/devenv-command-line-switches.md)
- [/ Derleme (devenv.exe)](../../ide/reference/build-devenv-exe.md)
- [/ Clean (devenv.exe)](../../ide/reference/clean-devenv-exe.md)
- [/ (Devenv.exe out)](../../ide/reference/out-devenv-exe.md)
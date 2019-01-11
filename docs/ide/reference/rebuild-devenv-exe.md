---
title: -Rebuild (devenv.exe)
ms.date: 12/10/2018
ms.prod: visual-studio-dev15
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
manager: douge
ms.workload:
- multiple
ms.openlocfilehash: b899ca08efac05bb58cc119b7e63489c6b8934d5
ms.sourcegitcommit: 01185dadd2fa1f9a040d2a366869f1a5e1d18e0f
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/11/2019
ms.locfileid: "54227973"
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

  İsteğe bağlı. Adlı çözüm yeniden oluşturmak için kullanılacak çözüm yapılandırması adı *SolutionName*. Bu bağımsız değişken kalan, çözümün etkin Yapılandırma Aracı'nı kullanır.

- `/Project` *ProjName*

  İsteğe bağlı. Çözüm içindeki bir proje dosyasının adı ve yolu. Projenin görünen adını veya göreli bir yol girebilirsiniz *SolutionName* proje dosyasını klasör. Ayrıca, proje dosyasının adını ve tam yolunu da girebilirsiniz.

- `/ProjectConfig` *ProjConfigName*

  İsteğe bağlı. Projenin yapı yapılandırması adı yeniden oluştururken kullanılacak `/Project` adlı. Bu anahtar belirtilirse, onu geçersiz kılar *SolnConfigName* bağımsız değişken.

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
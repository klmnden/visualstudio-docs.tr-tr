---
title: -Fark (devenv.exe)
ms.date: 12/10/2018
ms.prod: visual-studio-dev15
ms.topic: reference
helpviewer_keywords:
- Devenv, /Diff switch
- /Diff Devenv switch
- Diff Devenv switch
ms.assetid: 5377fedb-632a-4e86-a947-7c11c86451e7
author: gewarren
ms.author: gewarren
manager: douge
ms.workload:
- multiple
ms.openlocfilehash: cfe0fcdb039b4c7b234f3f43e6ce5741d96f5e9c
ms.sourcegitcommit: 01185dadd2fa1f9a040d2a366869f1a5e1d18e0f
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/11/2019
ms.locfileid: "54227453"
---
# <a name="diff-devenvexe"></a>/ Diff (devenv.exe)

İki dosyayı karşılaştırır. Farklar, özel bir Visual Studio penceresinde görüntülenir.

## <a name="syntax"></a>Sözdizimi

```shell
devenv /Diff SourceFile TargetFile [SourceDisplayName [TargetDisplayName]]
```

## <a name="arguments"></a>Arguments

- *Kaynakdosya*

  Gerekli. Karşılaştırılacak ilk dosya adını ve tam yolu.

- *Hedefdosya*

  Gerekli. Karşılaştırılacak ikinci dosyasının adını ve tam yolu.

- *SourceDisplayName*

  İsteğe bağlı. İlk dosya görünen adı.

- *TargetDisplayName*

  İsteğe bağlı. İkinci dosyanın görünen adı.
    
## <a name="remarks"></a>Açıklamalar

IDE örneği zaten açık değilse, dosya karşılaştırma geçerli IDE'de bir sekmede görünür.

## <a name="example"></a>Örnek

İlk örnek, kullanıcıların görünen adlarını değiştirmeden iki dosyayı karşılaştırır. İkinci örnek, her iki ekran adlarına değiştirilirken dosyaları karşılaştırır. Üçüncü ve dördüncü örnekler, iki dosyayı Karşılaştır ancak bir diğer ad yalnızca ilk veya ikinci dosyasını için geçerlidir.

```shell
devenv /diff File1.txt File2.txt

devenv /diff File1.txt File2.txt FirstAlias "Second Alias"

devenv /diff File1.txt File2.txt "File One"

devenv /diff File1.txt File2.txt "" FileTwo
```

## <a name="see-also"></a>Ayrıca bkz.

- [Devenv komut satırı anahtarları](../../ide/reference/devenv-command-line-switches.md)

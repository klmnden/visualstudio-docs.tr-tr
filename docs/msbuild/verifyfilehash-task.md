---
title: VerifyFileHash görevi | Microsoft Docs
ms.date: 01/28/2019
ms.topic: reference
dev_langs:
- VB
- CSharp
- C++
- jsharp
helpviewer_keywords:
- VerifyFileHash task [MSBuild]
- MSBuild, VerifyFileHash task
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 3acdaabffc35122616cced4113abbc5a43beb9a1
ms.sourcegitcommit: 16175e0cea6af528e9ec76f0b94690faaf1bed30
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/28/2019
ms.locfileid: "71481968"
---
# <a name="verifyfilehash-task"></a>VerifyFileHash görevi

Bir dosyanın beklenen dosya karmasıyla eşleştiğini doğrular.

Bu görev 15,8 ' ye eklenmiştir, ancak 16,0 ' nin altındaki MSBuild sürümleri için kullanmak üzere [geçici bir çözüm](https://github.com/Microsoft/msbuild/pull/3999#issuecomment-458193272) gerektirir.

## <a name="task-parameters"></a>Görev parametreleri

 Aşağıdaki tablo, `VerifyFileHash` görevin parametrelerini açıklar.

|Parametre|Açıklama|
|---------------|-----------------|
|`File`|Gerekli `String` parametre.<br /><br />Karma hale getirilen ve doğrulanacak dosya.|
|`Hash`|Gerekli `String` parametre.<br /><br />Dosyanın beklenen karması.|
|`Algorithm`|İsteğe `String` bağlı parametre.<br /><br />Algoritma. İzin verilen değerler: `SHA256`, `SHA384`, `SHA512`. Varsayılan = `SHA256`.|
|`HashEncoding`|İsteğe `String` bağlı parametre.<br /><br />Oluşturulan karmaları için kullanılacak kodlama. Varsayılan olarak `hex`. İzin verilen değerler = `hex`, `base64`.|

## <a name="example"></a>Örnek

Aşağıdaki örnek, kendi sağlama toplamını doğrulamak için `VerifyFileHash` görevini kullanır.

```xml
<Project>
  <Target Name="VerifyHash">
    <GetFileHash Files="$(MSBuildProjectFullPath)">
      <Output
          TaskParameter="Items"
          ItemName="FilesWithHashes" />
    </GetFileHash>

    <Message Importance="High"
             Text="@(FilesWithHashes->'%(Identity): %(FileHash)')" />

    <VerifyFileHash File="$(MSBuildThisFileFullPath)"
                    Hash="$(ExpectedHash)" />
  </Target>
</Project>
```

## <a name="see-also"></a>Ayrıca bkz.

- [Görevler](../msbuild/msbuild-tasks.md)
- [Görev başvurusu](../msbuild/msbuild-task-reference.md)
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
ms.openlocfilehash: 2e7330e750d0f636979f52eacf398ca7d496c523
ms.sourcegitcommit: 689ba54ea14257d13031de881f5d4fe937a36f56
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/27/2019
ms.locfileid: "71342413"
---
# <a name="verifyfilehash-task"></a>VerifyFileHash görevi

Bir dosyanın beklenen dosya karmasıyla eşleştiğini doğrular.

Bu görev 15,8 ' ye eklenmiştir, ancak 16,0 ' nin altındaki MSBuild sürümleri için kullanmak üzere [geçici bir çözüm](https://github.com/Microsoft/msbuild/pull/3999#issuecomment-458193272) gerektirir.

## <a name="task-parameters"></a>Görev parametreleri

 Aşağıdaki tablo, `VerifyFileHash` görevin parametrelerini açıklar.

|Parametre|Açıklama|
|---------------|-----------------|
|`File`|Gerekli <xref:Microsoft.Build.Framework.ITaskItem> parametre.<br /><br />Karma hale getirilen ve doğrulanacak dosyalar.|
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
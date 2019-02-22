---
title: VerifyFileHash görev | Microsoft Docs
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
ms.openlocfilehash: faf7738019680085020b9650094931d5860bc29b
ms.sourcegitcommit: d0425b6b7d4b99e17ca6ac0671282bc718f80910
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/21/2019
ms.locfileid: "56618386"
---
# <a name="verifyfilehash-task"></a>VerifyFileHash görevi

Bir dosyanın beklenen dosya karması eşleştiğini doğrular.

Bu görevi, içinde 15,8 eklendi, ancak gerektiren bir [geçici çözüm](https://github.com/Microsoft/msbuild/pull/3999#issuecomment-458193272) 16,0 altındaki MSBuild sürümleri için kullanılacak.

## <a name="task-parameters"></a>Görev parametreleri

 Parametreleri aşağıdaki tabloda açıklanmıştır `VerifyFileHash` görev.

|Parametre|Açıklama|
|---------------|-----------------|
|`File`|Gerekli <xref:Microsoft.Build.Framework.ITaskItem> parametresi.<br /><br />Karma çözülemediğinden ve dosyaları.|
|`Hash`|Gerekli `String` parametresi.<br /><br />Dosyanın beklenen karma değeri.|
|`Items`|<xref:Microsoft.Build.Framework.ITaskItem>`[]` Çıkış parametresi.<br /><br />`Files` Ek meta veri kümesi için dosya karması ile giriş.|
|`Algorithm`|İsteğe bağlı `String` parametresi.<br /><br />Algoritma. İzin verilen değerler: `SHA256`, `SHA384`, `SHA512`. Varsayılan = `SHA256`.|
|`HashEncoding`|İsteğe bağlı `String` parametresi.<br /><br />İçin kullanılacak kodlama karmaları oluşturulur. Varsayılan olarak `hex`. İzin verilen değerler = `hex`, `base64`.|

## <a name="example"></a>Örnek

Aşağıdaki örnekte `VerifyFileHash` görev kendi sağlama toplamı doğrulanamadı.

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
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
ms.openlocfilehash: b8122f1a3869efe32d7ae35ff05cdbb77ad84375
ms.sourcegitcommit: e3d96b20381916bf4772f9db52b22275763bb603
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/31/2019
ms.locfileid: "55484892"
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

[Görevler](../msbuild/msbuild-tasks.md)

[Görev başvurusu](../msbuild/msbuild-task-reference.md)
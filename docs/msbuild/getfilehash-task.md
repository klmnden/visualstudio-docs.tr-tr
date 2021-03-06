---
title: GetFileHash görev | Microsoft Docs
ms.date: 01/28/2019
ms.topic: reference
dev_langs:
- VB
- CSharp
- C++
- jsharp
helpviewer_keywords:
- GetFileHash task [MSBuild]
- MSBuild, GetFileHash task
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: ab5da58b125f86627d54547bd9f6f7cddc16c4de
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62977509"
---
# <a name="getfilehash-task"></a>GetFileHash görevi

Bir dosyanın içeriğini veya dosya kümesini sağlama toplamlarını hesaplar.

Bu görevi, içinde 15,8 eklendi, ancak gerektiren bir [geçici çözüm](https://github.com/Microsoft/msbuild/pull/3999#issuecomment-458193272) 16,0 altındaki MSBuild sürümleri için kullanılacak.

## <a name="task-parameters"></a>Görev parametreleri

 Parametreleri aşağıdaki tabloda açıklanmıştır `GetFileHash` görev.

|Parametre|Açıklama|
|---------------|-----------------|
|`Files`|Gerekli <xref:Microsoft.Build.Framework.ITaskItem>`[]` parametresi.<br /><br />Karma hale getirilecek dosyaları.|
|`Items`|<xref:Microsoft.Build.Framework.ITaskItem>`[]` Çıkış parametresi.<br /><br />`Files` Ek meta veri kümesi için dosya karması ile giriş.|
|`Hash`|`String` Çıkış parametresi.<br /><br />Dosya karması. Bu çıkış, yalnızca geçirilen tam olarak bir öğe varsa ayarlanır.|
|`Algorithm`|İsteğe bağlı `String` parametresi.<br /><br />Algoritma. İzin verilen değerler: `SHA256`, `SHA384`, `SHA512`. Varsayılan = `SHA256`.|
|`MetadataName`|İsteğe bağlı `String` parametresi.<br /><br />Her öğe, karma depolandığı meta veri adı. Varsayılan olarak `FileHash`.|
|`HashEncoding`|İsteğe bağlı `String` parametresi.<br /><br />İçin kullanılacak kodlama karmaları oluşturulur. Varsayılan olarak `hex`. İzin verilen değerler = `hex`, `base64`.|

## <a name="example"></a>Örnek

Aşağıdaki örnekte `GetFileHash` belirlemek ve sağlama toplamı, yazdırmak için görev `FilesToHash` öğeleri.

```xml
<Project>
  <ItemGroup>
    <FilesToHash Include="$(MSBuildThisFileDirectory)\*" />
  </ItemGroup>
  <Target Name="GetHash">
    <GetFileHash Files="@(FilesToHash)">
      <Output
          TaskParameter="Items"
          ItemName="FilesWithHashes" />
    </GetFileHash>

    <Message Importance="High"
             Text="@(FilesWithHashes->'%(Identity): %(FileHash)')" />
  </Target>
</Project>
```

## <a name="see-also"></a>Ayrıca bkz.

- [Görevler](../msbuild/msbuild-tasks.md)

- [Görev başvurusu](../msbuild/msbuild-task-reference.md)
---
title: XmlPoke görevi | Microsoft Docs
ms.date: 11/04/2016
ms.topic: reference
dev_langs:
- VB
- CSharp
- C++
- jsharp
helpviewer_keywords:
- XmlPoke task [MSBuild]
- MSBuild, XmlPoke task
ms.assetid: 6ba1953c-be3b-4df8-8561-e133408f8270
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 6eb87a279da834004e599a49b33d0c1b32355269
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62777622"
---
# <a name="xmlpoke-task"></a>XmlPoke görevi

Bir XML dosyasına bir XPath sorgusu tarafından belirtilen değerleri ayarlar.

## <a name="parameters"></a>Parametreler

 Parametreleri aşağıdaki tabloda açıklanmıştır `XmlPoke` görev.

|Parametre|Açıklama|
|---------------|-----------------|
|`Namespaces`|İsteğe bağlı `String` parametresi.<br /><br /> XPath sorgusu ön ekleri için ad alanlarını belirtir. `Namespaces` olan oluşan bir XML kod parçacığı `Namespace` öznitelikleri öğelerle `Prefix` ve `Uri`. Öznitelik `Prefix` önek belirtilen ad alanı ile ilişkilendirilecek belirtir `Uri` özniteliği. Boş bir kullanmayın `Prefix`.|
|`Query`|İsteğe bağlı `String` parametresi.<br /><br /> XPath sorgusu belirtir.|
|`Value`|Gerekli <xref:Microsoft.Build.Framework.ITaskItem> parametresi.<br /><br /> Belirtilen yola eklenmesi için kullanılacak değeri belirtir.|
|`XmlInputPath`|İsteğe bağlı <xref:Microsoft.Build.Framework.ITaskItem> parametresi.<br /><br /> XML Giriş bir dosya yolu belirtir.|

## <a name="remarks"></a>Açıklamalar

 Tabloda listelenen parametreleri sahip olmaya ek olarak, bu görev parametreleri devralan <xref:Microsoft.Build.Tasks.TaskExtension> kendisi sınıfının devraldığı <xref:Microsoft.Build.Utilities.Task> sınıfı. Bu ek parametrelerin ve Tanımlamaların bir listesi için bkz. [TaskExtension taban sınıfı](../msbuild/taskextension-base-class.md).

## <a name="example"></a>Örnek

Bir örnek.XML değiştirmek için şu şekildedir:

```xml
<Package xmlns="http://schemas.microsoft.com/appx/manifest/foundation/windows10"
         xmlns:mp="http://schemas.microsoft.com/appx/2014/phone/manifest"
         xmlns:uap="http://schemas.microsoft.com/appx/manifest/uap/windows10" >
<Identity Name="Sample.Product " Publisher="CN=1234" Version="1.0.0.0" />
<mp:PhoneIdentity PhoneProductId="456" PhonePublisherId="0" />
</Package>
```

Bu örnekte, değişiklik yapmak istiyorsanız `/Package/mp:PhoneIdentity/PhonePublisherId`, ardından kullanın

```xml
<Project xmlns="http://schemas.microsoft.com/developer/msbuild/2003">
  <PropertyGroup>
    <Namespace>
        <Namespace Prefix="dn" Uri="http://schemas.microsoft.com/appx/manifest/foundation/windows10" />
        <Namespace Prefix="mp" Uri="http://schemas.microsoft.com/appx/2014/phone/manifest" />
        <Namespace Prefix="uap" Uri="http://schemas.microsoft.com/appx/manifest/uap/windows10" />
    </Namespace>
</PropertyGroup>

<Target Name="Poke">
  <XmlPoke
    XmlInputPath="Sample.xml"
    Value="MyId"
    Query="/dn:Package/mp:PhoneIdentity/@PhoneProductId"
    Namespaces="$(Namespace)"/>
</Target>
</Project>
```

`dn` Burada bir yapay ad alanı öneki varsayılan ad alanı için kullanılır.

## <a name="see-also"></a>Ayrıca bkz.

- [Görevler](../msbuild/msbuild-tasks.md)
- [Görev başvurusu](../msbuild/msbuild-task-reference.md)

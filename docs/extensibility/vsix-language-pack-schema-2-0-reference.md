---
title: VSıX dil paketi şeması 2,0 başvurusu | Microsoft Docs
ms.date: 10/26/2017
ms.topic: conceptual
helpviewer_keywords:
- language pack
- localize vsix
- localize package
- localize extension
ms.assetid: 2a2932bc-cdbe-4d32-91fa-a3e0474f9098
ms.author: zorio
author: zoeyr
manager: jillfra
ms.openlocfilehash: fe6d4bd9e82950d77925dda1560b5c204633d392
ms.sourcegitcommit: dae5dfd626277b58ebd7b21a75757f683f1eacc5
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/06/2019
ms.locfileid: "70739324"
---
# <a name="vsix-language-pack-schema-20-reference"></a>VSıX dil paketi şeması 2,0 başvurusu

VSıX dil paketi şeması, VSıX paketleri için yerelleştirilmiş yükleme bilgilerini sağlar. Bu şemanın sürüm 2,0, ek yerelleştirme öğelerini destekler.

## <a name="language-pack-schema"></a>Dil paketi şeması

Dil paketi dosyasının kök öğesi, dil paketi biçiminin `<PackageLanguagePackManifest>`sürümü olan öğesinin `Version`bir özniteliğiyle birlikte bulunur. Bu makalede, `Version` özniteliği değere `Version="2.0.0"`ayarlanarak bildirimde belirtilen dil paketi biçiminin 2,0 sürümü açıklanır. Kök öğesi tam olarak bir alt `<Metadata>` öğe içeriyor.

### <a name="packagelanguagepackmanifest-element"></a>PackageLanguagePackManifest öğesi

`<PackageLanguagePackManifest>` Öğesi içinde aşağıdaki öğe var olmalıdır:

|Başlık|Açıklama|
|-----------|-----------------|
|`<Metadata>`| Tüm yerelleştirilmiş paket meta verileri için kapsayan öğe

### <a name="metadata-element"></a>Metadata öğesi

`<Metadata>` Öğesi içinde aşağıdaki öğelere sahip olabilirsiniz:

|Başlık|Açıklama|
|-----------|-----------------|
|`<DisplayName>`|Yüklenecek uzantının yerelleştirilmiş adı|
|`<Description>`|Yüklenecek uzantının yerelleştirilmiş açıklaması|
|`<License>`| Uzantının lisansının yerelleştirilmiş bir sürümünün yolu|
|`<MoreInfo>`| Uzantı ile ilgili yerelleştirilmiş bilgilere bir bağlantı|
|`<ReleaseNotes>`| Sürüm notlarının yerelleştirilmiş bir sürümüne yol veya bağlantı|
|`<Icon>`| Uzantılar simgesinin yerelleştirilmiş bir sürümünün yolu|

### <a name="sample-manifest"></a>Örnek bildirim

```xml
<?xml version="1.0" encoding="utf-8"?>
<PackageLanguagePackManifest Version="2.0.0" xmlns="http://schemas.microsoft.com/developer/vsx-schema/2011">
  <Metadata>
    <DisplayName>Arbol de Familia</LocalizedName>
    <Description> Esta extensión pone control personalizado en la caja de herramientas por manejar información de familia.</Description>
    <MoreInfo> http://www.contoso.com/products/es/ArbolDeFamilia.htm</MoreInfo>
    <License>Eula.rtf</License>
    <ReleaseNotes>ReleaseNotes.rtf</ReleaseNotes>
    <Icon>Icon.png</Icon>
  </Metadata>
</PackageLanguagePackManifest>
```

## <a name="see-also"></a>Ayrıca bkz.

|Başlık|Açıklama|
|-----------|-----------------|
|[VSıX paketlerini yerelleştirme](../extensibility/localizing-vsix-packages.md)|Bir VSıX paketi için yerelleştirilmiş yükleme desteğinin nasıl sağlanması gerektiğini gösterir.|
|[VSıX uzantı Şeması 2,0 başvurusu](../extensibility/vsix-extension-schema-2-0-reference.md)|VSıX bildirimi bir *. VSIX* dağıtım dosyasının içeriğini açıklar. Dağıtım dosyası, **Uzantılar ve güncelleştirmeler** iletişim kutusunu kullanarak bir Visual Studio uzantısı yüklemenizi sağlar.|
|[Visual Studio uzantıları bulma ve kullanma](../ide/finding-and-using-visual-studio-extensions.md)|Uzantılar **ve güncelleştirmeler** iletişim kutusunun uzantıları yüklemek, kaldırmak, etkinleştirmek ve devre dışı bırakmak için nasıl kullanılacağını gösterir.|

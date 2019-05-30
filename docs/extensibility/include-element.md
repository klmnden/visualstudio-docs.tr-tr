---
title: Öğe dahil | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
f1_keywords:
- Include
helpviewer_keywords:
- Include element (VSCT XML schema)
- VSCT XML schema elements, Include
ms.assetid: c923dfe6-084a-4105-aec1-f0a3f8399c54
author: madskristensen
ms.author: madsk
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: 7287f4e8b611f55ea28e648aec3f95d1407bf07e
ms.sourcegitcommit: 40d612240dc5bea418cd27fdacdf85ea177e2df3
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/29/2019
ms.locfileid: "66350105"
---
# <a name="include-element"></a>Öğe Ekle
INCLUDE öğesi bulunabilir dosyayı belirtir. sağlanan üzerinde geçerli dosyasına ekleme yolu ekleyin.  Tüm semboller ve tanımlanan türleri derlenen sonuçtaki bir parçası olur.

## <a name="syntax"></a>Sözdizimi

```csharp
<Include href="stdidcmd.h" />
```

## <a name="attributes-and-elements"></a>Öznitelikler ve öğeler
 Öznitelikler, alt ve üst öğeler aşağıdaki bölümlerde açıklanmaktadır.

### <a name="attributes"></a>Öznitelikler

|Öznitelik|Açıklama|
|---------------|-----------------|
|href|Gerekli. Üstbilgi dosyası yolu:<br /><br /> href="stdidcmd.h"|
|Koşul|İsteğe bağlı. Bkz: [koşullu öznitelikler](../extensibility/vsct-xml-schema-conditional-attributes.md).|

### <a name="child-elements"></a>Alt öğeleri

|Öğe|Açıklama|
|-------------|-----------------|
|Yok.|Yok.|

### <a name="parent-elements"></a>Üst öğeler

|Öğe|Açıklama|
|-------------|-----------------|
|[CommandTable öğesi](../extensibility/commandtable-element.md)|Tüm komutları temsil eden öğeler tanımlar — diğer bir deyişle, menü öğeleri, menüler, araç çubukları ve birleşik giriş kutuları — IDE'ye VSPackage sağlayan.|

## <a name="example"></a>Örnek

```
<Include href="PackagePlacements.vsct"/>
```

## <a name="see-also"></a>Ayrıca bkz.
- [Visual Studio komut tablosu (.vsct) dosyaları](../extensibility/internals/visual-studio-command-table-dot-vsct-files.md)
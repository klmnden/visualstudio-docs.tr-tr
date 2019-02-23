---
title: VisibilityConstraints öğesi | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
f1_keywords:
- VisibilityConstraints
helpviewer_keywords:
- VSCT XML schema elements, VisibilityConstraints
- VisibilityConstraints element (VSCT XML schema)
ms.assetid: d6dcd314-6fe4-4693-a189-91fa026c7b34
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: 6c567291f2b91e092afecb264c2b2e0ca1bfd108
ms.sourcegitcommit: b0d8e61745f67bd1f7ecf7fe080a0fe73ac6a181
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/22/2019
ms.locfileid: "56702583"
---
# <a name="visibilityconstraints-element"></a>VisibilityConstraints öğesi
VisibilityConstraints öğesi gruplarını komutları ve araç çubukları statik görünürlüğünü belirler. Görünürlük varsayılan tarafından denetlenir [!INCLUDE[vsprvs](../code-quality/includes/vsprvs_md.md)] VSPackage yükleme olmadan tümleşik geliştirme ortamı (IDE).

## <a name="syntax"></a>Sözdizimi

```xml
<VisibilityConstraints>
  <VisibilityConstraint>... </VisibilityConstraint>
  <VisibilityConstraint>... </VisibilityConstraint>
</VisibilityConstraint>
```

## <a name="attributes-and-elements"></a>Öznitelikler ve öğeler
 Öznitelikler, alt ve üst öğeler aşağıdaki bölümlerde açıklanmaktadır.

### <a name="attributes"></a>Öznitelikler

|Öznitelik|Açıklama|
|---------------|-----------------|
|Koşul|İsteğe bağlı. Bkz: [koşullu öznitelikler](../extensibility/vsct-xml-schema-conditional-attributes.md).|

### <a name="child-elements"></a>Alt öğeleri

|Öğe|Açıklama|
|-------------|-----------------|
|[Visibilityıtem öğesi](../extensibility/visibilityitem-element.md)|Komutlar ve araç çubukları statik görünürlüğünü belirler.|
|[VisibilityConstraints](../extensibility/visibilityconstraints-element.md)|Komutlar ve araç çubukları grupları statik görünürlüğünü belirler.|

### <a name="parent-elements"></a>Üst öğeler

|Öğe|Açıklama|
|-------------|-----------------|
|[CommandTable öğesi](../extensibility/commandtable-element.md)|VSPackage sunar IDE'nin komutlarını (örneğin, menü öğeleri, menüler, araç çubukları ve birleşik giriş kutuları) temsil eden tüm öğeleri tanımlar.|

## <a name="example"></a>Örnek

```xml
<VisibilityConstraints>
  <VisibilityItem guid="cmdSetGuidMyProductCommands"     id="cmdidAddWidget"
    context="guidNotViewSourceMode"/>
</VisibilityConstraints>
```

## <a name="see-also"></a>Ayrıca bkz.
- [Visibilityıtem öğesi](../extensibility/visibilityitem-element.md)
- [Visual Studio komut tablosu (. Vsct) dosyaları](../extensibility/internals/visual-studio-command-table-dot-vsct-files.md)
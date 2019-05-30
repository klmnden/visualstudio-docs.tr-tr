---
title: CommandPlacement öğesi | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
helpviewer_keywords:
- CommandPlacements element (VSCT XML schema)
- VSCT XML schema elements, CommandPlacements
ms.assetid: 2cbd7ac8-c55a-43d8-a26d-713b3d790016
author: madskristensen
ms.author: madsk
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: 3c43dab922d51d2d3f96ffaba0ef24f8f0e18fa1
ms.sourcegitcommit: 40d612240dc5bea418cd27fdacdf85ea177e2df3
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/29/2019
ms.locfileid: "66341878"
---
# <a name="commandplacement-element"></a>CommandPlacement öğesi
CommandPlacement öğesi düğmeler, grupları ve menüler birden fazla grup veya menüdeki dahil edilmesini sağlar. CommandPlacement öğesi kullanarak tam bir kullanıcı arabirimi görünümünü değiştirmek için bu öğeleri bulunabileceğini gerekmez.

 Daha fazla bilgi için [yeniden kullanılabilir düğme grupları oluşturma](../extensibility/creating-reusable-groups-of-buttons.md).

## <a name="syntax"></a>Sözdizimi

```
<CommandPlacement guid="guidMyCommandSet" id="MyCommand" priority="0x001" >
  <Parent>... </Parent>
</CommandPlacement>
```

## <a name="attributes-and-elements"></a>Öznitelikler ve öğeler
 Öznitelikler, alt ve üst öğeler aşağıdaki bölümlerde açıklanmaktadır.

### <a name="attributes"></a>Öznitelikler

|Öznitelik|Açıklama|
|---------------|-----------------|
|GUID|Gerekli. Sınıfında tanımlandığı gibi komut kümesi GUID'si [Symbols öğesi](../extensibility/symbols-element.md).|
|kimlik|Gerekli. Menü, Grup veya sınıfında tanımlandığı gibi yerleştirilmesini komut kimliğini `Symbols Element`.|
|öncelik|Gerekli. Üst öğesi görsel öğe konumunu belirler.|
|Koşul|İsteğe bağlı. Bkz: [koşullu Aattributes](../extensibility/vsct-xml-schema-conditional-attributes.md).|

### <a name="child-elements"></a>Alt öğeleri

|Öğe|Açıklama|
|-------------|-----------------|
|Üst öğe|Gerekli. Menü veya yerleştirilecek öğesi barındıran grup.|

### <a name="parent-elements"></a>Üst Öğeler

|Öğe|Açıklama|
|-------------|-----------------|
|[CommandPlacements öğesi](../extensibility/commandplacements-element.md)|CommandPlacements ve CommandPlacement öğelerin grupları belirtir.|

## <a name="example"></a>Örnek

```
<CommandPlacements>
  <CommandPlacement guid="guidWidgetPackage" id="cmdidInsertOptions"
    priority="0x0300">
    <Parent guid="cmdGuidWidgetCommands" id="menuIDEditWidget"/>
  </CommandPlacement>
</CommandPlacements>
```

## <a name="see-also"></a>Ayrıca bkz.
- [CommandPlacements öğesi](../extensibility/commandplacements-element.md)
- [Visual Studio komut tablosu (.vsct) dosyaları](../extensibility/internals/visual-studio-command-table-dot-vsct-files.md)

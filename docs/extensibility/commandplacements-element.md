---
title: CommandPlacements öğesi | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
f1_keywords:
- CommandPlacements
helpviewer_keywords:
- CommandPlacements element (VSCT XML schema)
- VSCT XML schema elements, CommandPlacements
ms.assetid: 78a5724a-3b9f-4c78-9c0d-8faa3924f81c
author: madskristensen
ms.author: madsk
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: bb22359c936caacef81f4c9b81993a46d47ccc0b
ms.sourcegitcommit: 40d612240dc5bea418cd27fdacdf85ea177e2df3
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/29/2019
ms.locfileid: "66341892"
---
# <a name="commandplacements-element"></a>CommandPlacements öğesi
CommandPlacements öğesi CommandPlacement öğeleri ve diğer CommandPlacements gruplandırmaları gruplandırır.

 CommandPlacements öğesi isteğe bağlıdır. Hiçbir komut, grupları veya menüler, ikincil bir konumda eklenmelidir, bu bölümde eklemek gerekmez, *.vsct* dosya.

## <a name="syntax"></a>Sözdizimi

```xml
<CommandPlacements>
  <CommandPlacement>... </CommandPlacement>
  <CommandPlacement>... </CommandPlacement>
</CommandPlacements>
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
|CommandPlacements|CommandPlacement öğeleri gruplandırır ve diğer CommandPlacements gruplandırmaları.|
|[CommandPlacement öğesi](../extensibility/commandplacement-element.md)|Düğmeler, grupları ve menüler birden fazla grup veya menüdeki dahil edilmesini sağlar.|

### <a name="parent-elements"></a>Üst öğeler

|Öğe|Açıklama|
|-------------|-----------------|
|[CommandTable öğesi](../extensibility/commandtable-element.md)|Komutları temsil eden tüm öğeleri tanımlar.|

## <a name="example"></a>Örnek

```xml
<CommandPlacements>
  <CommandPlacement guid="guidWidgetPackage" id="cmdidInsertOptions"
    priority="0x0300">
    <Parent guid="cmdGuidWidgetCommands" id="menuIDEditWidget"/>
  </CommandPlacement>
</CommandPlacements>
```

## <a name="see-also"></a>Ayrıca bkz.
- [CommandPlacement öğesi](../extensibility/commandplacement-element.md)
- [Visual Studio komut tablosu (.vsct) dosyaları](../extensibility/internals/visual-studio-command-table-dot-vsct-files.md)
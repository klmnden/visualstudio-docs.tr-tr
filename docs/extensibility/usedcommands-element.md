---
title: UsedCommands öğesi | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
f1_keywords:
- UsedCommands
helpviewer_keywords:
- UsedCommands element (VSCT XML schema)
- VSCT XML schema elements, UsedCommands
ms.assetid: 5e000ee0-a919-46e9-9277-2a0659f1eb78
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: e951776df807cae1b66cbc3564b9ee7a3d0165ae
ms.sourcegitcommit: b0d8e61745f67bd1f7ecf7fe080a0fe73ac6a181
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/22/2019
ms.locfileid: "56699866"
---
# <a name="usedcommands-element"></a>UsedCommands Öğesi
UsedCommands öğesi UsedCommand öğeleri ve diğer UsedCommands gruplandırmaları gruplandırır.

 UsedCommands öğesi isteğe bağlıdır. Paketiniz dışında tanımlanan komutları çağırmayın, bu bölümde .vsct dosyanıza dahil gerekmez.

## <a name="syntax"></a>Sözdizimi

```
<UsedCommands condition="Defined(DEBUG)">
  <UsedCommand ... />
</UsedCommands>
```

## <a name="attributes-and-elements"></a>Öznitelikler ve Öğeler
 Öznitelikler, alt ve üst öğeler aşağıdaki bölümlerde açıklanmaktadır.

### <a name="attributes"></a>Öznitelikler

|Öznitelik|Açıklama|
|---------------|-----------------|
|Koşul|İsteğe bağlı. Bkz: [koşullu öznitelikler](../extensibility/vsct-xml-schema-conditional-attributes.md).|

### <a name="child-elements"></a>Alt Öğeler

|Öğe|Açıklama|
|-------------|-----------------|
|[UsedCommand Öğesi](../extensibility/usedcommand-element.md)|Başka kod tarafından uygulanan komutu.|

### <a name="parent-elements"></a>Üst Öğeler

|Öğe|Açıklama|
|-------------|-----------------|
|[CommandTable Öğesi](../extensibility/commandtable-element.md)|VSPackage sağlayan komutlar (örneğin, menü öğeleri, menüler, araç çubukları ve birleşik giriş kutuları) tümleşik geliştirme ortamı (IDE) temsil eden tüm öğeleri tanımlar.|

## <a name="example"></a>Örnek

```
<UsedCommands>
  <UsedCommand guid="guidVSStd97" id="cmdidCut"/>
  <UsedCommand guid="guidVSStd97" id="cmdidCopy"/>
  <UsedCommand guid="guidVSStd97" id="cmdidPaste"/>
</UsedCommands>
```

## <a name="see-also"></a>Ayrıca Bkz.
- [UsedCommand Öğesi](../extensibility/usedcommand-element.md)
- [Visual Studio Komut Tablosu (.Vsct) Dosyaları](../extensibility/internals/visual-studio-command-table-dot-vsct-files.md)
---
title: Button öğesi | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
helpviewer_keywords:
- Buttons element (VSCT XML schema)
- VSCT XML schema elements, Buttons
ms.assetid: 96dccf51-2b00-4700-9d28-924b34c21ecd
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: 1e62436d32d85c76685c86ea0da396dacae1bf3f
ms.sourcegitcommit: b0d8e61745f67bd1f7ecf7fe080a0fe73ac6a181
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/22/2019
ms.locfileid: "56694276"
---
# <a name="button-element"></a>Button öğesi
Kullanıcının etkileşime geçtiği bir öğe tanımlar. Düğmeler, farklı türde olabilir: Düğme, MenuButton ve SplitDropDown.

## <a name="syntax"></a>Sözdizimi

```
<Button guid="guidMyCommandSet" id="MyCommand" priority="0x102" type="button">
  <Parent>... </Parent>
  <Icon>... </Icon>
  <CommandFlag>... </CommandFlag>
  <Strings>... </Strings>
</Button>
```

## <a name="attributes-and-elements"></a>Öznitelikler ve öğeler
 Öznitelikler, alt ve üst öğeler aşağıdaki bölümlerde açıklanmaktadır.

### <a name="attributes"></a>Öznitelikler

|Öznitelik|Açıklama|
|---------------|-----------------|
|GUID|Gerekli. GUID/ID komut tanımlayıcısı GUİD'si.|
|kimlik|Gerekli. Kimliği bir GUID/ID komut tanımlayıcısı.|
|öncelik|İsteğe bağlı. Bir sayısal değer yönelik önceliği belirtir.|
| türü|İsteğe bağlı. Düğme türünü belirten bir numaralandırılmış değeri.<br /><br /> Belirtilmemişse, düğme kullanır.<br /><br /> Düğme<br /> Araç çubuklarında (genellikle icon bir düğme olarak), menüler ve bağlam menüleri görünür bir standart komutu.<br /><br /> MenuButton<br /> Komut yürütme değil, ancak başka bir menü üreten bir menü öğesi.<br /><br /> SplitDropDown<br /> Microsoft Word standart araç çubuğundaki Geri Al ve Yinele düğmeler gibi denetimler.|
|Koşul|İsteğe bağlı. Bkz: [koşullu öznitelikler](../extensibility/vsct-xml-schema-conditional-attributes.md).|

### <a name="child-elements"></a>Alt Öğeler

|Öğe|Açıklama|
|-------------|-----------------|
|[Üst öğe](../extensibility/parent-element.md)|İsteğe bağlı. Düğmenin üst öğe.|
|[Icon öğesi](../extensibility/icon-element.md)|İsteğe bağlı. Düğme ile ilişkili simge.|
|[Command flag öğesi](../extensibility/command-flag-element.md)|Gerekli. Bir düğme için geçerli CommandFlag değerler aşağıdaki gibidir.<br /><br /> -AllowParams<br /><br /> - CommandWellOnly<br /><br /> -DefaultDisabled<br /><br /> -DefaultInvisible<br /><br /> - DontCache<br /><br /> -DynamicItemStart<br /><br /> -DynamicVisibility<br /><br /> -FixMenuController<br /><br /> -IconAndText<br /><br /> -NoButtonCustomize<br /><br /> -NoCustomize<br /><br /> -NoKeyCustomize<br /><br /> - NoShowOnMenuController<br /><br /> -PICT<br /><br /> - PostExec<br /><br /> - ProfferedCmd<br /><br /> - RouteToDocs<br /><br /> - TextCascadeUseBtn<br /><br /> - TextMenuUseButton<br /><br /> -TextChanges<br /><br /> - TextChangesButton<br /><br /> - TextContextUseButton<br /><br /> - TextMenuCtrlUseMenu<br /><br /> - TextMenuUseButton<br /><br /> - TextOnly|
|[Strings öğesi](../extensibility/strings-element.md)|Gerekli. Alt [ButtonText öğesi](../extensibility/buttontext-element.md) tanımlanması gerekir.|
|Ek Açıklama|İsteğe bağlı bir açıklama.|

### <a name="parent-elements"></a>Üst öğeler

|Öğe|Açıklama|
|-------------|-----------------|
|[Buttons öğesi](../extensibility/buttons-element.md)|Düğme öğelerini gruplandırır.|

## <a name="example"></a>Örnek
 Aşağıdaki örnek, bir düğme olarak tanımlar. bir *.vsct* dosya.

 ```xml
<Button guid="guidMenuTextCmdSet" id="cmdidMyCommand" priority="0x0100" type="Button">
    <Parent guid="guidMenuTextCmdSet" id="MyMenuGroup" />
    <Icon guid="guidImages" id="bmpPic1" />
    <CommandFlag>TextChanges</CommandFlag>
    <Strings>
          <CommandName>cmdidMyCommand</CommandName>
          <ButtonText>My Command name</ButtonText>
    </Strings>
</Button>
 ```

## <a name="see-also"></a>Ayrıca bkz.
- [Visual Studio komut tablosu (.vsct) dosyaları](../extensibility/internals/visual-studio-command-table-dot-vsct-files.md)
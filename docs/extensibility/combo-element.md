---
title: Combos öğesi | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
helpviewer_keywords:
- Combos element (VSCT XML schema)
- VSCT XML schema elements, Combos
ms.assetid: 392e3063-f0a0-4130-9583-23bd2aa3fa36
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: 7cfce045531a871e4630a6175d2fc24f4a50ebd8
ms.sourcegitcommit: b0d8e61745f67bd1f7ecf7fe080a0fe73ac6a181
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/22/2019
ms.locfileid: "56715719"
---
# <a name="combo-element"></a>Combos öğesi
Bir açılan kutunun içinde görünen komutlar tanımlar. Şu şekilde birleşik giriş kutuları dört çeşit vardır: Aşağı açılan, DynamicCombo, IndexCombo ve MRUCombo.

## <a name="syntax"></a>Sözdizimi

```xml
<combo guid="guidMyCommandSet" id="MyCommand" defaultWidth="20" idCommandList="MyCommandListID" priority="0x102" type="DropDownCombo">
  <Parent>... </Parent
  <CommandFlag>... </CommandFlag>
  <Strings>... </Strings>
</combo>
```

## <a name="attributes-and-elements"></a>Öznitelikler ve öğeler
 Öznitelikler, alt ve üst öğeler aşağıdaki bölümlerde açıklanmaktadır.

### <a name="attributes"></a>Öznitelikler

|Öznitelik|Açıklama|
|---------------|-----------------|
|GUID|Gerekli. GUID/ID komut tanımlayıcısı GUİD'si.|
|kimlik|Gerekli. Kimliği bir GUID/ID komut tanımlayıcısı.|
|defaultWidth|Gerekli. Birleşik giriş kutusu için bir piksel genişliği belirten bir tamsayı.|
|idCommandList|Gerekli. Etkin komut hedefinin birleşik giriş kutusunda görüntülenecek öğelerin listesini almak için gönderilen bir kimliği. Kimlik denetimi ile aynı GUID kapsamda olur.|
|öncelik|İsteğe bağlı. Bir sayısal değer yönelik önceliği belirtir.|
| türü|İsteğe bağlı. Düğmenin türü belirten bir numaralandırılmış değeri.<br /><br /> Belirtilmemişse, düğme kullanır.<br /><br /> Aşağı açılan<br /> VSPackage'ı bu birleşik giriş kutusunun içeriğini doldurma için sorumludur. Kullanıcının herhangi bir şey bu açılan metin kutusuna yazamazsınız.<br /><br /> DynamicCombo<br /> VSPackage'ı bu birleşik giriş kutusunun içeriğini doldurmak için sorumludur. Kullanıcı bu birleşik düzenleyebilir ve ayrıca öğeleri seçin.<br /><br /> IndexCombo<br /> BT'nin dışında DynamicCombo aynı metin yerine öğenin dizinini oluşturur.<br /><br /> MRUCombo<br /> VSPackage'ı adına tümleşik geliştirme ortamı (IDE) tarafından doldurulur.  Kullanıcı bu birleşik giriş kutusunda düzenleyebilirsiniz. Son 16 girişleri birleşik giriş kutusu başına en fazla IDE hatırlar.<br /><br /> Kullanıcı bir birleşik giriş kutusunda seçerse ya da yeni bir şeyler girer, IDE uygun VSPackage size bildirir.|
|Koşul|İsteğe bağlı. Bkz: [koşullu öznitelikler](../extensibility/vsct-xml-schema-conditional-attributes.md).|

### <a name="child-elements"></a>Alt öğeleri

|Öğe|Açıklama|
|-------------|-----------------|
|Üst öğe|İsteğe bağlı. Düğmenin üst öğe.|
|CommandFlag|Gerekli. Bkz: [Command flag öğesi](../extensibility/command-flag-element.md). Bir düğme için geçerli CommandFlag değerler aşağıdaki gibidir.<br /><br /> -CaseSensitive<br /><br /> - CommandWellOnly<br /><br /> -DefaultDisabled<br /><br /> -DefaultInvisible<br /><br /> -DynamicVisibility<br /><br /> -Süzme<br /><br /> -IconAndText<br /><br /> -NoAutoComplete<br /><br /> -NoButtonCustomize<br /><br /> -NoCustomize<br /><br /> -NoKeyCustomize<br /><br /> -StretchHorizontally|
|Dizeler|Gerekli. Bkz: [Strings öğesi](../extensibility/strings-element.md). Alt ButtonText öğesi tanımlanmalıdır.|
|Ek Açıklama|İsteğe bağlı bir açıklama.|

### <a name="parent-elements"></a>Üst öğeler

|Öğe|Açıklama|
|-------------|-----------------|
|[Commands öğesi](../extensibility/commands-element.md)|VSPackage araç çubuğundaki komutları koleksiyonunu temsil eder.|

## <a name="example"></a>Örnek

```xml
<Combo guid="guidWidgetPackage" id="cmdidInsertOptions"
  defaultWidth="100" idCommandList="cmdidGetInsertOptionsList">
  <CommandFlag>DynamicVisibility</CommandFlag>
  <Strings>
    <ButtonText>Select Insert Options</ButtonText>
  </Strings>
</Combo>

<Combo guid="guidWidgetPackage" id="cmdidInsertOptions"
  priority="0x0500" type="DropDownCombo" defaultWidth="100"
  idCommandList="cmdidGetInsertOptionsList">
  <Parent guid="cmdSetGuidWidgetCommands" id="groupIDFileEdit">
  <CommandFlag>DynamicVisibility</CommandFlag>
  <Strings>
    <ButtonText>Select Insert Options</ButtonText>
  </Strings>
</Combo>
```

## <a name="see-also"></a>Ayrıca bkz.
- [Visual Studio komut tablosu (.vsct) dosyaları](../extensibility/internals/visual-studio-command-table-dot-vsct-files.md)

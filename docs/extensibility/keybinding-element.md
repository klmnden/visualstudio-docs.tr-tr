---
title: KeyBinding öğesi | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
helpviewer_keywords:
- VSCT XML schema elements, KeyBindings
- KeyBinding element (VSCT XML schema)
ms.assetid: e55a1098-15df-42a9-9f87-e3a99cf437dd
author: madskristensen
ms.author: madsk
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: 9c3bc5e10c928c50bca1ea3879531885f4580519
ms.sourcegitcommit: 40d612240dc5bea418cd27fdacdf85ea177e2df3
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/29/2019
ms.locfileid: "66309637"
---
# <a name="keybinding-element"></a>KeyBinding öğesi
Komut için klavye kısayolları KeyBinding öğesi belirtir.

 Komutlar tek ve çift tuş bağlamaları ilişkili olabilir. Tek bir tuş bağlama örneğidir **Ctrl**+**S** için **Kaydet** komutu. Bir komut tetiklemek için iki ardışık tuş birleşimleri çift anahtar bağlamalarını gerektirir. Bir çift anahtar bağlama örneğidir <strong>Ctrl *+</strong>K<strong>,</strong>Ctrl<strong>+</strong>K** işareti ayarlamak için.

## <a name="syntax"></a>Sözdizimi

```
<Keybinding guid="MyGuid" id="MyId" Editor="MyEditor" key1="B" key2="x" mod1="Control" mod2="Alt" />
```

## <a name="attributes-and-elements"></a>Öznitelikler ve öğeler
 Öznitelikler, alt ve üst öğeler aşağıdaki bölümlerde açıklanmaktadır.

### <a name="attributes"></a>Öznitelikler

|Öznitelik|Açıklama|
|---------------|-----------------|
|GUID|Gerekli.|
|kimlik|Gerekli.|
|düzenleyici|Gerekli. GUID Düzenleyici klavye kısayolu etkin olacağı düzenleme bağlamı gösterir. Genel bağlama kapsam "guidVSStd97" değeridir.|
|key1|Gerekli. Geçerli değerler tüm typable alfasayısal karakterler ve iki basamaklı onaltılık değerler 0 x öncesinde ve [VK_constants](/windows/desktop/inputdev/virtual-key-codes).|
|Değişiklik1|İsteğe bağlı. Herhangi bir birleşimini **Ctrl**, **Alt**, ve **Shift** boşlukla ayrılmış.|
|key2|İsteğe bağlı. Geçerli değerler tüm typable alfasayısal karakterler ve iki basamaklı onaltılık değerler 0 x öncesinde ve [VK_constants](/windows/desktop/inputdev/virtual-key-codes).|
|mod2|İsteğe bağlı. Herhangi bir birleşimini **Ctrl**, **Alt**, ve **Shift** boşlukla ayrılmış.|
|Öykünücü|İsteğe bağlı.|
|Koşul|İsteğe bağlı. Bkz: [koşullu öznitelikler](../extensibility/vsct-xml-schema-conditional-attributes.md).|

### <a name="child-elements"></a>Alt öğeleri

|Öğe|Açıklama|
|-------------|-----------------|
|Üst öğe||
|Ek Açıklama||

### <a name="parent-elements"></a>Üst öğeler

|Öğe|Açıklama|
|-------------|-----------------|
|[KeyBindings öğesi](../extensibility/keybindings-element.md)|Tuş öğeleri gruplandırır ve diğer KeyBindings gruplandırmaları.|

## <a name="example"></a>Örnek

```
<KeyBindings>
  <KeyBinding guid="guidWidgetPackage" id="cmdidUpdateWidget"
    editor="guidWidgetEditor" key1="VK_F5"/>
  <KeyBinding guid="guidWidgetPackage" id="cmdidRunWidget"
    editor="guidWidgetEditor" key1="VK_F5" mod1="Control"/>
</KeyBindings>
```

## <a name="see-also"></a>Ayrıca bkz.
- [KeyBindings öğesi](../extensibility/keybindings-element.md)
- [Visual Studio komut tablosu (.vsct) dosyaları](../extensibility/internals/visual-studio-command-table-dot-vsct-files.md)

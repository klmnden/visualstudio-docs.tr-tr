---
title: Extern öğesi | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
f1_keywords:
- Extern
helpviewer_keywords:
- VSCT XML schema elements, Extern
- Extern element (VSCT XML schema)
ms.assetid: db6c3ddd-a1ba-450a-897a-bb568a5377fc
author: madskristensen
ms.author: madsk
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: 34e38618a153aa74bdc2449895272fc9e399c82d
ms.sourcegitcommit: 40d612240dc5bea418cd27fdacdf85ea177e2df3
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/29/2019
ms.locfileid: "66342793"
---
# <a name="extern-element"></a>Extern öğesi
Extern öğesi herhangi bir dış başlığını başvurur ( *.h*) ile birleştirmek için dosyaları *.vsct* dosya derleme zamanında. VSCT derleyici için verilen ya da başvurduğu yoluna birleştirilecek dosyaları olmalıdır bir [INCLUDE öğesi](../extensibility/include-element.md). Diğer dosyalar olabilir *.vsct* veya C++ üst bilgi dosyaları.

 Üst bilgi dosyaları tanımlarında biçiminde olmalıdır "# [Value] [simge] define" önceden tanımlı değilse değer başka bir sembol olabilir. Tanımları komut öğeleri koşullu ifadelerde kullanılabilir. Gerçekten kullanılmıyorsa herhangi bir simge atılacak.

 CommandTable öğesi Extern öğesi

## <a name="syntax"></a>Sözdizimi

```xml
<Extern href="stdidcmd.h" />
```

## <a name="attributes-and-elements"></a>Öznitelikler ve öğeler
 Öznitelikler, alt ve üst öğeler aşağıdaki bölümlerde açıklanmaktadır.

### <a name="attributes"></a>Öznitelikler

|Öznitelik|Açıklama|
|---------------|-----------------|
|href|Gerekli. Üstbilgi dosyası yolu:<br /><br /> href="stdidcmd.h"|
|Koşul|İsteğe bağlı. Bkz: [koşullu öznitelikler](../extensibility/vsct-xml-schema-conditional-attributes.md).|
|dil|İsteğe bağlı. Tüm varsayılan dili [ \<dizeleri >](../extensibility/strings-element.md) komut tablosu öğeleri:<br /><br /> Dil = "en-us"|

### <a name="child-elements"></a>Alt öğeleri

|Öğe|Açıklama|
|-------------|-----------------|
|Yok.|Yok.|

### <a name="parent-elements"></a>Üst öğeler

|Öğe|Açıklama|
|-------------|-----------------|
|[CommandTable öğesi](../extensibility/commandtable-element.md)|Tüm komutları temsil eden öğeler tanımlar — diğer bir deyişle, menü öğeleri, menüler, araç çubukları ve birleşik giriş kutuları — IDE'ye VSPackage sağlayan.|

## <a name="example"></a>Örnek

```xml
<?xml version="1.0" encoding="utf-8"?>
<CommandTable xmlns="http://schemas.microsoft.com/VisualStudio/2005-10-
  18/CommandTable" xmlns:xs="http://www.w3.org/2001/XMLSchema">
    <Extern href="C:\VSCore\vscommon\inc\vsshlids.h"/>
    ...
  <Commands package="guidMyPackage">
</CommandTable>
```

## <a name="see-also"></a>Ayrıca bkz.
- [Visual Studio komut tablosu (.vsct) dosyaları](../extensibility/internals/visual-studio-command-table-dot-vsct-files.md)
- [VSPackage kullanıcı arabirimi öğelerini nasıl eklenir](../extensibility/internals/how-vspackages-add-user-interface-elements.md)
- [Komutlar, menüler ve araç çubukları](../extensibility/internals/commands-menus-and-toolbars.md)
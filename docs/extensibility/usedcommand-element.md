---
title: UsedCommand öğesi | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
helpviewer_keywords:
- UsedCommands element (VSCT XML schema)
- VSCT XML schema elements, UsedCommands
ms.assetid: 99cd05d3-644a-42ff-b289-8458cd1b20c0
author: madskristensen
ms.author: madsk
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: 36dbfa484b69832c67c7a1dd28f217706e1a91a6
ms.sourcegitcommit: 40d612240dc5bea418cd27fdacdf85ea177e2df3
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/29/2019
ms.locfileid: "66316311"
---
# <a name="usedcommand-element"></a>UsedCommand Öğesi
VSPackage'ı başka bir .vsct dosyası içinde tanımlanan bir komutuna erişmek üzere etkinleştirir. Örneğin, standart, VSPackage'ı kullanıyorsa, **kopyalama** tanımlanan komutu [!INCLUDE[vsprvs](../code-quality/includes/vsprvs_md.md)] shell ekleyebileceğiniz komut bir menü veya araç yeniden uygulamadan.

## <a name="syntax"></a>Sözdizimi

```
<UsedCommand guid="guidMyCommandGroup" id="MyCommand" />
```

## <a name="attributes-and-elements"></a>Öznitelikler ve Öğeler
 Öznitelikler, alt ve üst öğeler aşağıdaki bölümlerde açıklanmaktadır.

### <a name="attributes"></a>Öznitelikler

|Öznitelik|Açıklama|
|---------------|-----------------|
|GUID|Gerekli. Komut tanımlayan GUID kimliği çiftinin GUID.|
|kimlik|Gerekli. Komut tanımlayan GUID kimliği çifti kimliği.|
|Koşul|İsteğe bağlı. Bkz: [koşullu öznitelikler](../extensibility/vsct-xml-schema-conditional-attributes.md).|

### <a name="child-elements"></a>Alt Öğeler

|Öğe|Açıklama|
|-------------|-----------------|
|Yok.||

### <a name="parent-elements"></a>Üst Öğeler

|Öğe|Açıklama|
|-------------|-----------------|
|[UsedCommands Öğesi](../extensibility/usedcommands-element.md)|UsedCommand öğeleri gruplandırır ve diğer UsedCommands gruplandırmaları.|

## <a name="remarks"></a>Açıklamalar
 Bir komutu ekleyerek `<UsedCommands>` öğesi, bir VSPackage'ı bilgilendirir [!INCLUDE[vsprvs](../code-quality/includes/vsprvs_md.md)] ortam VSPackage komutu gerektirir. Eklemeniz bir `<UsedCommand>` paketinizi gerektiren herhangi bir komutun öğesi, değil tüm sürümleri ve yapılandırmaları Visual Studio'nun içinde bulunabilir. Paketiniz Visual C++ için belirli bir komut çağırırsa, eklemediğiniz sürece Örneğin, komut Visual Web Developer kullanıcılara kullanılamaz bir `<UsedCommand>` komutu için öğesi.

## <a name="example"></a>Örnek

```
<UsedCommands>
  <UsedCommand guid="guidVSStd97" id="cmdidCut"/>
  <UsedCommand guid="guidVSStd97" id="cmdidCopy"/>
  <UsedCommand guid="guidVSStd97" id="cmdidPaste"/>
</UsedCommands>
```

## <a name="see-also"></a>Ayrıca Bkz.
- [UsedCommands Öğesi](../extensibility/usedcommands-element.md)
- [Visual Studio Komut Tablosu (.Vsct) Dosyaları](../extensibility/internals/visual-studio-command-table-dot-vsct-files.md)
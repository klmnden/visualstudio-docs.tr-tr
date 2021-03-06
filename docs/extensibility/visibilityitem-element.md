---
title: Visibilityıtem öğesi | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
helpviewer_keywords:
- VisibilityItem element (VSCT XML schema)
- VSCT XML schema elements, VisibilityItem
ms.assetid: 0932f551-972d-4194-84bb-426e3e4375e4
author: madskristensen
ms.author: madsk
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: 6c817b9a004872800b02f6a7c6d0f64fd324304b
ms.sourcegitcommit: 40d612240dc5bea418cd27fdacdf85ea177e2df3
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/29/2019
ms.locfileid: "66310725"
---
# <a name="visibilityitem-element"></a>Visibilityıtem öğesi
`VisibilityItem` Komutları ve araç çubuklarını statik görünürlüğünü belirler. Her giriş, bir komut veya menü ve ayrıca bir ilişkili komut UI bağlamı tanımlar. Visual Studio, bunları tanımlama VSPackage'ları yüklemeden komutlar, menüler ve araç çubukları ve kendi görünürlük algılar. IDE kullanır <xref:Microsoft.VisualStudio.Shell.Interop.IVsMonitorSelection.IsCmdUIContextActive%2A> komut UI bağlamı etkin olup olmadığını belirlemek için yöntemi.

 VSPackage'ı yüklendikten sonra Visual Studio komut görünürlük VSPackage'ı tarafından belirlenecek bekliyor yerine `VisibilityItem`. Komutun görünürlüğü belirlemek için ya da uygulayabilirsiniz <xref:Microsoft.VisualStudio.Shell.OleMenuCommand.BeforeQueryStatus> olay işleyicisi veya <xref:Microsoft.VisualStudio.OLE.Interop.IOleCommandTarget.QueryStatus%2A> komutunuz nasıl uyguladıysanız bağlı olarak yöntemi.

 Bir komut veya sahip menü bir `VisibilityItem` öğesi, yalnızca ilişkili bağlam etkin olduğunda görünür. Her bir bağlam içi komut bileşimi için bir giriş ekleyerek, bir veya daha fazla komut UI bağlamı ile tek bir komut, menü veya araç ilişkilendirebilirsiniz. Bir komut veya menü birden fazla komut UI bağlamı ile ilişkili ise, ilişkili komut UI bağlamları herhangi biri etkin olduğunda ardından bir komut veya menüyü görülebilir.

 `VisibilityItem` Öğesi uygulandığı yalnızca komutlar, menüler ve araç çubuklarını, grupları uygulanmaz. İlgili olmayan bir öğe `VisibilityItem` öğesi, kendi üst menü etkin olduğunda görülebilir.

## <a name="syntax"></a>Sözdizimi

```xml
<VisibilityItem
  guid ="="cmdGuidMyProductCommands"
  id=="cmdidAddWidget"
  context="guidNotViewSourceMode"/>
```

## <a name="attributes-and-elements"></a>Öznitelikler ve öğeler
 Öznitelikler, alt ve üst öğeler aşağıdaki bölümlerde açıklanmaktadır.

### <a name="attributes"></a>Öznitelikler

|Öznitelik|Açıklama|
|---------------|-----------------|
|GUID|Gerekli. GUID/ID komut tanımlayıcısı GUİD'si.|
|kimlik|Gerekli. GUID/ID komut tanımlayıcısı kimliği.|
|bağlam|Gerekli. UI bağlamı komutu görülebilir.|
|Koşul|İsteğe bağlı. Bkz: [koşullu öznitelikler](../extensibility/vsct-xml-schema-conditional-attributes.md).|

### <a name="child-elements"></a>Alt öğeleri
 Yok.

### <a name="parent-elements"></a>Üst öğeler

|Öğe|Açıklama|
|-------------|-----------------|
|[VisibilityConstraints öğesi](../extensibility/visibilityconstraints-element.md)|`VisibilityConstraints` Komutları ve araç çubukları grupları statik görünürlüğünü belirler.|

## <a name="remarks"></a>Açıklamalar
 Standart bir Visual Studio UI bağlamları içinde tanımlanan *Visual Studio SDK yükleme yolunu*\VisualStudioIntegration\Common\Inc\vsshlids.h dosyasında da olarak <xref:Microsoft.VisualStudio.Shell.Interop.UIContextGuids> ve <xref:Microsoft.VisualStudio.Shell.Interop.UIContextGuids80> sınıfları. UI bağlamları daha eksiksiz bir kümesini tanımlanan <xref:Microsoft.VisualStudio.VSConstants> sınıfı.

## <a name="example"></a>Örnek

```xml
<VisibilityConstraints>
  <VisibilityItem guid="cmdSetGuidMyProductCommands"     id="cmdidAddWidget"
    context="guidNotViewSourceMode"/>
</VisibilityConstraints>
```

## <a name="see-also"></a>Ayrıca bkz.
- <xref:Microsoft.VisualStudio.Shell.Interop.IVsMonitorSelection.IsCmdUIContextActive%2A>
- <xref:Microsoft.VisualStudio.Shell.OleMenuCommand.BeforeQueryStatus>
- <xref:Microsoft.VisualStudio.VSConstants>
- <xref:Microsoft.VisualStudio.Shell.Interop.UIContextGuids>
- <xref:Microsoft.VisualStudio.Shell.Interop.UIContextGuids80>
- [VisibilityConstraints öğesi](../extensibility/visibilityconstraints-element.md)
- [Visual Studio komut tablosu (. Vsct) dosyaları](../extensibility/internals/visual-studio-command-table-dot-vsct-files.md)
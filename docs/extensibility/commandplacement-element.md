---
title: CommandPlacement öğesi | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
helpviewer_keywords:
- CommandPlacements element (VSCT XML schema)
- VSCT XML schema elements, CommandPlacements
ms.assetid: 2cbd7ac8-c55a-43d8-a26d-713b3d790016
author: gregvanl
ms.author: gregvanl
manager: douge
ms.workload:
- vssdk
ms.openlocfilehash: c5d694f6ed12d3fd7d531ec6a0a01ec70a826561
ms.sourcegitcommit: 37fb7075b0a65d2add3b137a5230767aa3266c74
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/02/2019
ms.locfileid: "53941372"
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
 [CommandPlacements öğesi](../extensibility/commandplacements-element.md)   
 [Visual Studio komut tablosu (.vsct) dosyaları](../extensibility/internals/visual-studio-command-table-dot-vsct-files.md)

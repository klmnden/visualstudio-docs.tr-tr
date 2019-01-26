---
title: Groups öğesi | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
helpviewer_keywords:
- VSCT XML schema elements, Groups
- Groups element (VSCT XML schema)
ms.assetid: 740ca4ec-79fa-4b98-8f9a-2a137f9f7f98
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: 35266ff23d93e0dbdfbe6a2be14631db5c0629e5
ms.sourcegitcommit: 2193323efc608118e0ce6f6b2ff532f158245d56
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/25/2019
ms.locfileid: "54972712"
---
# <a name="groups-element"></a>Groups öğesi
VSPackage komut gruplarını tanımlar girişleri içerir.  
  
## <a name="syntax"></a>Sözdizimi  
  
```xml  
<Groups>  
  <Group>... </Group>  
  <Group>... </Group>  
</Groups>  
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
|[Group öğesi](../extensibility/group-element.md)|Tek bir komut grubunu temsil eder.|  
|[Groups öğesi](../extensibility/groups-element.md)|VSPackage komut gruplarını tanımlar girişleri içerir.|  
  
### <a name="parent-elements"></a>Üst öğeler  
  
|Öğe|Açıklama|  
|-------------|-----------------|  
|[Commands öğesi](../extensibility/commands-element.md)|VSPackage araç çubuğundaki komutları koleksiyonunu temsil eder.|  
  
## <a name="example"></a>Örnek  
  
```xml  
<Groups>  
  <Group guid="cmdSetGuidWidgetCommands" id="groupIDFileEdit">  
    <Parent guid="guidSHLMainMenu" id="IDM_VS_TOOL_MAINMENU"/>  
  </Group>  
</Groups>  
```  
  
## <a name="see-also"></a>Ayrıca bkz.  
 [VSPackage kullanıcı arabirimi öğelerini nasıl eklenir](../extensibility/internals/how-vspackages-add-user-interface-elements.md)   
 [Komutlar, menüler ve araç çubukları](../extensibility/internals/commands-menus-and-toolbars.md)
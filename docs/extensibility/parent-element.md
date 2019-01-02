---
title: Üst öğe | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
helpviewer_keywords:
- VSCT XML schema elements, Parent
- Parent element (VSCT XML schema)
ms.assetid: e4624ac8-1b9a-4940-910a-528a661cefad
author: gregvanl
ms.author: gregvanl
manager: douge
ms.workload:
- vssdk
ms.openlocfilehash: c025957bd0d3cf06bf73e1b35b5faa661386a0a5
ms.sourcegitcommit: 37fb7075b0a65d2add3b137a5230767aa3266c74
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/02/2019
ms.locfileid: "53902443"
---
# <a name="parent-element"></a>Üst öğe
Bir düğme veya birleşik giriş kutusunun üst yalnızca bir grup olabilir. Bir menü veya grubun üst herhangi bir menü veya grup olabilir. İçinde bir [CommandPlacement öğesi](../extensibility/commandplacement-element.md), bu öğe gereklidir; diğer tüm durumlarda isteğe bağlıdır. Bu öğe atlanırsa, üst `Group_Undefined:0` kapsanan.  
  
## <a name="syntax"></a>Sözdizimi  
  
```xml  
<Parent guid="guidMyCommandSet" id="MyParentGroupOrMenu" />  
```  
  
## <a name="attributes-and-elements"></a>Öznitelikler ve öğeler  
 Öznitelikler, alt ve üst öğeler aşağıdaki bölümlerde açıklanmaktadır.  
  
### <a name="attributes"></a>Öznitelikler  
  
|Öznitelik|Açıklama|  
|---------------|-----------------|  
|GUID|Gerekli. GUID GUID/kimliği komut tanımlayıcısı.|  
|kimlik|Gerekli. Kimliği GUID/kimliği komut tanımlayıcısı.|  
  
### <a name="child-elements"></a>Alt öğeleri  
 Hiçbiri  
  
### <a name="parent-elements"></a>Üst öğeler  
  
|Öğe|Açıklama|  
|-------------|-----------------|  
|[CommandTable öğesi](../extensibility/commandtable-element.md)|VSPackage sağlayan komutlar tümleşik geliştirme ortamı (IDE) temsil eden tüm öğeleri tanımlar. Örneğin, menü öğeleri, menüler, araç çubukları ve birleşik giriş kutuları.|  
|[Buttons öğesi](../extensibility/buttons-element.md)|Grupları [Button öğesi](../extensibility/button-element.md) öğeleri.|  
|[Menus öğesi](../extensibility/menus-element.md)|VSPackage'ı uygulayan tüm menüleri tanımlar.|  
|[Groups öğesi](../extensibility/groups-element.md)|VSPackage komut gruplarını tanımlar girişleri içerir.|  
  
## <a name="see-also"></a>Ayrıca bkz.  
 [Visual Studio komut tablosu (.vsct) dosyaları](../extensibility/internals/visual-studio-command-table-dot-vsct-files.md)
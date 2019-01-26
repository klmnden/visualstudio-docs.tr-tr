---
title: Idsymbol öğesi | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
helpviewer_keywords:
- IDSymbol element (VSCT XML schema)
- VSCT XML schema elements, IDSymbol
ms.assetid: 760cfd20-3c06-422c-9103-98bfa1f387f8
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: 93973eeadf7629201aa6bd739f33a094677efe5f
ms.sourcegitcommit: 2193323efc608118e0ce6f6b2ff532f158245d56
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/25/2019
ms.locfileid: "54961484"
---
# <a name="idsymbol-element"></a>Idsymbol öğesi
`IDSymbol` Öğesi menüsü, Grup veya komutu temsil eden GUID:ID çifti Kimliğini içerir. GUID üst öğesinden gelen `GuidSymbol` öğesi. `IDSymbol` Öğeye sahip bir `name` bulunan kimliği için bir kolay ad sağlayan öznitelik `value` özniteliği.  
  
## <a name="syntax"></a>Sözdizimi  
  
```xml  
<IDSymbol name=ElementName value="0x0010" />  
```  
  
## <a name="attributes-and-elements"></a>Öznitelikler ve öğeler  
 Öznitelikler, alt ve üst öğeler aşağıdaki bölümlerde açıklanmaktadır.  
  
### <a name="attributes"></a>Öznitelikler  
  
|Öznitelik|Açıklama|  
|---------------|-----------------|  
|name|Gerekli. Kimliği sembol adı.|  
|value|Gerekli. Kimliği sembolün sayısal kimlik değeri.|  
  
### <a name="child-elements"></a>Alt öğeleri  
 Yok.  
  
### <a name="parent-elements"></a>Üst öğeler  
  
|Öğe|Açıklama|  
|-------------|-----------------|  
|[GuidSymbol öğesi](../extensibility/guidsymbol-element.md)|Bir menü, Grup veya komutu temsil eden GUID:ID çiftinin GUID içerir. Grupları `IDSymbol` öğeleri.|  
  
## <a name="remarks"></a>Açıklamalar  
 Her `IDSymbol` öğesinde bir verilen `GuidSymbol` öğesi benzersiz olmalı `value`. Ancak, `IDSymbol` farklı bir üst öğeye sahip oldukları sürece aynı değerlere sahip öğeleri bir paket içinde bulunabilir.  
  
## <a name="see-also"></a>Ayrıca bkz.  
 [Visual Studio komut tablosu (.vsct) dosyaları](../extensibility/internals/visual-studio-command-table-dot-vsct-files.md)
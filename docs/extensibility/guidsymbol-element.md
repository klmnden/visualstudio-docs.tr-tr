---
title: GuidSymbol öğesi | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
helpviewer_keywords:
- VSCT XML schema elements, GuidSymbol
- GuidSymbol element (VSCT XML schema)
ms.assetid: 11fb3545-8974-4776-9a54-6b6e7739ae31
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: d8b36df3fe4e546e8391d23ccadc33faf9f2a642
ms.sourcegitcommit: 2193323efc608118e0ce6f6b2ff532f158245d56
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/25/2019
ms.locfileid: "54992886"
---
# <a name="guidsymbol-element"></a>GuidSymbol öğesi
`GuidSymbol` Öğeyi içeren bir menü, Grup veya komutu temsil eden GUID:ID çiftinin GUID. Kimliği geldiği bir `IDSymbol` öğesinde `GuidSymbol` öğesi. `GuidSymbol` Öğeye sahip bir `name` bulunan GUID için kolay bir ad sağlar özniteliği `value` özniteliği.  
  
## <a name="syntax"></a>Sözdizimi  
  
```xml  
<GuidSymbol name="guidMyCommandSet" value="{xxxxxxxxxxxxx-xxxx-xxxx-xxxxxxxxxxxx}">  
  <IDSymbol>... </IDSymbol>  
  <IDSymbol>... </IDSymbol>  
</GuidSymbol>  
```  
  
## <a name="attributes-and-elements"></a>Öznitelikler ve öğeler  
 Öznitelikler, alt ve üst öğeler aşağıdaki bölümlerde açıklanmaktadır.  
  
### <a name="attributes"></a>Öznitelikler  
  
|Öznitelik|Açıklama|  
|---------------|-----------------|  
|name|Gerekli. GUID sembol adı.|  
|value|Gerekli. GUID sembol GUİD'si.|  
  
### <a name="child-elements"></a>Alt öğeleri  
  
|Öğe|Açıklama|  
|-------------|-----------------|  
|[Idsymbol öğesi](../extensibility/idsymbol-element.md)|Bir menü, Grup veya komutu temsil eden GUID:ID çifti Kimliğini içerir.|  
  
### <a name="parent-elements"></a>Üst öğeler  
  
|Öğe|Açıklama|  
|-------------|-----------------|  
|[Symbols öğesi](../extensibility/symbols-element.md)|Grupları `GuidSymbol` öğelerinde bir *.vsct* dosya.|  
  
## <a name="remarks"></a>Açıklamalar  
 Genellikle, bir *.vsct* dosya içeren üç `GuidSymbol` öğesinde kendi `Symbols` bölümü, bir paket için bir komut kümesi (menüleri koleksiyonunu gruplandırır ve paket kullanımınıza sunduğu komutlar) için ve biri bit eşlemler düğmeler ve diğer görsel bileşenleri için simgeler sağlar. Her `IDSymbol` öğesinde bir verilen `GuidSymbol` öğesi benzersiz olmalı `value`. Ancak, `IDSymbol` farklı bir üst öğeye sahip oldukları sürece aynı değerlere sahip öğeleri bir paket içinde bulunabilir.  
  
## <a name="see-also"></a>Ayrıca bkz.  
 [Visual Studio komut tablosu (.vsct) dosyaları](../extensibility/internals/visual-studio-command-table-dot-vsct-files.md)
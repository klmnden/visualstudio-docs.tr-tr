---
title: GuidSymbol öğesi | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-sdk
ms.topic: reference
helpviewer_keywords:
- VSCT XML schema elements, GuidSymbol
- GuidSymbol element (VSCT XML schema)
ms.assetid: 11fb3545-8974-4776-9a54-6b6e7739ae31
caps.latest.revision: 9
ms.author: gregvanl
manager: jillfra
ms.openlocfilehash: 5f11ed48d9dcf961228957cf15db3815c00d14d7
ms.sourcegitcommit: 8b538eea125241e9d6d8b7297b72a66faa9a4a47
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54770070"
---
# <a name="guidsymbol-element"></a>GuidSymbol Öğesi
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

`GuidSymbol` Öğeyi içeren bir menü, Grup veya komutu temsil eden GUID:ID çiftinin GUID. Kimliği geldiği bir `IDSymbol` öğesinde `GuidSymbol` öğesi. `GuidSymbol` Öğeye sahip bir `name` bulunan GUID için kolay bir ad sağlar özniteliği `value` özniteliği.  
  
## <a name="syntax"></a>Sözdizimi  
  
```  
<GuidSymbol name="guidMyCommandSet" value="{xxxxxxxxxxxxx-xxxx-xxxx-xxxxxxxxxxxx}">  
  <IDSymbol>... </IDSymbol>  
  <IDSymbol>... </IDSymbol>  
</GuidSymbol>  
```  
  
## <a name="attributes-and-elements"></a>Öznitelikler ve Öğeler  
 Öznitelikler, alt ve üst öğeler aşağıdaki bölümlerde açıklanmaktadır.  
  
### <a name="attributes"></a>Öznitelikler  
  
|Öznitelik|Açıklama|  
|---------------|-----------------|  
|name|Gerekli. GUID sembol adı.|  
|value|Gerekli. GUID sembol GUİD'si.|  
  
### <a name="child-elements"></a>Alt Öğeler  
  
|Öğe|Açıklama|  
|-------------|-----------------|  
|[IDSymbol Öğesi](../extensibility/idsymbol-element.md)|Bir menü, Grup veya komutu temsil eden GUID:ID çifti Kimliğini içerir.|  
  
### <a name="parent-elements"></a>Üst Öğeler  
  
|Öğe|Açıklama|  
|-------------|-----------------|  
|[Symbols Öğesi](../extensibility/symbols-element.md)|Grupları `GuidSymbol` .vsct dosyası öğeleri.|  
  
## <a name="remarks"></a>Açıklamalar  
 Genellikle, .vsct dosyası üç içeren `GuidSymbol` öğesinde kendi `Symbols` bölümü, bir paket için bir komut kümesi (menüler, grupları ve paket kullanıma sunduğu komutları koleksiyonu) için ve biri bit eşlemler sağlamak için düğme ve diğer görsel bileşenleri için simgeler. Her `IDSymbol` öğesinde bir verilen `GuidSymbol` öğesi benzersiz olmalı `value`. Ancak, `IDSymbol` farklı bir üst öğeye sahip oldukları sürece aynı değerlere sahip öğeleri bir paket içinde bulunabilir.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Visual Studio Komut Tablosu (.Vsct) Dosyaları](../extensibility/internals/visual-studio-command-table-dot-vsct-files.md)

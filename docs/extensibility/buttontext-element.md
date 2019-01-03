---
title: ButtonText öğesi | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
helpviewer_keywords:
- ButtonText element (VSCT XML schema)
- VSCT XML schema elements, ButtonText
ms.assetid: 56aba884-0356-4894-ae4e-32d3938f6865
author: gregvanl
ms.author: gregvanl
manager: douge
ms.workload:
- vssdk
ms.openlocfilehash: 8edd12a2f37ea0de3a3c01f013adea64a08424f5
ms.sourcegitcommit: 37fb7075b0a65d2add3b137a5230767aa3266c74
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/02/2019
ms.locfileid: "53905591"
---
# <a name="buttontext-element"></a>ButtonText öğesi
Bu alan çeşitli menülerde görüntülenen metin belirtmenize olanak sağlar. Varsayılan olarak, `ButtonText` öğesi menüsü denetleyicileri görünür. `ButtonText` Öğesi diğer metin alanları boş ise varsayılan ayrıca olur. `ButtonText` Bile diğer metin alanları öğesi boş olamaz.  
  
## <a name="syntax"></a>Sözdizimi  
  
```xml  
<ButtonText>My Command</ButtonText>  
```  
  
## <a name="attributes-and-elements"></a>Öznitelikler ve öğeler  
 Öznitelikler, alt ve üst öğeler aşağıdaki bölümlerde açıklanmaktadır.  
  
### <a name="attributes"></a>Öznitelikler  
 Yok.  
  
### <a name="child-elements"></a>Alt öğeleri  
 Yok.  
  
### <a name="parent-elements"></a>Üst öğeler  
  
|Öğe|Açıklama|  
|-------------|-----------------|  
|[Strings Öğesi](../extensibility/strings-element.md)|Metin öğeleri gibi gruplar `ButtonText` ve `CommandName`.|  
  
## <a name="text-value"></a>Metin değeri  
 Metin değeri `ButtonText` öğesi menü öğeleri, combos ve görünen metin sahip diğer kullanıcı arabirimi (UI) öğeleri için görüntülenen metni sağlar.  
  
## <a name="see-also"></a>Ayrıca bkz.  
 [Visual Studio komut tablosu (.vsct) dosyaları](../extensibility/internals/visual-studio-command-table-dot-vsct-files.md)
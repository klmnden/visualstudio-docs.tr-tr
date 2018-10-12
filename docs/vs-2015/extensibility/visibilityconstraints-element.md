---
title: VisibilityConstraints öğesi | Microsoft Docs
ms.custom: ''
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.reviewer: ''
ms.suite: ''
ms.technology:
- vs-ide-sdk
ms.tgt_pltfrm: ''
ms.topic: article
f1_keywords:
- VisibilityConstraints
helpviewer_keywords:
- VSCT XML schema elements, VisibilityConstraints
- VisibilityConstraints element (VSCT XML schema)
ms.assetid: d6dcd314-6fe4-4693-a189-91fa026c7b34
caps.latest.revision: 11
ms.author: gregvanl
manager: ghogen
ms.openlocfilehash: b5b290884a2377cdaba573788f0881ec82a19cdf
ms.sourcegitcommit: 9ceaf69568d61023868ced59108ae4dd46f720ab
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/12/2018
ms.locfileid: "49222384"
---
# <a name="visibilityconstraints-element"></a>VisibilityConstraints Öğesi
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

VisibilityConstraints öğesi gruplarını komutları ve araç çubukları statik görünürlüğünü belirler. Görünürlük varsayılan tarafından denetlenir [!INCLUDE[vsprvs](../includes/vsprvs-md.md)] VSPackage yükleme olmadan tümleşik geliştirme ortamı (IDE).  
  
## <a name="syntax"></a>Sözdizimi  
  
```  
<VisibilityConstraints>  
  <VisibilityConstraint>... </VisibilityConstraint>  
  <VisibilityConstraint>... </VisibilityConstraint>  
</VisibilityConstraint>  
```  
  
## <a name="attributes-and-elements"></a>Öznitelikler ve Öğeler  
 Öznitelikler, alt ve üst öğeler aşağıdaki bölümlerde açıklanmaktadır.  
  
### <a name="attributes"></a>Öznitelikler  
  
|Öznitelik|Açıklama|  
|---------------|-----------------|  
|Koşul|İsteğe bağlı. Bkz: [koşullu öznitelikler](../extensibility/vsct-xml-schema-conditional-attributes.md).|  
  
### <a name="child-elements"></a>Alt Öğeler  
  
|Öğe|Açıklama|  
|-------------|-----------------|  
|[VisibilityItem Öğesi](../extensibility/visibilityitem-element.md)|Komutlar ve araç çubukları statik görünürlüğünü belirler.|  
|[VisibilityConstraints](../extensibility/visibilityconstraints-element.md)|Komutlar ve araç çubukları grupları statik görünürlüğünü belirler.|  
  
### <a name="parent-elements"></a>Üst Öğeler  
  
|Öğe|Açıklama|  
|-------------|-----------------|  
|[CommandTable Öğesi](../extensibility/commandtable-element.md)|VSPackage sunar IDE'nin komutlarını (örneğin, menü öğeleri, menüler, araç çubukları ve birleşik giriş kutuları) temsil eden tüm öğeleri tanımlar.|  
  
## <a name="example"></a>Örnek  
  
```  
<VisibilityConstraints>  
  <VisibilityItem guid="cmdSetGuidMyProductCommands"     id="cmdidAddWidget"  
    context="guidNotViewSourceMode"/>  
</VisibilityConstraints>  
```  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Visibilityıtem öğesi](../extensibility/visibilityitem-element.md)   
 [Visual Studio Komut Tablosu (.Vsct) Dosyaları](../extensibility/internals/visual-studio-command-table-dot-vsct-files.md)


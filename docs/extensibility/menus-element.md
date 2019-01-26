---
title: Menus öğesi | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
helpviewer_keywords:
- VSCT XML schema elements, Menus
- Menus element (VSCT XML schema)
ms.assetid: d825a99b-e05c-4dd9-8933-a180216d667a
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: e31be4d128ef9a349c4f2278a5b3f64982e1a4eb
ms.sourcegitcommit: 2193323efc608118e0ce6f6b2ff532f158245d56
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/25/2019
ms.locfileid: "55039130"
---
# <a name="menus-element"></a>Menus öğesi
Tüm bir VSPackage'ı uygulayan araç çubukları ve menüler tanımlar.  
  
## <a name="syntax"></a>Sözdizimi  
  
```xml  
<Menus>  
  <Menu>... </Menu>  
  <Menu>... </Menu>  
</Menus>  
```  
  
## <a name="attributes-and-elements"></a>Öznitelikler ve öğeler  
 Öznitelikler, alt ve üst öğeler aşağıdaki bölümlerde açıklanmaktadır.  
  
### <a name="attributes"></a>Öznitelikler  
  
|Öznitelik|Açıklama|  
|---------------|-----------------|  
|Koşul|İsteğe bağlı. Bkz: [koşullu öznitelikler](../extensibility/vsct-xml-schema-conditional-attributes.md).|  
  
### <a name="child-elements"></a>Alt Öğeler  
  
|Öğe|Açıklama|  
|-------------|-----------------|  
|[Menus öğesi](../extensibility/menus-element.md)|Tüm bir VSPackage'ı uygulayan araç çubukları ve menüler tanımlar.|  
|[Menü öğesi](../extensibility/menu-element.md)|Tek bir menü veya araç çubuğunu temsil eder.|  
  
### <a name="parent-elements"></a>Üst öğeler  
  
|Öğe|Açıklama|  
|-------------|-----------------|  
|[Commands öğesi](../extensibility/commands-element.md)|VSPackage'ı komutlarında koleksiyonunu temsil eder.|  
  
## <a name="example"></a>Örnek  
  
```xml  
<Commands package="guidMyPackage">  
    <Menus>  
      <Menu Condition="'%(DEBUG)' != 'true'"   
        guid="cmdSetGuidMyProductCommands" id="menuIDMainMenu"   
        priority="0x0000" type="Menu">  
        <Annotation>  
          <Documentation>this is an annotation</Documentation>  
          <AppInfo>  
            <CustomData>  
              <CustomSubElement>Some data</CustomSubElement>  
            </CustomData>  
          </AppInfo>  
        </Annotation>  
        <CommandFlag>AlwaysCreate</CommandFlag>  
        <Strings>  
          <ButtonText>MainMenu</ButtonText>  
        </Strings>  
      </Menu>  
  </Menus>  
<Commands>  
```  
  
## <a name="see-also"></a>Ayrıca bkz.  
 [VSPackage kullanıcı arabirimi öğelerini nasıl eklenir](../extensibility/internals/how-vspackages-add-user-interface-elements.md)   
 [Komutlar, menüler ve araç çubukları](../extensibility/internals/commands-menus-and-toolbars.md)
---
title: Komutlar öğenin | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
f1_keywords:
- Commands
helpviewer_keywords:
- Commands element (VSCT XML schema)
- VSCT XML schema elements, Commands
ms.assetid: 47cf16a5-d78b-452e-86f6-b5893856dddf
author: gregvanl
ms.author: gregvanl
manager: douge
ms.workload:
- vssdk
ms.openlocfilehash: 704a37b1aeb211921b962fd816af89abb686a14e
ms.sourcegitcommit: 37fb7075b0a65d2add3b137a5230767aa3266c74
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/02/2019
ms.locfileid: "53955938"
---
# <a name="commands-element"></a>Commands öğesi
VSPackage araç çubuğundaki komutları koleksiyonunu temsil eder. Koleksiyon en fazla beş alt bölümlerde, aşağıdaki gibi olabilir: menüler, grupları, düğmeler, combos ve bit eşlemler.  
  
 Her alt alt öğesi, örneğin, \<menüsü >, bir GUID ve sayısal tanımlayıcı çifti benzersiz komut Kimliğine göre tanımlanır. GUID "komut kümesini" tanımlayan ve mantıksal olarak ilgili komutları gruplandırmak için kullanılır. VSPackage'ı diğer VSPackages tarafından tanımlanan komut kimlikleri çarpışmalardan kaçınmak için set kendi komutu tanımlamanız gerekir.  
  
## <a name="syntax"></a>Sözdizimi  
  
```xml  
<Commands package="GuidMyPackage" >  
  <Menus>... </Menus>  
  <Groups>... </Groups>  
  <Buttons>... </Buttons>  
  <Combos>... </Combos>  
  <Bitmaps>... </Bitmaps>  
</Commands>  
```  
  
## <a name="attributes-and-elements"></a>Öznitelikler ve öğeler  
 Öznitelikler, alt ve üst öğeler aşağıdaki bölümlerde açıklanmaktadır.  
  
### <a name="attributes"></a>Öznitelikler  
  
|Öznitelik|Açıklama|  
|---------------|-----------------|  
|Paket|VSPackage'ı tanımlayan bir GUID, komutlar sağlar.<br /><br /> Örneğin, paket = "guidVsPackage1Pkg".|  
  
### <a name="child-elements"></a>Alt öğeleri  
  
|Öğe|Açıklama|  
|-------------|-----------------|  
|[Menus öğesi](../extensibility/menus-element.md)|VSPackage'ı uygulayan tüm menüleri tanımlar.|  
|[Groups öğesi](../extensibility/groups-element.md)|VSPackage'ı içinde komut gruplarını tanımlama girişleri içerir.|  
|[Buttons öğesi](../extensibility/buttons-element.md)|Düğme öğelerini gruplandırır.|  
|[Bitmaps öğesi](../extensibility/bitmaps-element.md)|Bit eşlem öğeleri gruplandırır.|  
|[Combos öğesi](../extensibility/combos-element.md)|Birleşik giriş öğelerini gruplandırır.|  
  
### <a name="parent-elements"></a>Üst öğeler  
  
|Öğe|Açıklama|  
|-------------|-----------------|  
|[CommandTable öğesi](../extensibility/commandtable-element.md)|VSPackage sunar IDE'nin komutları temsil eden tüm öğeleri tanımlar. Menü öğeleri, menüler, araç çubukları ve birleşik giriş kutuları Bunun olası öğeleridir.|  
  
## <a name="example"></a>Örnek  
 Aşağıdaki örnek nasıl kullanılacağını gösteren bir [komutlar öğenin](../extensibility/commands-element.md).  
  
```  
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
---
title: Komutlar öğenin | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-sdk
ms.topic: reference
f1_keywords:
- Commands
helpviewer_keywords:
- Commands element (VSCT XML schema)
- VSCT XML schema elements, Commands
ms.assetid: 47cf16a5-d78b-452e-86f6-b5893856dddf
caps.latest.revision: 18
ms.author: gregvanl
manager: jillfra
ms.openlocfilehash: 194768a3b540511996e1d99e6450a7a9b24ebc74
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "68184300"
---
# <a name="commands-element"></a>Commands Öğesi
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

VSPackage araç çubuğundaki komutları koleksiyonunu temsil eder. Koleksiyon en fazla beş alt bölümlerde, aşağıdaki gibi olabilir: menüler, grupları, düğmeler, combos ve bit eşlemler.  
  
 Her alt alt öğesi, örneğin, \<menüsü >, bir GUID ve sayısal tanımlayıcı çifti benzersiz komut Kimliğine göre tanımlanır. GUID "komut kümesini" tanımlayan ve mantıksal olarak ilgili komutları gruplandırmak için kullanılır. VSPackage'ı diğer VSPackages tarafından tanımlanan komut kimlikleri çarpışmalardan kaçınmak için set kendi komutu tanımlamanız gerekir.  
  
## <a name="syntax"></a>Sözdizimi  
  
```  
<Commands package="GuidMyPackage" >  
  <Menus>... </Menus>  
  <Groups>... </Groups>  
  <Buttons>... </Buttons>  
  <Combos>... </Combos>  
  <Bitmaps>... </Bitmaps>  
</Commands>  
```  
  
## <a name="attributes-and-elements"></a>Öznitelikler ve Öğeler  
 Öznitelikler, alt ve üst öğeler aşağıdaki bölümlerde açıklanmaktadır.  
  
### <a name="attributes"></a>Öznitelikler  
  
|Öznitelik|Açıklama|  
|---------------|-----------------|  
|Paket|VSPackage'ı tanımlayan bir GUID, komutlar sağlar.<br /><br /> Örneğin, paket = "guidVsPackage1Pkg".|  
  
### <a name="child-elements"></a>Alt Öğeler  
  
|Öğe|Açıklama|  
|-------------|-----------------|  
|[Menus Öğesi](../extensibility/menus-element.md)|VSPackage'ı uygulayan tüm menüleri tanımlar.|  
|[Groups Öğesi](../extensibility/groups-element.md)|VSPackage'ı içinde komut gruplarını tanımlama girişleri içerir.|  
|[Buttons Öğesi](../extensibility/buttons-element.md)|Düğme öğelerini gruplandırır.|  
|[Bitmaps Öğesi](../extensibility/bitmaps-element.md)|Bit eşlem öğeleri gruplandırır.|  
|[Combos Öğesi](../extensibility/combos-element.md)|Birleşik giriş öğelerini gruplandırır.|  
  
### <a name="parent-elements"></a>Üst Öğeler  
  
|Öğe|Açıklama|  
|-------------|-----------------|  
|[CommandTable Öğesi](../extensibility/commandtable-element.md)|VSPackage sunar IDE'nin komutları temsil eden tüm öğeleri tanımlar. Menü öğeleri, menüler, araç çubukları ve birleşik giriş kutuları Bunun olası öğeleridir.|  
  
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
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [VSPackage kullanıcı arabirimi öğelerini nasıl eklenir](../extensibility/internals/how-vspackages-add-user-interface-elements.md)   
 [Komutlar, Menüler ve Araç Çubukları](../extensibility/internals/commands-menus-and-toolbars.md)

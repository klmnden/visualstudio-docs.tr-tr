---
title: Üst öğe | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-sdk
ms.topic: reference
helpviewer_keywords:
- VSCT XML schema elements, Parent
- Parent element (VSCT XML schema)
ms.assetid: e4624ac8-1b9a-4940-910a-528a661cefad
caps.latest.revision: 9
ms.author: gregvanl
manager: jillfra
ms.openlocfilehash: 2086473bc484fed4e8e351f0c3838074557586c9
ms.sourcegitcommit: 8b538eea125241e9d6d8b7297b72a66faa9a4a47
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54763724"
---
# <a name="parent-element"></a>Üst Öğe
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Bir düğme veya birleşik giriş kutusunun üst yalnızca bir grup olabilir. Bir menü veya grubun üst herhangi bir menü veya grup olabilir. İçinde bir [CommandPlacement öğesi](../extensibility/commandplacement-element.md), bu öğe gereklidir; diğer tüm durumlarda isteğe bağlıdır. Bu öğe atlanırsa, üst `Group_Undefined:0` kapsanan.  
  
## <a name="syntax"></a>Sözdizimi  
  
```  
<Parent guid="guidMyCommandSet" id="MyParentGroupOrMenu" />  
```  
  
## <a name="attributes-and-elements"></a>Öznitelikler ve Öğeler  
 Öznitelikler, alt ve üst öğeler aşağıdaki bölümlerde açıklanmaktadır.  
  
### <a name="attributes"></a>Öznitelikler  
  
|Öznitelik|Açıklama|  
|---------------|-----------------|  
|GUID|Gerekli. GUID GUID/kimliği komut tanımlayıcısı.|  
|kimlik|Gerekli. Kimliği GUID/kimliği komut tanımlayıcısı.|  
  
### <a name="child-elements"></a>Alt Öğeler  
 Hiçbiri  
  
### <a name="parent-elements"></a>Üst Öğeler  
  
|Öğe|Açıklama|  
|-------------|-----------------|  
|[CommandTable Öğesi](../extensibility/commandtable-element.md)|VSPackage sağlayan komutlar tümleşik geliştirme ortamı (IDE) temsil eden tüm öğeleri tanımlar. Örneğin, menü öğeleri, menüler, araç çubukları ve birleşik giriş kutuları.|  
|[Buttons Öğesi](../extensibility/buttons-element.md)|Grupları [Button öğesi](../extensibility/button-element.md) öğeleri.|  
|[Menus Öğesi](../extensibility/menus-element.md)|VSPackage'ı uygulayan tüm menüleri tanımlar.|  
|[Groups Öğesi](../extensibility/groups-element.md)|VSPackage komut gruplarını tanımlar girişleri içerir.|  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Visual Studio Komut Tablosu (.Vsct) Dosyaları](../extensibility/internals/visual-studio-command-table-dot-vsct-files.md)

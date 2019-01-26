---
title: CustomParameters öğesi (Visual Studio şablonları) | Microsoft Docs
ms.date: 11/04/2016
ms.technology: vs-ide-general
ms.topic: reference
f1_keywords:
- http://schemas.microsoft.com/developer/vstemplate/2005#CustomParameters
helpviewer_keywords:
- CustomParameters element [Visual Studio project templates]
ms.assetid: cf3efc91-1532-4022-bbb8-a18658424fee
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: 1f3816943ca3779b9110de2359fd10852330eb20
ms.sourcegitcommit: 2193323efc608118e0ce6f6b2ff532f158245d56
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/25/2019
ms.locfileid: "54940264"
---
# <a name="customparameters-element-visual-studio-templates"></a>CustomParameters öğesi (Visual Studio şablonları)
Sihirbaz parametresi değişiklik yaptığında için Şablon Sihirbazı'nı geçirilecek özel parametreler gruplandırır.  
  
## <a name="syntax"></a>Sözdizimi  
  
```  
<CustomParameters>  
    <CustomParameter/>  
    <CustomParameter/>  
</CustomParameters>  
```  
  
## <a name="attributes-and-elements"></a>Öznitelikler ve öğeler  
 Öznitelikler, alt ve üst öğeler aşağıdaki bölümlerde açıklanmaktadır.  
  
### <a name="attributes"></a>Öznitelikler  
 Yok.  
  
### <a name="child-elements"></a>Alt öğeleri  
  
|Öğe|Açıklama|  
|-------------|-----------------|  
|[CustomParameter](../extensibility/customparameter-element-visual-studio-templates.md)|İsteğe bağlı öğe.<br /><br /> Bir özel parametre adı ve şablondan bir proje veya öğe oluşturulduğunda kullanılacak değeri içerir. Sıfır veya daha fazla olabilir `CustomParameter` öğelerinde bir `CustomParameters` öğesi.|  
  
### <a name="parent-elements"></a>Üst öğeler  
  
|Öğe|Açıklama|  
|-------------|-----------------|  
|[TemplateContent](../extensibility/templatecontent-element-visual-studio-templates.md)|Şablonu içeriğini belirtir.|  
  
## <a name="remarks"></a>Açıklamalar  
  
## <a name="example"></a>Örnek  
 Aşağıdaki örnek, şablonda birkaç özel parametreler kullanmayı gösterir. Bir proje veya öğe oluşturulduğunda aşağıdaki özel parametreleri, tüm örneklerini ile bir şablondan `$color1$` ve `$color2$` şablon dosyaları ile değiştirilecek `Red` ve `Blue`sırasıyla.  
  
```  
<CustomParameters>  
    <CustomParameter Name="$color1$" Value="Red"/>  
    <CustomParameter Name="$color2$" Value="Blue "/>  
</CustomParameters>  
```  
  
## <a name="see-also"></a>Ayrıca bkz.  
 [CustomParameter öğesi (Visual Studio şablonları)](../extensibility/customparameter-element-visual-studio-templates.md)   
 [Şablon parametreleri](../ide/template-parameters.md)   
 [Visual Studio Şablon Şeması Başvurusu](../extensibility/visual-studio-template-schema-reference.md)
---
title: RequiredPlatformVersion öğesi (Visual Studio şablonları) | Microsoft Docs
ms.date: 11/04/2016
ms.technology: vs-ide-general
ms.topic: reference
ms.assetid: 6f0e4986-3157-4bba-aed3-c28413ebe976
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: b04a4332169f2f7ae57daaaeebb8a71ea0fafc72
ms.sourcegitcommit: 2193323efc608118e0ce6f6b2ff532f158245d56
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/25/2019
ms.locfileid: "54947510"
---
# <a name="requiredplatformversion-element-visual-studio-templates"></a>RequiredPlatformVersion öğesi (Visual Studio şablonları)
Proje şablonu düzgün çalışması için gerekli işletim sistemi en düşük sürümünü belirtir. Bu öğe oluşturmak için proje şablonları kullanılan [!INCLUDE[win8_appname_long](../debugger/includes/win8_appname_long_md.md)] uygulamalar.  
  
 `RequiredPlatformVersion` Değeri doğrudan işletim sistemi sürümü ile karşılaştırılır. Varsa `RequiredPlatformVersion` işletim sistemi sürümünden daha yüksek olan şablon görünmez **yeni proje** iletişim kutusu. Bir şablon için belirttiğiniz için [!INCLUDE[win8](../debugger/includes/win8_md.md)] veya üzeri olarak ayarlayın `RequiredPlatformVersion` 6.2.0 için. Bir şablon için belirttiğiniz için [!INCLUDE[win81](../debugger/includes/win81_md.md)] veya üzeri olarak ayarlayın `RequiredPlatformVersion` 6.3.0 için.  
  
 Belirten şablonları `RequiredPlatformVersion`= 8 önceki müşteri ile uyumlu [!INCLUDE[win8_appname_long](../debugger/includes/win8_appname_long_md.md)] şablonları.  
  
 VSTemplate  
TemplateData  
.....TargetPlatformName  
RequiredPlatformVersion  
  
## <a name="syntax"></a>Sözdizimi  
  
```xml  
<RequiredPlatformVersion> OperatingSystem </RequiredPlatformVersion>  
```  
  
## <a name="attributes-and-elements"></a>Öznitelikler ve öğeler  
 Yok.  
  
### <a name="attributes"></a>Öznitelikler  
 Yok.  
  
### <a name="child-elements"></a>Alt öğeleri  
 Yok.  
  
### <a name="parent-elements"></a>Üst öğeler  
  
|Öğe|Açıklama|  
|-------------|-----------------|  
|[TemplatePlatformName](../extensibility/templatedata-element-visual-studio-templates.md)|Platformunu belirtir, proje şablonu hedefler.|  
  
## <a name="text-value"></a>Metin değeri  
 Bir metin değeri gereklidir.  
  
## <a name="remarks"></a>Açıklamalar  
 Bu metin şablon için gerekli en düşük işletim sistemi sürümünü belirtir.  
  
## <a name="example"></a>Örnek  
 Bu örnekte belirten proje şablonunun hedeflediği [!INCLUDE[win8](../debugger/includes/win8_md.md)] veya üzeri.  
  
```xml  
<VSTemplate Type="Project" Version="3.0.0"    xmlns="http://schemas.microsoft.com/developer/vstemplate/2005">  
    <TemplateData>  
        <TargetPlatformName>Windows</TargetPlatformName>  
            <RequiredPlatformVersion>6.3.0</RequiredPlatformVersion>  
  
    </TemplateData>  
    <TemplateContent>  
  
    </TemplateContent>  
</VSTemplate>  
```  
  
## <a name="see-also"></a>Ayrıca bkz.  
 [TargetPlatformName öğesi (Visual Studio şablonları)](../extensibility/targetplatformname-element-visual-studio-templates.md)   
 [Proje ve öğe şablonları oluşturma](../ide/creating-project-and-item-templates.md)   
 [Visual Studio Şablon Şeması Başvurusu](../extensibility/visual-studio-template-schema-reference.md)
---
title: Templateıd öğesi (Visual Studio şablonları) | Microsoft Docs
ms.date: 11/04/2016
ms.technology: vs-ide-general
ms.topic: reference
f1_keywords:
- http://schemas.microsoft.com/developer/vstemplate/2005#TemplateID
helpviewer_keywords:
- <TemplateID> element [Visual Studio Templates]
- TemplateID element [Visual Studio Templates]
ms.assetid: 6ca24b4e-0325-4a9e-855e-0cbbe7361d8f
author: gregvanl
ms.author: gregvanl
manager: douge
ms.workload:
- vssdk
ms.openlocfilehash: 8bbd9bddaeab9d073affb35a1b275f0eef7afe99
ms.sourcegitcommit: 37fb7075b0a65d2add3b137a5230767aa3266c74
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/02/2019
ms.locfileid: "53874076"
---
# <a name="templateid-element-visual-studio-templates"></a>TemplateID Öğesi (Visual Studio Şablonları)
Bir gruba öğe şablonları tarafından kategorilere ayrılmıştır bir öğe şablonu için bir tanımlayıcı belirtir [Templategroupıd](../extensibility/templategroupid-element-visual-studio-templates.md) öğesi.  
  
 \<VSTemplate >  
 \<TemplateData >  
 \<Templateıd >  
  
## <a name="syntax"></a>Sözdizimi  
  
```  
<TemplateID> ... </TemplateID>  
```  
  
## <a name="attributes-and-elements"></a>Öznitelikler ve Öğeler  
 Öznitelikler, alt ve üst öğeler aşağıdaki bölümlerde açıklanmaktadır.  
  
### <a name="attributes"></a>Öznitelikler  
 Yok.  
  
### <a name="child-elements"></a>Alt Öğeler  
 Yok.  
  
### <a name="parent-elements"></a>Üst Öğeler  
  
|Öğe|Açıklama|  
|-------------|-----------------|  
|[TemplateData](../extensibility/templatedata-element-visual-studio-templates.md)|Gerekli öğe.<br /><br /> Şablonu kategorilere ayırır ve nasıl görüntülendiğini tanımlar **yeni proje** veya **Yeni Öğe Ekle** iletişim kutusu.|  
  
## <a name="text-value"></a>Metin Değeri  
 A `string` temsil eden öğe şablonları tarafından bir grup halinde kategorilere ayrılmıştır bir öğe şablonu için bir tanımlayıcı `TemplateGroupID` öğesi.  
  
## <a name="remarks"></a>Açıklamalar  
 `TemplateID` İsteğe bağlı bir öğedir.  
  
 .Vstemplate dosyası çıkarırsa `TemplateID` öğesi, ardından [adı](../extensibility/name-element-visual-studio-templates.md) öğe şablonu tanımlayıcı olarak kullanılır.  
  
 Değerini `TemplateID` öğesi, proje sistemi kaydı ile birlikte kullanılır (HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\VisualStudio\11.0\Projects\\) görünen filtre şablonlarına **Add New Item** iletişim kutusu.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Visual Studio Şablon Şeması Başvurusu](../extensibility/visual-studio-template-schema-reference.md)   
 [Proje ve Öğe Şablonları Oluşturma](../ide/creating-project-and-item-templates.md)
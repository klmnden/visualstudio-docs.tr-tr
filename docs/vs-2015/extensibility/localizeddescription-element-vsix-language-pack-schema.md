---
title: LocalizedDescription öğesi (VSIX Dil Paketi Şeması) | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-sdk
ms.topic: reference
ms.assetid: 766a1732-bbaf-4875-b276-feb42169633a
caps.latest.revision: 9
ms.author: gregvanl
manager: jillfra
ms.openlocfilehash: 281f3823d22ee0e290e4b6bb32a8280f4773a592
ms.sourcegitcommit: 08fc78516f1107b83f46e2401888df4868bb1e40
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/15/2019
ms.locfileid: "65679903"
---
# <a name="localizeddescription-element-vsix-language-pack-schema"></a>LocalizedDescription öğesi (VSIX Dil Paketi Şeması)
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Gerekli. Uzantının yerelleştirilmiş bir açıklama sağlar.  
  
## <a name="syntax"></a>Sözdizimi  
  
```  
<LocalizedDescription>Localized description of the extension</LocalizedDescription>  
```  
  
## <a name="attributes-and-elements"></a>Öznitelikler ve Öğeler  
 Öznitelikler, alt ve üst öğeler aşağıdaki bölümlerde açıklanmaktadır.  
  
### <a name="attributes"></a>Öznitelikler  
  
|Öznitelik|Açıklama|  
|---------------|-----------------|  
|Yok.||  
  
### <a name="child-elements"></a>Alt Öğeler  
  
|Öğe|Açıklama|  
|-------------|-----------------|  
|None||  
  
### <a name="parent-elements"></a>Üst Öğeler  
  
|Öğe|Açıklama|  
|-------------|-----------------|  
|[VSIX LanguagePack Öğesi](../extensibility/vsixlanguagepack-element-vsix-language-pack-schema.md)|Gerekli. VSIX Dil Paketi için kök öğe sağlar.|  
  
## <a name="text-value"></a>Metin Değeri  
 Gerekli. Hedef Dil uzantısında metin açıklaması.  
  
## <a name="element-information"></a>Öğe Bilgisi  
  
|                 |                                                           |
|-----------------|-----------------------------------------------------------|
|    Ad Alanı    | http://schemas.microsoft.com/developer/vsx-schema-lp/2010 |
|   Şema adı   |                 VSIX Dil Paketi şeması                 |
| Doğrulama dosyası |                VSIXLanguagePackSchema.xsd                 |
|  Boş olabilir.   |                      Geçerli değil                       |
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [VSX dil paketi Şeması Başvurusu](../extensibility/vsx-language-pack-schema-reference.md)   
 [VSIX paketlerini yerelleştirme](../extensibility/localizing-vsix-packages.md)   
 [VSIX Uzantı Şeması 1.0 başvurusu](https://msdn.microsoft.com/76e410ec-b1fb-4652-ac98-4a4c52e09a2b)

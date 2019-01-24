---
title: LocalizedName öğesi (VSIX Dil Paketi Şeması) | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-sdk
ms.topic: reference
ms.assetid: 57b7f502-3b04-42d9-90d5-f57772a7c757
caps.latest.revision: 8
ms.author: gregvanl
manager: jillfra
ms.openlocfilehash: 0747dfe89c2d8d4ceb8321f00f723f973f3ff526
ms.sourcegitcommit: 8b538eea125241e9d6d8b7297b72a66faa9a4a47
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54783719"
---
# <a name="localizedname-element-vsix-language-pack-schema"></a>LocalizedName öğesi (VSIX Dil Paketi Şeması)
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Gerekli. Uzantının yüklenmesini yerelleştirilmiş adı.  
  
## <a name="syntax"></a>Sözdizimi  
  
```  
<Name>Localized name of the extension</Name>  
```  
  
## <a name="attributes-and-elements"></a>Öznitelikler ve Öğeler  
 Öznitelikler, alt ve üst öğeler aşağıdaki bölümlerde açıklanmaktadır.  
  
### <a name="attributes"></a>Öznitelikler  
  
|Öznitelik|Açıklama|  
|---------------|-----------------|  
|Hiçbiri||  
  
### <a name="child-elements"></a>Alt Öğeler  
  
|Öğe|Açıklama|  
|-------------|-----------------|  
|Hiçbiri||  
  
### <a name="parent-elements"></a>Üst Öğeler  
  
|Öğe|Açıklama|  
|-------------|-----------------|  
|[VSIX LanguagePack Öğesi](../extensibility/vsixlanguagepack-element-vsix-language-pack-schema.md)|Gerekli. VSIX Dil Paketi için kök öğe sağlar.|  
  
## <a name="text-value"></a>Metin Değeri  
 Gerekli. Dil paketi hedef dil adı.  
  
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
 [VSIX Uzantı Şeması 1.0 başvurusu](http://msdn.microsoft.com/76e410ec-b1fb-4652-ac98-4a4c52e09a2b)

---
title: VSIXLanguagePack öğesi (VSIX Dil Paketi Şeması) | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-sdk
ms.topic: reference
ms.assetid: 767f5c22-8b87-49ca-92aa-a7a3f026469f
caps.latest.revision: 9
ms.author: gregvanl
manager: jillfra
ms.openlocfilehash: 7b4ba4e98b8b2d42485a7594d5bab658e1bd6ccb
ms.sourcegitcommit: 8b538eea125241e9d6d8b7297b72a66faa9a4a47
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54786099"
---
# <a name="vsixlanguagepack-element-vsix-language-pack-schema"></a>VSIXLanguagePack öğesi (VSIX Dil Paketi Şeması)
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Gerekli. VSIX Dil Paketi için kök öğe sağlar. VSIX Dil Paketi, bir VSIX paketi için yerelleştirilmiş yükleme bilgilerini sağlar.  
  
## <a name="syntax"></a>Sözdizimi  
  
```  
<VSIXLanguagePack>  
  <LocalizedName>...</LocalizedName>  
  <LocalizedDescription>...</LocalizedDescription>  
  <MoreInfoURL>...</MoreInfoURL>  
  <License>...</License>  
</VSIXLanguagePack>  
```  
  
## <a name="attributes-and-elements"></a>Öznitelikler ve Öğeler  
 Öznitelikler, alt ve üst öğeler aşağıdaki bölümlerde açıklanmaktadır.  
  
### <a name="attributes"></a>Öznitelikler  
  
|Öznitelik|Açıklama|  
|---------------|-----------------|  
|`xmlns`|VSIX Dil Paketi şeması tanımlandığı XML ad alanı.|  
  
## <a name="xmlns-attribute"></a>xmlns özniteliğinin  
  
|Değer|Açıklama|  
|-----------|-----------------|  
|`http://schemas.microsoft.com/developer/vsx-schema-lp/2010`|Gerekli. Dil paketleri şemasını tanımlayan dosyasının konumu.|  
  
### <a name="child-elements"></a>Alt Öğeler  
  
|Öğe|Açıklama|  
|-------------|-----------------|  
|[LocalizedName Öğesi](../extensibility/localizedname-element-vsix-language-pack-schema.md)|Gerekli. Uzantının yüklenmesini yerelleştirilmiş adı.|  
|[LocalizedDescription Öğesi](../extensibility/localizeddescription-element-vsix-language-pack-schema.md)|Gerekli. Yerelleştirilmiş açıklama uzantısının yüklenmesi.|  
|[MoreInfoURL Öğesi](../extensibility/moreinfourl-element-vsix-language-pack-schema.md)|İsteğe bağlı. Yerelleştirilmiş uzantısı hakkında bilgi almak için bir bağlantı.|  
|[License Öğesi](../extensibility/license-element-vsix-language-pack-schema.md)|İsteğe bağlı. Uzantının lisans dosyası yerelleştirilmiş bir sürümünü yolu.|  
  
### <a name="parent-elements"></a>Üst Öğeler  
  
|Öğe|Açıklama|  
|-------------|-----------------|  
|Hiçbiri||  
  
## <a name="element-information"></a>Öğe Bilgisi  
  
|                 |                                                           |
|-----------------|-----------------------------------------------------------|
|    Ad Alanı    | http://schemas.microsoft.com/developer/vsx-schema-lp/2010 |
|   Şema adı   |                 VSIX Dil Paketi şeması                 |
| Doğrulama dosyası |                VSIXLanguagePackSchema.xsd                 |
|  Boş olabilir.   |                            Hayır                             |
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [VSX dil paketi Şeması Başvurusu](../extensibility/vsx-language-pack-schema-reference.md)   
 [VSIX paketlerini yerelleştirme](../extensibility/localizing-vsix-packages.md)   
 [VSIX Uzantı Şeması 1.0 başvurusu](http://msdn.microsoft.com/76e410ec-b1fb-4652-ac98-4a4c52e09a2b)

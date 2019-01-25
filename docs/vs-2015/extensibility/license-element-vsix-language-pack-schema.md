---
title: Lisans öğesi (VSIX Dil Paketi Şeması) | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-sdk
ms.topic: reference
ms.assetid: 57dac3b7-0cdd-405c-9af5-30ed9ca45e53
caps.latest.revision: 9
ms.author: gregvanl
manager: jillfra
ms.openlocfilehash: a3a46e772849646a82d70ce9a68491d0b388b6c1
ms.sourcegitcommit: 8b538eea125241e9d6d8b7297b72a66faa9a4a47
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54763733"
---
# <a name="license-element-vsix-language-pack-schema"></a>Lisans öğesi (VSIX Dil Paketi Şeması)
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

İsteğe bağlı. Uzantının lisans dosyası yerelleştirilmiş bir sürümünü yolu.  
  
## <a name="syntax"></a>Sözdizimi  
  
```  
<License>FilePath\license.txt</License>  
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
 Görüntülenecek yerelleştirilmiş lisans dosyasının göreli yolu.  
  
## <a name="remarks"></a>Açıklamalar  
 Varsa `License` öğesinin tanımlanmış, ardından Kurulum sırasında belirtilen lisans dosyasını metni görüntülenir ve kullanıcı devam etmek için lisans kabul etmelidir.  
  
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

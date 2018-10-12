---
title: ButtonText öğesi | Microsoft Docs
ms.custom: ''
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.reviewer: ''
ms.suite: ''
ms.technology:
- vs-ide-sdk
ms.tgt_pltfrm: ''
ms.topic: article
helpviewer_keywords:
- ButtonText element (VSCT XML schema)
- VSCT XML schema elements, ButtonText
ms.assetid: 56aba884-0356-4894-ae4e-32d3938f6865
caps.latest.revision: 7
ms.author: gregvanl
manager: ghogen
ms.openlocfilehash: f5ec72ffd7d0cc96b1ce66098efcfbda4fc30390
ms.sourcegitcommit: 9ceaf69568d61023868ced59108ae4dd46f720ab
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/12/2018
ms.locfileid: "49255339"
---
# <a name="buttontext-element"></a>ButtonText Öğesi
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Bu alan çeşitli menülerde görüntülenen metin belirtmenize olanak sağlar. Varsayılan olarak, `ButtonText` öğesi menüsü denetleyicileri görünür. `ButtonText` Öğesi diğer metin alanları boş ise varsayılan ayrıca olur. `ButtonText` Bile diğer metin alanları öğesi boş olamaz.  
  
## <a name="syntax"></a>Sözdizimi  
  
```  
<ButtonText>My Command</ButtonText>  
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
|[Strings Öğesi](../extensibility/strings-element.md)|Metin öğeleri gibi gruplar `ButtonText` ve `CommandName`.|  
  
## <a name="text-value"></a>Metin Değeri  
 Metin değeri `ButtonText` öğesi menü öğeleri, combos ve görünen metin sahip diğer kullanıcı arabirimi (UI) öğeleri için görüntülenen metni sağlar.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Visual Studio Komut Tablosu (.Vsct) Dosyaları](../extensibility/internals/visual-studio-command-table-dot-vsct-files.md)


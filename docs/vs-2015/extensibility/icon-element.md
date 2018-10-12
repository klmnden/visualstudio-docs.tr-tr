---
title: Icon öğesi | Microsoft Docs
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
- VSCT XML schema elements, Icon
- Icon element (VSCT XML schema)
ms.assetid: 73c58fe3-d53c-4f4e-b025-29567c6cbb7c
caps.latest.revision: 6
ms.author: gregvanl
manager: ghogen
ms.openlocfilehash: 31a6e0cf18422118c184f290fc8200d9c9263356
ms.sourcegitcommit: 9ceaf69568d61023868ced59108ae4dd46f720ab
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/12/2018
ms.locfileid: "49186686"
---
# <a name="icon-element"></a>Icon Öğesi
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Guid özniteliği simge etiketi, tanımlı bir bit eşlem GUID'dir.  ID özniteliği, bit eşlem şeridinde yuvası seçer. Bu öğe isteğe bağlıdır.  Bu öğe atlanırsa değerini **guidOfficeIcon:msotcidNoIcon** kapsanan.  
  
## <a name="syntax"></a>Sözdizimi  
  
```  
<Icon guid="guidImages" id="bmpPic1" />  
```  
  
## <a name="attributes-and-elements"></a>Öznitelikler ve Öğeler  
 Öznitelikler, alt ve üst öğeler aşağıdaki bölümlerde açıklanmaktadır.  
  
### <a name="attributes"></a>Öznitelikler  
  
|Öznitelik|Açıklama|  
|---------------|-----------------|  
|GUID|Gerekli. Tanımlı bir bit eşlem guid'si.|  
|kimlik|Gerekli. Yuva bit eşlem şeridinde seçer.|  
  
### <a name="child-elements"></a>Alt Öğeler  
  
|Öğe|Açıklama|  
|-------------|-----------------|  
|Yok.|Yok.|  
  
### <a name="parent-elements"></a>Üst Öğeler  
  
|Öğe|Açıklama|  
|-------------|-----------------|  
|[Buttons Öğesi](../extensibility/buttons-element.md)||  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Visual Studio Komut Tablosu (.Vsct) Dosyaları](../extensibility/internals/visual-studio-command-table-dot-vsct-files.md)


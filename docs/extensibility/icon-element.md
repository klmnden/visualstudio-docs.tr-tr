---
title: Icon öğesi | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
helpviewer_keywords:
- VSCT XML schema elements, Icon
- Icon element (VSCT XML schema)
ms.assetid: 73c58fe3-d53c-4f4e-b025-29567c6cbb7c
author: gregvanl
ms.author: gregvanl
manager: douge
ms.workload:
- vssdk
ms.openlocfilehash: 475bca35ca1bdc1879301912c7ddd271f369a6ef
ms.sourcegitcommit: 37fb7075b0a65d2add3b137a5230767aa3266c74
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/02/2019
ms.locfileid: "53870014"
---
# <a name="icon-element"></a>Icon öğesi
Guid özniteliği simge etiketi, tanımlı bir bit eşlem GUID'dir. `id` Özniteliği, bit eşlem şeridinde yuvası seçer. Bu öğe isteğe bağlıdır. Bu öğe değilse, değeri dahil **guidOfficeIcon:msotcidNoIcon** kapsanan.  
  
## <a name="syntax"></a>Sözdizimi  
  
```xml  
<Icon guid="guidImages" id="bmpPic1" />  
```  
  
## <a name="attributes-and-elements"></a>Öznitelikler ve öğeler  
 Öznitelikler, alt ve üst öğeler aşağıdaki bölümlerde açıklanmaktadır.  
  
### <a name="attributes"></a>Öznitelikler  
  
|Öznitelik|Açıklama|  
|---------------|-----------------|  
|GUID|Gerekli. Tanımlı bir bit eşlem guid'si.|  
|kimlik|Gerekli. Yuva bit eşlem şeridinde seçer.|  
  
### <a name="child-elements"></a>Alt öğeleri  
  
|Öğe|Açıklama|  
|-------------|-----------------|  
|Yok.|Yok.|  
  
### <a name="parent-elements"></a>Üst öğeler  
  
|Öğe|Açıklama|  
|-------------|-----------------|  
|[Buttons öğesi](../extensibility/buttons-element.md)||  
  
## <a name="see-also"></a>Ayrıca bkz.  
 [Visual Studio komut tablosu (.vsct) dosyaları](../extensibility/internals/visual-studio-command-table-dot-vsct-files.md)
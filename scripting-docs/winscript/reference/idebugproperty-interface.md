---
title: Idebugproperty arabirimi | Microsoft Docs
ms.custom: ''
ms.date: 01/18/2017
ms.prod: windows-script-interfaces
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
helpviewer_keywords:
- IDebugProperty interface
ms.assetid: 7e8f5341-23ef-4029-814d-f5c2307b9203
caps.latest.revision: 8
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: 2e5e5274e8a3d1c81ce010afc3893b27510a0fad
ms.sourcegitcommit: 8bf9e51c77a5a602fab9513b9187e59e57dfebad
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/16/2019
ms.locfileid: "54348366"
---
# <a name="idebugproperty-interface"></a>IDebugProperty Arabirimi
Adı, türü ve değeri içeren hiyerarşik özelliği ayıklanan varlık tanımlamak için kullanılır. En yaygın olarak, `IDebugProperty` ifade değerlendirme, ifade değerlendirme veya kayıt değerlendirme sonucu tanımlamak için kullanılır.  
  
## <a name="methods-in-vtable-order"></a>Vtable sırayla yöntemleri  
 Aşağıdaki tabloda yöntemlerini gösterilmektedir `IDebugProperty` arabirimi.  
  
|Yöntem|Açıklama|  
|------------|-----------------|  
|[IDebugProperty::GetPropertyInfo](../../winscript/reference/idebugproperty-getpropertyinfo.md)|Alma `DebugPropertyInfo` bu açıklar `IDebugProperty``.`|  
|[IDebugProperty::GetExtendedInfo](../../winscript/reference/idebugproperty-getextendedinfo.md)|Genişletilmiş bir özellik bilgileri alır.|  
|[IDebugProperty::SetValueAsString](../../winscript/reference/idebugproperty-setvalueasstring.md)|Bir dizedeki bir özelliğin değerini ayarlar.|  
|[IDebugProperty::EnumMembers](../../winscript/reference/idebugproperty-enummembers.md)|Bir özellik üyesi numaralandırır.|  
|[IDebugProperty::GetParent](../../winscript/reference/idebugproperty-getparent.md)|Bir özelliğin üst alır.|  
  
## <a name="requirements"></a>Gereksinimler  
 Üstbilgi: dbgprop.h
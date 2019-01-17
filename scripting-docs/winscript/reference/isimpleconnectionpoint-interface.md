---
title: Isimpleconnectionpoint arabirimi | Microsoft Docs
ms.custom: ''
ms.date: 01/18/2017
ms.prod: windows-script-interfaces
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
helpviewer_keywords:
- ISimpleConnectionPoint interface
ms.assetid: f632a82f-942d-4291-963e-e9fa2b162493
caps.latest.revision: 8
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: 4a756fa3f933f4adff56c41a86aee19a0a2a93aa
ms.sourcegitcommit: 8bf9e51c77a5a602fab9513b9187e59e57dfebad
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/16/2019
ms.locfileid: "54346416"
---
# <a name="isimpleconnectionpoint-interface"></a>ISimpleConnectionPoint Arabirimi
Açıklayan ve belirli bir bağlantı noktasında harekete geçirilen olayları numaralandırma için basit bir yol sağlar. Bu arabirim de takma kolaylaştırır bir `IDispatch` olaylar için nesne. Bu arabirim, işlem hata ayıklama Yöneticisi (PDM) tarafından uygulanan ve komut dosyası motoru tarafından kullanılan.  
  
 Bu arabirim kullanılabilir `IDebugHelper::CreateSimpleConnectionPoint`.  
  
 Devralınan yöntemleri yanı sıra `IUnknown`, `ISimpleConnectionPoint` arabirimi aşağıdaki yöntemleri sunar.  
  
## <a name="methods-in-vtable-order"></a>Vtable sırayla yöntemleri  
  
|Yöntem|Açıklama|  
|------------|-----------------|  
|[ISimpleConnectionPoint::Advise](../../winscript/reference/isimpleconnectionpoint-advise.md)|Basit bir bağlantı noktası nesnesi ve istemcinin havuzu arasında bir bağlantı kurar.|  
|[ISimpleConnectionPoint::DescribeEvents](../../winscript/reference/isimpleconnectionpoint-describeevents.md)|Olaylar belirtilen bir aralıktaki DISPID ve her olay için adı döndürür.|  
|[ISimpleConnectionPoint::GetEventCount](../../winscript/reference/isimpleconnectionpoint-geteventcount.md)|Bu arabirimde kullanıma sunulan olay sayısını döndürür.|  
|[ISimpleConnectionPoint::Unadvise](../../winscript/reference/isimpleconnectionpoint-unadvise.md)|Daha önce yoluyla kurulmuş bir danışmanlık bağlantıyı sonlandırır `ISimpleConnectionPoint::Advise`.|  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [IDebugProperty Arabirimi](../../winscript/reference/idebugproperty-interface.md)
---
title: Isimpleconnectionpoint arabirimi | Microsoft Docs
ms.custom: ''
ms.date: 01/18/2017
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
ms.openlocfilehash: 0d18c8f9eef6ddb1a38473eb19984bd9cf7dbd96
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "63001509"
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
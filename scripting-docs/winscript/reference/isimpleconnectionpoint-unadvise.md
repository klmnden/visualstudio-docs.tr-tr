---
title: ISimpleConnectionPoint::Unadvise | Microsoft Docs
ms.custom: ''
ms.date: 01/18/2017
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
apiname:
- ISimpleConnectionPoint.Unadvise
apilocation:
- pdm.dll
helpviewer_keywords:
- ISimpleConnectionPoint::Unadvise
ms.assetid: eae06a58-ed42-4839-aad4-14420b15343f
caps.latest.revision: 8
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: 189c07c10e93df9a61218b6a94a0b317999676d2
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "63001499"
---
# <a name="isimpleconnectionpointunadvise"></a>ISimpleConnectionPoint::Unadvise
Daha önce yoluyla kurulmuş bir danışmanlık bağlantıyı sonlandırır `ISimpleConnectionPoint::Advise`.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp
HRESULT Unadvise(  
   DWORD  dwCookie  
);  
```  
  
#### <a name="parameters"></a>Parametreler  
 `dwCookie`  
 [in] Döndürülen sonlandırmak için bağlantı belirteci `ISimpleConnectionPoint::Advise`.  
  
## <a name="return-value"></a>Dönüş Değeri  
 Yöntem döndürür bir `HRESULT`. Olası değerler aşağıdaki tablodakileri içerir, ancak bunlarla da sınırlı değildir:  
  
|Değer|Açıklama|  
|-----------|-----------------|  
|`S_OK`|Yöntem başarılı oldu.|  
  
## <a name="remarks"></a>Açıklamalar  
 Danışmanlık bir bağlantı sonlandırıldığında bağlantı noktası çağrıları `Release` bağlantı sırasında kaydedilmiş işaretçinin yöntemi `ISimpleConnectionPoint::Advise` yöntemi. Çevirmelerinin çağrı `AddRef` sırasında gerçekleştirildi `ISimpleConnectionPoint::Advise` danışmanlık havuz 's çağırdığında bağlantı noktası `QueryInterface`.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [ISimpleConnectionPoint Arabirimi](../../winscript/reference/isimpleconnectionpoint-interface.md)
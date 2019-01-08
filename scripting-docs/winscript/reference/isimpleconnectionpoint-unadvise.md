---
title: ISimpleConnectionPoint::Unadvise | Microsoft Docs
ms.custom: ''
ms.date: 01/18/2017
ms.prod: windows-script-interfaces
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
ms.openlocfilehash: 83fdf8f6a6e9378d328a9df61b1561a1ae747ae8
ms.sourcegitcommit: 116e9614867e0b3c627ce9001012a4c39435a42b
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/08/2019
ms.locfileid: "54089277"
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
---
title: ISimpleConnectionPoint::DescribeEvents | Microsoft Docs
ms.custom: ''
ms.date: 01/18/2017
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
apiname:
- ISimpleConnectionPoint.DescribeEvents
apilocation:
- pdm.dll
helpviewer_keywords:
- ISimpleConnectionPoint::DescribeEvents
ms.assetid: 659ea05f-d41e-424a-bb38-df7672b2d135
caps.latest.revision: 8
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: 1b5824f945ad25f177fc169b58157377bf53bcce
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62786425"
---
# <a name="isimpleconnectionpointdescribeevents"></a>ISimpleConnectionPoint::DescribeEvents
Olaylar belirtilen bir aralıktaki DISPID ve her olay için adı döndürür.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp
HRESULT DescribeEvents(  
   ULONG    iEvent,  
   ULONG    cEvents,  
   DISPID*  prgid,  
   BSTR*    prgbstr,  
   ULONG*   pcEventsFetched  
);  
```  
  
#### <a name="parameters"></a>Parametreler  
 `iEvent`  
 [in] Alınacak ilk olay dizini.  
  
 `cEvents`  
 [in] Alınacak olay sayısı.  
  
 `prgid`  
 [out] Olay DISPID değerleri dizisi.  
  
 `prgbstr`  
 [out] Olay adları dizisi.  
  
 `pcEventsFetched`  
 [out] Alınan olayları gerçek sayısı.  
  
## <a name="return-value"></a>Dönüş Değeri  
 Yöntem döndürür bir `HRESULT`. Olası değerler aşağıdaki tablodakileri içerir, ancak bunlarla da sınırlı değildir:  
  
|Değer|Açıklama|  
|-----------|-----------------|  
|`S_OK`|Yöntem başarılı oldu.|  
|`S_FALSE`|Daha fazla olay, kullanılabilir olan çok istendi. Kullanılabilir olaylar DISPID_NULL ve null BSTR ile temsil edilir.|  
|`E_INVALIDARG`|Hiçbir öğe getirilmeden.|  
  
## <a name="remarks"></a>Açıklamalar  
 Bu yöntem, olayları belirtilen bir aralıktaki her olay için adı ve DISPID döndürür.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [ISimpleConnectionPoint Arabirimi](../../winscript/reference/isimpleconnectionpoint-interface.md)
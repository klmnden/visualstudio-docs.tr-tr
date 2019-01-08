---
title: ISimpleConnectionPoint::DescribeEvents | Microsoft Docs
ms.custom: ''
ms.date: 01/18/2017
ms.prod: windows-script-interfaces
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
ms.openlocfilehash: 43a20a2d9580c80bc6aea5d22c6a0713f4843634
ms.sourcegitcommit: 116e9614867e0b3c627ce9001012a4c39435a42b
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/08/2019
ms.locfileid: "54088510"
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
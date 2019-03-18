---
title: IDispError::GetHresult | Microsoft Docs
ms.custom: ''
ms.date: 01/18/2017
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
apiname:
- IDispError.GetHresult
apilocation:
- scrobj.dll
helpviewer_keywords:
- IDispError::GetHresult
ms.assetid: a14d566e-473f-497b-a2f9-85331433e6c9
caps.latest.revision: 8
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: 161c29d4be70c388003ffc80ec5d885b9bcc632b
ms.sourcegitcommit: d3a485d47c6ba01b0fc9878cbbb7fe88755b29af
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/18/2019
ms.locfileid: "58157834"
---
# <a name="idisperrorgethresult"></a>IDispError::GetHresult
Gelen hata kodunu alır `IDispError` nesne.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp
HRESULT GetHresult(  
   HRESULT*  phr  
);  
```  
  
#### <a name="parameters"></a>Parametreler  
 `phr`  
 [out] Hata kodunu belirtir.  
  
## <a name="return-value"></a>Dönüş Değeri  
 Yöntem döndürür bir `HRESULT`. Olası değerler aşağıdaki tablodakileri içerir, ancak bunlarla da sınırlı değildir:  
  
|Değer|Açıklama|  
|-----------|-----------------|  
|`S_OK`|Yöntem başarılı oldu.|  
  
## <a name="remarks"></a>Açıklamalar  
 Bu yöntem, gelen hata kodunu alır. `IDispError` nesne.  
  
> [!NOTE]
>  Bu yöntem uygulanmadı.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [IDispError Arabirimi](../../winscript/reference/idisperror-interface.md)
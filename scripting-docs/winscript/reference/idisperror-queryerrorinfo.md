---
title: IDispError::QueryErrorInfo | Microsoft Docs
ms.custom: ''
ms.date: 01/18/2017
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
apiname:
- IDispError.QueryErrorInfo
apilocation:
- scrobj.dll
helpviewer_keywords:
- IDispError::QueryErrorInfo
ms.assetid: e7e71a14-77e2-4331-9ffc-1dace041fa84
caps.latest.revision: 8
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: 32d887cad92de28df7e84f71fe6b991ada9067e2
ms.sourcegitcommit: d3a485d47c6ba01b0fc9878cbbb7fe88755b29af
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/18/2019
ms.locfileid: "58160358"
---
# <a name="idisperrorqueryerrorinfo"></a>IDispError::QueryErrorInfo
Belirli bir tür hata bilgilerini alır.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp
HRESULT QueryErrorInfo(  
   GUID  guidErrorType,  
   IDispError**  ppde  
);  
```  
  
#### <a name="parameters"></a>Parametreler  
 `guidErrorType`  
 [in] Hata türü belirten GUID.  
  
 `ppde`  
 [out] Idisperror nesnesini belirtir.  
  
## <a name="return-value"></a>Dönüş Değeri  
 Yöntem döndürür bir `HRESULT`. Olası değerler aşağıdaki tablodakileri içerir, ancak bunlarla da sınırlı değildir:  
  
|Değer|Açıklama|  
|-----------|-----------------|  
|`S_OK`|Yöntem başarılı oldu.|  
  
## <a name="remarks"></a>Açıklamalar  
 `QueryErrorInfo` Yöntemi hata bilgilerinin belirli bir tür alır.  
  
> [!NOTE]
>  Bu yöntem uygulanmadı.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [IDispError Arabirimi](../../winscript/reference/idisperror-interface.md)
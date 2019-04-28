---
title: IDispError::GetNext | Microsoft Docs
ms.custom: ''
ms.date: 01/18/2017
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
apiname:
- IDispError.GetNext
apilocation:
- scrobj.dll
helpviewer_keywords:
- IDispError::GetNext
ms.assetid: 3e5267f8-ba62-41c3-bd3e-eced2ad85e8e
caps.latest.revision: 8
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: 4af2d239c26c156fad0be7fb45bc04f601d35c83
ms.sourcegitcommit: 47eeeeadd84c879636e9d48747b615de69384356
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "63437282"
---
# <a name="idisperrorgetnext"></a>IDispError::GetNext
Sonraki alır `IDispError` nesne.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp
HRESULT GetNext(  
   IDispError**  ppde  
);  
```  
  
#### <a name="parameters"></a>Parametreler  
 `ppde`  
 [out] Sonraki belirtir `IDispError` nesne.  
  
## <a name="return-value"></a>Dönüş Değeri  
 Yöntem döndürür bir `HRESULT`. Olası değerler aşağıdaki tablodakileri içerir, ancak bunlarla da sınırlı değildir:  
  
|Değer|Açıklama|  
|-----------|-----------------|  
|`S_OK`|Yöntem başarılı oldu.|  
  
## <a name="remarks"></a>Açıklamalar  
 Bu yöntem sonraki alır `IDispError` nesne. Bu son ise `IDispError` nesnesi, bu yöntem NULL döndürür.  
  
> [!NOTE]
> Bu yöntem uygulanmadı.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [IDispError Arabirimi](../../winscript/reference/idisperror-interface.md)
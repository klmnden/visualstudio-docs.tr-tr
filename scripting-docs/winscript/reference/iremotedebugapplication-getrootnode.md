---
title: IRemoteDebugApplication::GetRootNode | Microsoft Docs
ms.custom: ''
ms.date: 01/18/2017
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
apiname:
- IRemoteDebugApplication.GetRootNode
apilocation:
- pdm.dll
helpviewer_keywords:
- IRemoteDebugApplication::GetRootNode
ms.assetid: 6c043aba-1dc5-41de-9711-96cde5e040f6
caps.latest.revision: 8
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: ef8337e27bb5a666e8d5d8d38abcafb044da02ba
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62944218"
---
# <a name="iremotedebugapplicationgetrootnode"></a>IRemoteDebugApplication::GetRootNode
Uygulamayla ilişkili tüm düğümleri eklendiği uygulama düğümü döndürür.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp
HRESULT GetRootNode(  
   IDebugApplicationNode**  ppdanRoot  
);  
```  
  
#### <a name="parameters"></a>Parametreler  
 `ppdanRoot`  
 [out] Hata ayıklama uygulama düğümü altında uygulamayla ilişkili tüm düğümleri eklenir.  
  
## <a name="return-value"></a>Dönüş Değeri  
 Yöntem döndürür bir `HRESULT`. Olası değerler aşağıdaki tablodakileri içerir, ancak bunlarla da sınırlı değildir:  
  
|Değer|Açıklama|  
|-----------|-----------------|  
|`S_OK`|Yöntem başarılı oldu.|  
  
## <a name="remarks"></a>Açıklamalar  
 Bu yöntem uygulama ile ilişkili olan tüm düğümleri eklendiği uygulama düğümü döndürür.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [IRemoteDebugApplication Arabirimi](../../winscript/reference/iremotedebugapplication-interface.md)
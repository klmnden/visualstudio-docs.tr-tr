---
title: IDebugStackFrameSniffer::EnumStackFrames | Microsoft Docs
ms.custom: ''
ms.date: 01/18/2017
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
apiname:
- IDebugStackFrameSniffer.EnumStackFrames
apilocation:
- jscript.dll
helpviewer_keywords:
- IDebugStackFrameSniffer::EnumStackFrames
ms.assetid: a7629ab3-ef7d-4bbe-a137-bb2a8ad0f384
caps.latest.revision: 8
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: da0d6d46a3bbc508308c689b4e10bea15501fad3
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "63005738"
---
# <a name="idebugstackframesnifferenumstackframes"></a>IDebugStackFrameSniffer::EnumStackFrames
Geçerli iş parçacığı için yığın çerçevelerinin bir numaralandırıcı döndürür.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp
HRESULT EnumStackFrames(  
   IEnumDebugStackFrames**  ppedsf  
);  
```  
  
#### <a name="parameters"></a>Parametreler  
 `ppedsf`  
 [out] Geçerli iş parçacığı için yığın çerçevesi için Numaralandırıcı.  
  
## <a name="return-value"></a>Dönüş Değeri  
 Yöntem döndürür bir `HRESULT`. Olası değerler aşağıdaki tablodakileri içerir, ancak bunlarla da sınırlı değildir:  
  
|Değer|Açıklama|  
|-----------|-----------------|  
|`S_OK`|Yöntem başarılı oldu.|  
  
## <a name="remarks"></a>Açıklamalar  
 Yığın çerçeve Numaralandırıcı en yakın zamanda gönderilen çerçeve ile başlayarak yığının üstten başlayarak çerçeveleri döndürür.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [IDebugStackFrameSniffer Arabirimi](../../winscript/reference/idebugstackframesniffer-interface.md)
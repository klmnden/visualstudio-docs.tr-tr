---
title: IEnumDebugStackFrames::Reset | Microsoft Docs
ms.custom: ''
ms.date: 01/18/2017
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
apiname:
- IEnumDebugStackFrames.Reset
apilocation:
- jscript.dll
helpviewer_keywords:
- IEnumDebugStackFrames::Reset
ms.assetid: 57be2683-5346-4464-bdf5-6fd45b56253a
caps.latest.revision: 8
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: 76cb09ef9456f0dccf3bd034914c9988dd0ff187
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62963344"
---
# <a name="ienumdebugstackframesreset"></a>IEnumDebugStackFrames::Reset
Bir numaralandırma sıralı başlangıç durumuna sıfırlar.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp
HRESULT Reset();  
```  
  
#### <a name="parameters"></a>Parametreler  
 Bu yöntem parametre almaz.  
  
## <a name="return-value"></a>Dönüş Değeri  
 Yöntem döndürür bir `HRESULT`. Olası değerler aşağıdaki tablodakileri içerir, ancak bunlarla da sınırlı değildir:  
  
|Değer|Açıklama|  
|-----------|-----------------|  
|`S_OK`|Yöntem başarılı oldu.|  
  
## <a name="remarks"></a>Açıklamalar  
 Bu yöntem, bir numaralandırma sıralı başlangıç durumuna sıfırlar.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [IEnumDebugStackFrames Arabirimi](../../winscript/reference/ienumdebugstackframes-interface.md)
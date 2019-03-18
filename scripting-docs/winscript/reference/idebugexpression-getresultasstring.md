---
title: IDebugExpression::GetResultAsString | Microsoft Docs
ms.custom: ''
ms.date: 01/18/2017
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
apiname:
- IDebugExpression.GetResultAsString
apilocation:
- jscript.dll
helpviewer_keywords:
- IDebugExpression::GetResultAsString
ms.assetid: edadd2ad-9369-4878-bf87-cea15be9f363
caps.latest.revision: 8
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: 84255e364630245564a0cbab5d38c6dff38df0a8
ms.sourcegitcommit: d3a485d47c6ba01b0fc9878cbbb7fe88755b29af
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/18/2019
ms.locfileid: "58146597"
---
# <a name="idebugexpressiongetresultasstring"></a>IDebugExpression::GetResultAsString
Dize ve işlemin dönüş değeri olarak ifade değerlendirmesinin sonucu döndürür.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp
HRESULT GetResultAsString(  
   HRESULT*  phrResult,  
   BSTR*     pbstrResult  
);  
```  
  
#### <a name="parameters"></a>Parametreler  
 `phrResult`  
 [out] İşlemin dönüş değeri.  
  
 `pbstrResult`  
 [out] İfade değerlendirmesinin sonucu.  
  
## <a name="return-value"></a>Dönüş Değeri  
 Yöntem döndürür bir `HRESULT`. Olası değerler aşağıdaki tablodakileri içerir, ancak bunlarla da sınırlı değildir:  
  
|Değer|Açıklama|  
|-----------|-----------------|  
|`S_OK`|Yöntem başarılı oldu.|  
|`E_PENDING`|İşlemi hala geçerli olduğunu bekleniyor.|  
  
## <a name="remarks"></a>Açıklamalar  
 Bu yöntem bir dize ve işlem olarak ifade değerlendirmesinin sonucu döndürür `HRESULT`.  
  
 Bu yöntem döndürür `S_OK` ve `phrResult` döndürür `E_ABORT` varsa `Abort` işlemi durdurur.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [IDebugExpression Arabirimi](../../winscript/reference/idebugexpression-interface.md)
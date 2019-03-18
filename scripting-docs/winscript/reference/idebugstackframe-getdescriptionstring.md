---
title: IDebugStackFrame::GetDescriptionString | Microsoft Docs
ms.custom: ''
ms.date: 01/18/2017
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
apiname:
- IDebugStackFrame.GetDescriptionString
apilocation:
- jscript.dll
helpviewer_keywords:
- IDebugStackFrame::GetDescriptionString
ms.assetid: a2ddc069-c440-4dee-98dc-ab7c78773b94
caps.latest.revision: 8
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: f870c6dbc654f8465d201c53443228153ce4a68b
ms.sourcegitcommit: d3a485d47c6ba01b0fc9878cbbb7fe88755b29af
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/18/2019
ms.locfileid: "58152843"
---
# <a name="idebugstackframegetdescriptionstring"></a>IDebugStackFrame::GetDescriptionString
Yığın çerçevesinin kısa veya uzun metin açıklamasını döndürür.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp
HRESULT GetDescriptionString(  
   BOOL   fLong,  
   BSTR*  pbstrDescription  
);  
```  
  
#### <a name="parameters"></a>Parametreler  
 `fLong`  
 [in] Bayrağı, burada `TRUE` uzun açıklamasını döndürür ve `FALSE` kısa açıklamasını döndürür.  
  
 `pbstrDescription`  
 [out] Yığın çerçevesinin açıklaması.  
  
## <a name="return-value"></a>Dönüş Değeri  
 Yöntem döndürür bir `HRESULT`. Olası değerler aşağıdaki tablodakileri içerir, ancak bunlarla da sınırlı değildir:  
  
|Değer|Açıklama|  
|-----------|-----------------|  
|`S_OK`|Yöntem başarılı oldu.|  
  
## <a name="remarks"></a>Açıklamalar  
 Genellikle, `fLong` olduğu `FALSE`, bu yöntem yalnızca yığın çerçevesiyle ilgili işlevin adını sağlar. Zaman `fLong` olduğu `TRUE`, bu yöntem işlev parametrelerini ve diğer ilgili bilgileri de sağlayabilir.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [IDebugStackFrame Arabirimi](../../winscript/reference/idebugstackframe-interface.md)
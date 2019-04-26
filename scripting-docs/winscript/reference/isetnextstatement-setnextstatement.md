---
title: ISetNextStatement::SetNextStatement | Microsoft Docs
ms.custom: ''
ms.date: 01/18/2017
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
apiname:
- ISetNextStatement.SetNextStatement
apilocation:
- scrobj.dll
ms.assetid: c5534f3b-39a5-4466-b8fc-69b717c6eee9
caps.latest.revision: 5
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: 3f4add20384684b24a630a0799c50a9aaae58034
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62786301"
---
# <a name="isetnextstatementsetnextstatement"></a>ISetNextStatement::SetNextStatement
Bu yöntem, komut yorumlayıcı yürütebilen sonraki kod bağlamı güncelleştirir.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp
HRESULT SetNextStatement(  
   IDebugStackFrame*  pStackFrame,  
   IDebugCodeContext*  pCodeContext  
)  
```  
  
#### <a name="parameters"></a>Parametreler  
 `pStackFrame`  
 [in] Bir yığın çerçevesi nesne işaretçisi.  
  
 `pCodeContext`  
 [in] Kod kapsamı nesnesine işaretçi.  
  
## <a name="return-value"></a>Dönüş Değeri  
 Yöntem döndürür bir `HRESULT`. Olası değerler aşağıdaki tablodakileri içerir, ancak bunlarla da sınırlı değildir:  
  
|Değer|Açıklama|  
|-----------|-----------------|  
|`S_OK`|Yöntem başarılı oldu.|  
  
## <a name="remarks"></a>Açıklamalar  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [ISetNextStatement Arabirimi](../../winscript/reference/isetnextstatement-interface.md)
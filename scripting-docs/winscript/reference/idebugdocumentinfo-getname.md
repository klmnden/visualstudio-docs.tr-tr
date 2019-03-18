---
title: IDebugDocumentInfo::GetName | Microsoft Docs
ms.custom: ''
ms.date: 01/18/2017
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
apiname:
- IDebugDocumentInfo.GetName
apilocation:
- pdm.dll
helpviewer_keywords:
- IDebugDocumentInfo::GetName
ms.assetid: c25d73da-99b6-4c9f-82af-182b4853f81c
caps.latest.revision: 8
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: 9975563c27b986190fbd2731c3f36b1e32719c0b
ms.sourcegitcommit: d3a485d47c6ba01b0fc9878cbbb7fe88755b29af
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/18/2019
ms.locfileid: "58160332"
---
# <a name="idebugdocumentinfogetname"></a>IDebugDocumentInfo::GetName
Belirtilen belge adı döndürür.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp
HRESULT GetName(  
   DOCUMENTNAMETYPE  dnt,  
   BSTR*             pbstrName  
);  
```  
  
#### <a name="parameters"></a>Parametreler  
 `dnt`  
 [in] Belge adı döndürülecek türü.  
  
 `pbstrName`  
 [out] Ad içeren dize.  
  
## <a name="return-value"></a>Dönüş Değeri  
 Yöntem döndürür bir `HRESULT`. Olası değerler aşağıdaki tablodakileri içerir, ancak bunlarla da sınırlı değildir:  
  
|Değer|Açıklama|  
|-----------|-----------------|  
|`S_OK`|Yöntem başarılı oldu.|  
|`E_FAIL`|Belirtilen belge adı bilinmiyor.|  
  
## <a name="remarks"></a>Açıklamalar  
 Bu yöntem, belirtilen belge adı döndürür.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Idebugdocumentınfo arabirimi](../../winscript/reference/idebugdocumentinfo-interface.md)   
 [DOCUMENTNAMETYPE Sabit Listesi](../../winscript/reference/documentnametype-enumeration.md)
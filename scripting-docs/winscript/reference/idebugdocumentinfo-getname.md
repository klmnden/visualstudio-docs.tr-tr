---
title: IDebugDocumentInfo::GetName | Microsoft Docs
ms.custom: ''
ms.date: 01/18/2017
ms.prod: windows-script-interfaces
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
ms.openlocfilehash: f3ecde4fbde1a265596a01d7f0f953763363e797
ms.sourcegitcommit: 116e9614867e0b3c627ce9001012a4c39435a42b
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/08/2019
ms.locfileid: "54097701"
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
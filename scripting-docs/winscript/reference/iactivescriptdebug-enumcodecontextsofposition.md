---
title: IActiveScriptDebug::EnumCodeContextsOfPosition | Microsoft Docs
ms.custom: ''
ms.date: 01/18/2017
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
apiname:
- IActiveScriptDebug.EnumCodeContextsOfPosition
apilocation:
- jscript.dll
helpviewer_keywords:
- IActiveScriptDebug::EnumCodeContextsOfPosition
ms.assetid: 19f44420-bcc8-4c10-8c38-378d96044117
caps.latest.revision: 8
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: c364d00941a65272b4d22cc7674a0f0e6178f099
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "63009748"
---
# <a name="iactivescriptdebugenumcodecontextsofposition"></a>IActiveScriptDebug::EnumCodeContextsOfPosition
Temsilci seçmek için bir akıllı ana bilgisayar tarafından kullanılan `IDebugDocumentContext::EnumCodeContexts` yöntemi.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp
HRESULT EnumCodeContextsOfPosition(  
   DWORD_PTR                 dwSourceContext,  
   ULONG                     uCharacterOffset,  
   ULONG                     uNumChars,  
   IEnumDebugCodeContexts**  ppescc  
);  
```  
  
#### <a name="parameters"></a>Parametreler  
 `dwSourceContext`  
 [in] Sağlanan kaynak bağlamı `IActiveScriptParse::ParseScriptText` veya `IActiveScriptParse::AddScriptlet`.  
  
 `uCharacterOffset`  
 [in] Karakter başlangıç betiği metin göre uzaklığı.  
  
 `uNumChars`  
 [in] Bu bağlamda karakter sayısı.  
  
 `ppescc`  
 [out] Belirtilen aralıktaki kod bağlamları bir numaralandırıcı.  
  
## <a name="return-value"></a>Dönüş Değeri  
 Yöntem döndürür bir `HRESULT`. Olası değerler aşağıdaki tablodakileri içerir, ancak bunlarla da sınırlı değildir:  
  
|Değer|Açıklama|  
|-----------|-----------------|  
|`S_OK`|Yöntem başarılı oldu.|  
  
## <a name="remarks"></a>Açıklamalar  
 Akıllı ana bilgisayar temsilci seçmek için bu yöntemi kullanın `IDebugDocumentContext::EnumCodeContexts` yöntemi.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Iactivescriptdebug arabirimi](../../winscript/reference/iactivescriptdebug-interface.md)   
 [IDebugDocumentContext::EnumCodeContexts](../../winscript/reference/idebugdocumentcontext-enumcodecontexts.md)
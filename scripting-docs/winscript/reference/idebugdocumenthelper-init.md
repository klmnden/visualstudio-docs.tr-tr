---
title: IDebugDocumentHelper::Init | Microsoft Docs
ms.custom: ''
ms.date: 01/18/2017
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
apiname:
- IDebugDocumentHelper.Init
apilocation:
- pdm.dll
helpviewer_keywords:
- IDebugDocumentHelper::Init
ms.assetid: 1dd5a01f-0779-4109-8c6c-f16f5a3835bf
caps.latest.revision: 8
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: 3b399f51fc042aa1ed297ab30a7bf2c9bc4befca
ms.sourcegitcommit: d3a485d47c6ba01b0fc9878cbbb7fe88755b29af
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/18/2019
ms.locfileid: "58160020"
---
# <a name="idebugdocumenthelperinit"></a>IDebugDocumentHelper::Init
`Init` Yöntemi hata ayıklama belge yardımcı bir ad ve ilk öznitelikleri ile başlatır.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp
HRESULT Init(  
   IDebugApplication*  pda,  
   LPCOLESTR           pszShortName,  
   LPCOLESTR           pszLongName,  
   TEXT_DOC_ATTR       docAttr  
);  
```  
  
#### <a name="parameters"></a>Parametreler  
 `pda`  
 [in] Bu belgeyle ilişkili hata ayıklama uygulama.  
  
 `pszShortName`  
 [in] Belge kısa adını içeren null ile sonlandırılmış bir dize.  
  
 `pszLongName`  
 [in] Belge uzun adını içeren null ile sonlandırılmış bir dize.  
  
 `docAttr`  
 [in] Metin belgesi öznitelikleri belirtir.  
  
## <a name="return-value"></a>Dönüş Değeri  
 Yöntem döndürür bir `HRESULT`. Olası değerler aşağıdaki tablodakileri içerir, ancak bunlarla da sınırlı değildir:  
  
|Değer|Açıklama|  
|-----------|-----------------|  
|`S_OK`|Yöntem başarılı oldu.|  
  
## <a name="remarks"></a>Açıklamalar  
 Bu yöntem, hata ayıklama belge yardımcı bir ad ve ilk öznitelikleri ile başlatır.  
  
 Bu belge ağacında kadar görünmüyor `IDebugDocumentHelper::Attach` çağrılır.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [IDebugDocumentHelper::Attach](../../winscript/reference/idebugdocumenthelper-attach.md)   
 [Idebugdocumenthelper arabirimi](../../winscript/reference/idebugdocumenthelper-interface.md)   
 [TEXT_DOC_ATTR Sabitleri](../../winscript/reference/text-doc-attr-constants.md)
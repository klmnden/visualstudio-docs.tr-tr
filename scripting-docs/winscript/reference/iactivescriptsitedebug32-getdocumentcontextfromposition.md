---
title: IActiveScriptSiteDebug32::GetDocumentContextFromPosition | Microsoft Docs
ms.custom: ''
ms.date: 01/18/2017
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: article
ms.assetid: 53348dff-35a6-4303-b263-90c10af06bf3
caps.latest.revision: 4
author: mikejo5000
ms.author: mikejo
ms.openlocfilehash: 9a52abcfa4defb49526f944469c95a2247f5d85c
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62992525"
---
# <a name="iactivescriptsitedebug32getdocumentcontextfromposition"></a>IActiveScriptSiteDebug32::GetDocumentContextFromPosition
Temsilci seçme için dil altyapısı tarafından kullanılan `IDebugCodeContext::GetSourceContext`.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp
HRESULT GetDocumentContextFromPosition(  
   DWORD_PTR                dwSourceContext,  
   ULONG                    uCharacterOffset,  
   ULONG                    uNumChars,  
   IDebugDocumentContext**  ppsc  
);  
```  
  
#### <a name="parameters"></a>Parametreler  
 `dwSourceContext`  
 [in] Sağlanan kaynak içeriği `ParseScriptText` veya `AddScriptlet`.  
  
 `uCharacterOffset`  
 [in] Karakter göre betik bloğu ya da kod oluşturma başlangıç uzaklığı.  
  
 `uNumChars`  
 [in] Bu bağlamda karakter sayısı.  
  
 `ppsc`  
 [out] Bu karakter konumu aralığına karşılık gelen belge bağlamı.  
  
## <a name="return-value"></a>Dönüş Değeri  
 Yöntem döndürür bir `HRESULT`. Olası değerler aşağıdaki tablodakileri içerir, ancak bunlarla da sınırlı değildir:  
  
|Değer|Açıklama|  
|-----------|-----------------|  
|`S_OK`|Yöntem başarılı oldu.|  
  
## <a name="remarks"></a>Açıklamalar  
 Dil altyapıları temsilci seçmek için bu yöntemi kullanın `IDebugCodeContext::GetSourceContext`.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [IActiveScriptSiteDebug32 Arabirimi](../../winscript/reference/iactivescriptsitedebug32-interface.md)
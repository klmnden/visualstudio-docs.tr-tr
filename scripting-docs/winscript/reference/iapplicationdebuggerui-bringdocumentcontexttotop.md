---
title: IApplicationDebuggerUI::BringDocumentContextToTop | Microsoft Docs
ms.custom: ''
ms.date: 01/18/2017
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
apiname:
- IApplicationDebuggerUI.BringDocumentContextToTop
apilocation:
- scrobj.dll
helpviewer_keywords:
- IApplicationDebuggerUI::BringDocumentContextToTop
ms.assetid: 7844217d-658b-42af-8d10-2714f4eded20
caps.latest.revision: 8
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: 596f9357a8553bf6c39140a6948d8ae3085c3210
ms.sourcegitcommit: d3a485d47c6ba01b0fc9878cbbb7fe88755b29af
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/18/2019
ms.locfileid: "58147689"
---
# <a name="iapplicationdebuggeruibringdocumentcontexttotop"></a>IApplicationDebuggerUI::BringDocumentContextToTop
Üst hata ayıklayıcı kullanıcı arabirimi için belirtilen belge bağlamını içeren bir pencere getirir ve bağlam pencereye kaydırır.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp
HRESULT BringDocumentContextToTop(  
   IDebugDocumentContext*  pddc  
);  
```  
  
#### <a name="parameters"></a>Parametreler  
 `pddc`  
 [in] Hata ayıklayıcı kullanıcı arabiriminde dön getirmek için belge bağlamı.  
  
## <a name="return-value"></a>Dönüş Değeri  
 Yöntem döndürür bir `HRESULT`. Olası değerler aşağıdaki tablodakileri içerir, ancak bunlarla da sınırlı değildir:  
  
|Değer|Açıklama|  
|-----------|-----------------|  
|`S_OK`|Yöntem başarılı oldu.|  
|`E_INVALIDARG`|Tarafından belirtilen bağlamı `pddc` bilinmiyor.|  
  
## <a name="remarks"></a>Açıklamalar  
 Bu yöntem, üst hata ayıklayıcı kullanıcı arabirimi için belirtilen belge bağlamını içeren bir pencere getirir ve bağlam pencereye kaydırır.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [IApplicationDebuggerUI Arabirimi](../../winscript/reference/iapplicationdebuggerui-interface.md)
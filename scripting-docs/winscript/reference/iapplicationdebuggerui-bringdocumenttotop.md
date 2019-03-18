---
title: IApplicationDebuggerUI::BringDocumentToTop | Microsoft Docs
ms.custom: ''
ms.date: 01/18/2017
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
apiname:
- IApplicationDebuggerUI.BringDocumentToTop
apilocation:
- scrobj.dll
helpviewer_keywords:
- IApplicationDebuggerUI::BringDocumentToTop
ms.assetid: ef5fe1e7-4381-4409-a0d7-58f993abe84e
caps.latest.revision: 8
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: a8a88b44f609113670259492eb82491b16004d29
ms.sourcegitcommit: d3a485d47c6ba01b0fc9878cbbb7fe88755b29af
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/18/2019
ms.locfileid: "58148249"
---
# <a name="iapplicationdebuggeruibringdocumenttotop"></a>IApplicationDebuggerUI::BringDocumentToTop
Pencerenin üst hata ayıklayıcı belirtilen hata ayıklama belge içeren kullanıcı arabirimi sunar.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp
HRESULT BringDocumentToTop(  
   IDebugDocumentText*  pddt  
);  
```  
  
#### <a name="parameters"></a>Parametreler  
 `pddt`  
 [in] Belgenin en üstüne hata ayıklayıcı kullanıcı arabirimi Getir hata ayıklayın.  
  
## <a name="return-value"></a>Dönüş Değeri  
 Yöntem döndürür bir `HRESULT`. Olası değerler aşağıdaki tablodakileri içerir, ancak bunlarla da sınırlı değildir:  
  
|Değer|Açıklama|  
|-----------|-----------------|  
|`S_OK`|Yöntem başarılı oldu.|  
|`E_INVALIDARG`|Belge bilinmiyor.|  
  
## <a name="remarks"></a>Açıklamalar  
 Bu yöntem, kullanıcı arabirimi içeren belirtilen hata ayıklama belgenin en üstüne hata ayıklayıcı penceresini getirir.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [IApplicationDebuggerUI Arabirimi](../../winscript/reference/iapplicationdebuggerui-interface.md)
---
title: IBindEventHandler::BindHandler | Microsoft Docs
ms.custom: ''
ms.date: 01/18/2017
ms.prod: windows-script-interfaces
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
apiname:
- IBindEventHandler.BindHandler
apilocation:
- scrobj.dll
helpviewer_keywords:
- IBindEventHandler::BindHandler
ms.assetid: 87909828-2224-4bb1-a6c9-dfe715ac4c9b
caps.latest.revision: 8
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: 62ac6de8342f0a436d984f4194351507fdcd5edd
ms.sourcegitcommit: 116e9614867e0b3c627ce9001012a4c39435a42b
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/08/2019
ms.locfileid: "54090720"
---
# <a name="ibindeventhandlerbindhandler"></a>IBindEventHandler::BindHandler
Bir olay, bir nesneye bağlar.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp
HRESULT BindHandler(  
   LPCOLESTR   pstrEvent,  
   IDispatch*  pdisp  
);  
```  
  
#### <a name="parameters"></a>Parametreler  
 `pstrEvent`  
 [in] İşlenecek Olay belirtir.  
  
 `pdisp`  
 [in] Olayı işlemek için bir nesne belirtir.  
  
## <a name="return-value"></a>Dönüş Değeri  
 Yöntem döndürür bir `HRESULT`. Olası değerler aşağıdaki tablodakileri içerir, ancak bunlarla da sınırlı değildir:  
  
|Değer|Açıklama|  
|-----------|-----------------|  
|`S_OK`|Yöntem başarılı oldu.|  
  
## <a name="remarks"></a>Açıklamalar  
 Bu yöntem, bir nesne için bir olay bağlar.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [IBindEventHandler Arabirimi](../../winscript/reference/ibindeventhandler-interface.md)
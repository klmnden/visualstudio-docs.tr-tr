---
title: IDebugDocumentHelper::SetDebugDocumentHost | Microsoft Docs
ms.custom: ''
ms.date: 01/18/2017
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
apiname:
- IDebugDocumentHelper.SetDebugDocumentHost
apilocation:
- pdm.dll
helpviewer_keywords:
- IDebugDocumentHelper::SetDebugDocumentHost
ms.assetid: b26a03c3-8a3f-47b0-b916-4c65d5500f10
caps.latest.revision: 8
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: 47c003657518edae0e8ffed13ffef9f6f072d296
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62948999"
---
# <a name="idebugdocumenthelpersetdebugdocumenthost"></a>IDebugDocumentHelper::SetDebugDocumentHost
Kümeleri `IDebugDocumentHost` bu belge için.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp
HRESULT SetDebugDocumentHost(  
   IDebugDocumentHost*  pddh  
);  
```  
  
#### <a name="parameters"></a>Parametreler  
 `pddh`  
 [in] Hata ayıklama belge ana bilgisayar.  
  
## <a name="return-value"></a>Dönüş Değeri  
 Yöntem döndürür bir `HRESULT`. Olası değerler aşağıdaki tablodakileri içerir, ancak bunlarla da sınırlı değildir:  
  
|Değer|Açıklama|  
|-----------|-----------------|  
|`S_OK`|Yöntem başarılı oldu.|  
  
## <a name="remarks"></a>Açıklamalar  
 `IDebugDocumentHost` Arabirimi akıllı ana bilgisayar söz dizimi renklendirmesi için kullanılır, ertelenmiş metin getiriliyor ve yeni oluşturulan için kontrol eden nesneleri döndüren belge bağlamı.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Idebugdocumenthelper arabirimi](../../winscript/reference/idebugdocumenthelper-interface.md)   
 [IDebugDocumentHost Arabirimi](../../winscript/reference/idebugdocumenthost-interface.md)
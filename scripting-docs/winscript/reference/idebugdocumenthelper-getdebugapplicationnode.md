---
title: IDebugDocumentHelper::GetDebugApplicationNode | Microsoft Docs
ms.custom: ''
ms.date: 01/18/2017
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
apiname:
- IDebugDocumentHelper.GetDebugApplicationNode
apilocation:
- pdm.dll
helpviewer_keywords:
- IDebugDocumentHelper::GetDebugApplicationNode
ms.assetid: ecd18803-beb4-4ac2-9702-cc9e8a12c395
caps.latest.revision: 8
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: 10740c3489b617b1685ad222cac7c158e0196c4d
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62783097"
---
# <a name="idebugdocumenthelpergetdebugapplicationnode"></a>IDebugDocumentHelper::GetDebugApplicationNode
Bu belgeye karşılık gelen hata ayıklama uygulama düğümü döndürür.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp
HRESULT GetDebugApplicationNode(  
   IDebugApplicationNode**  ppdan  
);  
```  
  
#### <a name="parameters"></a>Parametreler  
 `ppdan`  
 [out] Bu belgeye karşılık gelen hata ayıklama uygulama düğümü.  
  
## <a name="return-value"></a>Dönüş Değeri  
 Yöntem döndürür bir `HRESULT`. Olası değerler aşağıdaki tablodakileri içerir, ancak bunlarla da sınırlı değildir:  
  
|Değer|Açıklama|  
|-----------|-----------------|  
|`S_OK`|Yöntem başarılı oldu.|  
  
## <a name="remarks"></a>Açıklamalar  
 Bu belgeye karşılık gelen hata ayıklama uygulama düğümü döndürür.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [IDebugDocumentHelper Arabirimi](../../winscript/reference/idebugdocumenthelper-interface.md)
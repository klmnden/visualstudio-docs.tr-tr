---
title: IProcessDebugManager::CreateDebugDocumentHelper | Microsoft Docs
ms.custom: ''
ms.date: 01/18/2017
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
apiname:
- IProcessDebugManager.CreateDebugDocumentHelper
apilocation:
- pdm.dll
helpviewer_keywords:
- IProcessDebugManager::CreateDebugDocumentHelper
ms.assetid: d644e192-1bcc-4768-a91e-239cd920adcd
caps.latest.revision: 8
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: 38de1e828ccd1715fb83cc76c06ba837818d2af0
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "63002353"
---
# <a name="iprocessdebugmanagercreatedebugdocumenthelper"></a>IProcessDebugManager::CreateDebugDocumentHelper
Bu uygulama için yeni bir hata ayıklama belge Yardımcısı oluşturur.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp
HRESULT CreateDebugDocumentHelper(  
   IUnknown*               punkOuter,  
   IDebugDocumentHelper**  pddh  
);  
```  
  
#### <a name="parameters"></a>Parametreler  
 `punkOuter`  
 [in] Döndürülen nesne toplanması için ise `punkOuter` denetlemek için bir arabirim işaretçisi `IUnknown`. Aksi takdirde, bir null işaretçidir.  
  
 `pddh`  
 [out] Bu uygulama için hata ayıklama belge yardımcı nesnesi.  
  
## <a name="return-value"></a>Dönüş Değeri  
 Yöntem döndürür bir `HRESULT`. Olası değerler aşağıdaki tablodakileri içerir, ancak bunlarla da sınırlı değildir:  
  
|Değer|Açıklama|  
|-----------|-----------------|  
|`S_OK`|Yöntem başarılı oldu.|  
  
## <a name="remarks"></a>Açıklamalar  
 Bu yöntem, bu uygulama için yeni bir hata ayıklama belge Yardımcısı oluşturur.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [IProcessDebugManager Arabirimi](../../winscript/reference/iprocessdebugmanager-interface.md)
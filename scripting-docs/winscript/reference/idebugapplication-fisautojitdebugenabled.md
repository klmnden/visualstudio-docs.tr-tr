---
title: IDebugApplication::FIsAutoJitDebugEnabled | Microsoft Docs
ms.custom: ''
ms.date: 01/18/2017
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
apiname:
- IDebugApplication.FIsAutoJitDebugEnabled
apilocation:
- pdm.dll
helpviewer_keywords:
- IDebugApplication::FIsAutoJitDebugEnabled
ms.assetid: 0551dd3b-e6eb-442a-8201-418f96fe62df
caps.latest.revision: 8
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: f594c5ce48ebd31a265ed438db176c5707d9b079
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62990869"
---
# <a name="idebugapplicationfisautojitdebugenabled"></a>IDebugApplication::FIsAutoJitDebugEnabled
Just-ın-time (JIT) hata ayıklayıcı otomatik hata ayıklama dumb Konaklara kayıtlı olup olmadığını belirler.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp
BOOL FIsAutoJitDebugEnabled();  
```  
  
#### <a name="parameters"></a>Parametreler  
 Bu yöntem parametre almaz.  
  
## <a name="return-value"></a>Dönüş Değeri  
 Yöntem başarılı olursa ve JIT hata ayıklayıcı otomatik hata ayıklama dumb Konaklara kaydedilir, yöntem döndürür `TRUE`. Aksi halde `FALSE`.  
  
## <a name="remarks"></a>Açıklamalar  
 JIT hata ayıklayıcı otomatik hata ayıklama dumb Konaklara kayıtlıysa, bu yöntem belirler.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [IDebugApplication Arabirimi](../../winscript/reference/idebugapplication-interface.md)
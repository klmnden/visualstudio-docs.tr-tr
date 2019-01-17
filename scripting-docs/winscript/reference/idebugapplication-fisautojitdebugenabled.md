---
title: IDebugApplication::FIsAutoJitDebugEnabled | Microsoft Docs
ms.custom: ''
ms.date: 01/18/2017
ms.prod: windows-script-interfaces
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
ms.openlocfilehash: b06d223d76ed741eef6b379ace6b522248ded2e1
ms.sourcegitcommit: 8bf9e51c77a5a602fab9513b9187e59e57dfebad
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/16/2019
ms.locfileid: "54348223"
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
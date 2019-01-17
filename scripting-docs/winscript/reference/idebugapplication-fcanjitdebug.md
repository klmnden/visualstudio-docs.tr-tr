---
title: IDebugApplication::FCanJitDebug | Microsoft Docs
ms.custom: ''
ms.date: 01/18/2017
ms.prod: windows-script-interfaces
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
apiname:
- IDebugApplication.FCanJitDebug
apilocation:
- pdm.dll
helpviewer_keywords:
- IDebugApplication::FCanJitDebug
ms.assetid: d7ddac65-4864-411f-bf66-34a46c03f239
caps.latest.revision: 8
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: 6808c8bb7e27e7b416e79b2f23e323c3ae3a528f
ms.sourcegitcommit: 8bf9e51c77a5a602fab9513b9187e59e57dfebad
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/16/2019
ms.locfileid: "54344843"
---
# <a name="idebugapplicationfcanjitdebug"></a>IDebugApplication::FCanJitDebug
Just-ın-time (JIT) hata ayıklayıcı kayıtlı olup olmadığını belirler.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp
BOOL FCanJitDebug();  
```  
  
#### <a name="parameters"></a>Parametreler  
 Bu yöntem parametre almaz.  
  
## <a name="return-value"></a>Dönüş Değeri  
 Yöntem başarılı olursa ve JIT hata ayıklayıcı kaydedilir, yöntem döndürür `TRUE`. Aksi halde `FALSE`.  
  
## <a name="remarks"></a>Açıklamalar  
 Bu yöntem, JIT hata ayıklayıcı kayıtlı olup olmadığını belirler.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [IDebugApplication Arabirimi](../../winscript/reference/idebugapplication-interface.md)
---
title: IActiveScriptGarbageCollector::CollectGarbage | Microsoft Docs
ms.custom: ''
ms.date: 01/18/2017
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
ms.assetid: 75f77c49-2190-4d49-a3e0-9dcf847c502b
caps.latest.revision: 3
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: db8683534e449b2cdd8fcdb344c245d93da8fafc
ms.sourcegitcommit: d3a485d47c6ba01b0fc9878cbbb7fe88755b29af
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/18/2019
ms.locfileid: "58144673"
---
# <a name="iactivescriptgarbagecollectorcollectgarbage"></a>IActiveScriptGarbageCollector::CollectGarbage
Etkin komut dosyası ana atık toplama başlatmak için bu yöntemi çağırır.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp
HRESULT CollectGarbage(        SCRIPTGCTYPE scriptgctype    );  
```  
  
#### <a name="parameters"></a>Parametreler  
 `scriptgctype`  
 [in] [SCRIPTGCTYPE numaralandırması](../../winscript/reference/scriptgctype-enumeration.md) normal veya ayrıntılı atık toplama etkinleştirilip etkinleştirilmeyeceğini belirtir.  
  
## <a name="return-value"></a>Dönüş Değeri  
 HRESULT döndürür.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [IActiveScriptGarbageCollector Arabirimi](../../winscript/reference/iactivescriptgarbagecollector-interface.md)
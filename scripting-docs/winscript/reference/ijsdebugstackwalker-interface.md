---
title: Ijsdebugstackwalker arabirimi | Microsoft Docs
ms.custom: ''
ms.date: 01/18/2017
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
ms.assetid: 3fe30394-49c8-48e9-bde9-ffe5d79b2121
caps.latest.revision: 4
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: d06af2c509339d9499f66e1f267c54c69951e225
ms.sourcegitcommit: d3a485d47c6ba01b0fc9878cbbb7fe88755b29af
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/18/2019
ms.locfileid: "58150900"
---
# <a name="ijsdebugstackwalker-interface"></a>IJsDebugStackWalker Arabirimi
Belirtilen iş parçacığı için yığın değişkenini temsil eder.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp
IJsDebugStackWalker : public IUnknown;  
```  
  
## <a name="members"></a>Üyeler  
  
### <a name="public-methods"></a>Ortak Yöntemler  
  
|Ad|Açıklama|  
|----------|-----------------|  
|[IJsDebugStackWalker::GetNext Metodu](../../winscript/reference/ijsdebugstackwalker-getnext-method.md)|Sonraki çerçeveyi alır.|  
  
## <a name="remarks"></a>Açıklamalar  
 Yığın yürüyüşçüleri, yalnızca hedef durdurulursa ve hedef işlem yeniden devam sonra geçersiz sırasında oluşturulabilir.  
  
## <a name="requirements"></a>Gereksinimler  
 **Başlık:** jscript9diag.h  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Windows Betik Arabirimleri Başvurusu](../../winscript/reference/windows-script-interfaces-reference.md)
---
title: Ijsdebugstackwalker arabirimi | Microsoft Docs
ms.custom: ''
ms.date: 01/18/2017
ms.prod: windows-script-interfaces
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
ms.assetid: 3fe30394-49c8-48e9-bde9-ffe5d79b2121
caps.latest.revision: 4
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: d79950c6d5595a0a8a95623a7510c5523f16e41b
ms.sourcegitcommit: 116e9614867e0b3c627ce9001012a4c39435a42b
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/08/2019
ms.locfileid: "54087909"
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
---
title: Scrıptprop_hostkeepalıve özelliği | Microsoft Docs
ms.custom: ''
ms.date: 01/18/2017
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
ms.assetid: bfa199f2-28ba-4320-bc0f-2320fad018bd
caps.latest.revision: 5
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: 3724bfcb1ec42617cda4c89269cb0160accafb1a
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62840359"
---
# <a name="scriptprophostkeepalive-property"></a>SCRIPTPROP_HOSTKEEPALIVE Özelliği
Komut dosyası altyapısı bekleyen başvuru olduğunda tam işlevsel tutulması gereken olup olmadığını belirtmek için kullanılır.  
  
 Kullanım [IActiveScriptProperty::SetProperty](../../winscript/reference/iactivescriptproperty-setproperty.md) bu özellik ayarlanacak `true`. Bu özellik ayarlanırsa `true`, komut dosyası altyapısı veya için en az bir bekleyen başvuru var olduğu sürece komut dosyası altyapısı tam olarak işlevsel tutulur bir `IDispatch` komut dosyası kullanılarak oluşturulan bir JavaScript nesne işaretçisi altyapısı. Bu özelliği ayarlandığında `true`, açıkça kapattığınızda veya komut dosyası altyapısı kullanarak sıfırlama [IActiveScript::Close](../../winscript/reference/iactivescript-close.md) veya [IActiveScript::SetScriptState](../../winscript/reference/iactivescript-setscriptstate.md) yöntemleri. Komut dosyası altyapısı sürümünü bir betik nesnesi son başvuruysa kapanır.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp
#define SCRIPTPROP_HOSTKEEPALIVE 0x70000004  
```  
  
## <a name="requirements"></a>Gereksinimler  
 Bu özellik yalnızca activscp.idl birlikte yüklenen sürümünü görünür [!INCLUDE[win8](../../javascript/includes/win8-md.md)], üzerinde Internet Explorer 8 KB 2707082 ile [!INCLUDE[win7](../../winscript/reference/includes/win7-md.md)], veya Internet Explorer 9'da için KB 2722913 [!INCLUDE[win7](../../winscript/reference/includes/win7-md.md)] veya [!INCLUDE[vista_first](../../winscript/reference/includes/vista-first-md.md)].
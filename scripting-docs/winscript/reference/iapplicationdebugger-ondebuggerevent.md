---
title: IApplicationDebugger::onDebuggerEvent | Microsoft Docs
ms.custom: ''
ms.date: 01/18/2017
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
apiname:
- IApplicationDebugger.onDebuggerEvent
apilocation:
- scrobj.dll
helpviewer_keywords:
- IApplicationDebugger::onDebuggerEvent
ms.assetid: 82a5faaa-1222-4bf1-8569-10439dbdf16d
caps.latest.revision: 8
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: b78bb3345463dfd682534dc60a216f3e0e8fdf2a
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62991369"
---
# <a name="iapplicationdebuggerondebuggerevent"></a>IApplicationDebugger::onDebuggerEvent
Özel uygulama olayını işler.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp
HRESULT onDebuggerEvent(  
   REFIID     riid,  
   IUnknown*  punk  
);  
```  
  
#### <a name="parameters"></a>Parametreler  
 `riid`  
 [in] Nesne için arabirim tanımlayıcısı.  
  
 `punk`  
 [in] Tarafından tanımlanan arabirimi uygulayan olay nesnesiyle `riid`.  
  
## <a name="return-value"></a>Dönüş Değeri  
 Yöntem döndürür bir `HRESULT`. Olası değerler aşağıdaki tablodakileri içerir, ancak bunlarla da sınırlı değildir:  
  
|Değer|Açıklama|  
|-----------|-----------------|  
|`S_OK`|Yöntem başarılı oldu.|  
|`E_NOTIMPL`|Yöntem henüz uygulanmadı.|  
  
## <a name="remarks"></a>Açıklamalar  
 Semantiği `IUnknown` olan tamamen uygulama/hata ayıklayıcı tanımlanmış.  
  
 Bu yöntem, hata ayıklayıcı modelinin özel uzantıları sağlar; şu anda uygulanmamaktadır.  
  
 Bu yöntem olduğunda çağrılır `IDebugApplication::FireDebuggerEvent` çağrılır.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Iapplicationdebugger arabirimi](../../winscript/reference/iapplicationdebugger-interface.md)   
 [IDebugApplication::FireDebuggerEvent](../../winscript/reference/idebugapplication-firedebuggerevent.md)
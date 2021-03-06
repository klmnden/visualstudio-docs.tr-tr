---
title: IDebugApplication::HandleBreakPoint | Microsoft Docs
ms.custom: ''
ms.date: 01/18/2017
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
apiname:
- IDebugApplication.HandleBreakPoint
apilocation:
- pdm.dll
helpviewer_keywords:
- IDebugApplication::HandleBreakPoint
ms.assetid: 97219bdf-a39a-4e69-81ac-4ca2afe77ce5
caps.latest.revision: 8
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: 5e3444e6eedde9576216552e41abb0e97aafa2d7
ms.sourcegitcommit: 47eeeeadd84c879636e9d48747b615de69384356
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "63412386"
---
# <a name="idebugapplicationhandlebreakpoint"></a>IDebugApplication::HandleBreakPoint
Geçerli iş parçacığını engellemek neden olur ve IDE hata ayıklayıcı kesme noktası bir bildirim gönderir.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp
HRESULT HandleBreakPoint(  
   BREAKREASON         br,  
   BREAKRESUMEACTION*  pbra  
);  
```  
  
#### <a name="parameters"></a>Parametreler  
 `br`  
 [in] Kesme nedeni.  
  
 `pbra`  
 [out] Hata ayıklayıcı uygulama devam ettiğinde gerçekleştirilecek eylem.  
  
## <a name="return-value"></a>Dönüş Değeri  
 Yöntem döndürür bir `HRESULT`. Olası değerler aşağıdaki tablodakileri içerir, ancak bunlarla da sınırlı değildir:  
  
|Değer|Açıklama|  
|-----------|-----------------|  
|`S_OK`|Yöntem başarılı oldu.|  
  
## <a name="remarks"></a>Açıklamalar  
 Bir dil altyapısı, bir kesme noktasına denk gelir, bir iş parçacığının bağlamında bu yöntemi çağırır. Bu yöntem, geçerli iş parçacığını engeller ve IDE hata ayıklayıcı bir kesme noktası bildirim gönderir. Hata ayıklayıcı, uygulama devam ettiğinde `pbra` parametresi, gerçekleştirilecek eylemi belirtir.  
  
> [!NOTE]
> Dil altyapısı, yığın numaralandırma gibi çerçeveleri veya sırasında kesme noktası nevyhodnocovat görevleri gerçekleştirmek için iş parçacığı tarafından çağrılabilir.  
  
 Bu yöntem neden `IApplicationDebugger::onHandleBreakPoint` çağrılabilir.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Idebugapplication arabirimi](../../winscript/reference/idebugapplication-interface.md)   
 [IApplicationDebugger::onHandleBreakPoint](../../winscript/reference/iapplicationdebugger-onhandlebreakpoint.md)   
 [BREAKREASON numaralandırması](../../winscript/reference/breakreason-enumeration.md)   
 [BREAKRESUMEACTION Sabit Listesi](../../winscript/reference/breakresumeaction-enumeration.md)
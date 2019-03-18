---
title: IDebugApplication::SynchronousCallInDebuggerThread | Microsoft Docs
ms.custom: ''
ms.date: 01/18/2017
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
apiname:
- IDebugApplication.SynchronousCallInDebuggerThread
apilocation:
- pdm.dll
helpviewer_keywords:
- IDebugApplication::SynchronousCallInDebuggerThread
ms.assetid: 9daa1722-f25a-4691-aefc-fd28672fb883
caps.latest.revision: 8
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: d5460efaa3448c7812707e0baa7b2f5afe1d27a0
ms.sourcegitcommit: d3a485d47c6ba01b0fc9878cbbb7fe88755b29af
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/18/2019
ms.locfileid: "58154035"
---
# <a name="idebugapplicationsynchronouscallindebuggerthread"></a>IDebugApplication::SynchronousCallInDebuggerThread
Çağıran kod hata ayıklayıcı iş parçacığında çalıştırmak bir mekanizma sağlar.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp
HRESULT SynchronousCallInDebuggerThread(  
   IDebugThreadCall*  pptc,  
   DWORD_PTR          dwParam1,  
   DWORD_PTR          dwParam2,  
   DWORD_PTR          dwParam3  
);  
```  
  
#### <a name="parameters"></a>Parametreler  
 `pptc`  
 [in] Aranacak nesne.  
  
 `dwParam1`  
 [in] Geçirmek için ilk parametre `IDebugThreadCall::ThreadCallHandler` yöntemi.  
  
 `dwParam2`  
 [in] Geçirmek için ikinci parametresinin `IDebugThreadCall::ThreadCallHandler` yöntemi.  
  
 `dwParam3`  
 [in] Geçirmek için üçüncü parametresinin `IDebugThreadCall::ThreadCallHandler` yöntemi.  
  
## <a name="return-value"></a>Dönüş Değeri  
 Yöntem döndürür bir `HRESULT`. Olası değerler aşağıdaki tablodakileri içerir, ancak bunlarla da sınırlı değildir:  
  
|Değer|Açıklama|  
|-----------|-----------------|  
|`S_OK`|Yöntem başarılı oldu.|  
  
## <a name="remarks"></a>Açıklamalar  
 Genellikle dil altyapıları ve konakları ücretsiz iş parçacıklı nesneleri, tek iş parçacıklı uygulamalar üzerinde uygulamak için bu yöntemi kullanın.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Idebugapplication arabirimi](../../winscript/reference/idebugapplication-interface.md)   
 [IDebugThreadCall Arabirimi](../../winscript/reference/idebugthreadcall-interface.md)
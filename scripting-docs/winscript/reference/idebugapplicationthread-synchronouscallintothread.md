---
title: IDebugApplicationThread::SynchronousCallIntoThread | Microsoft Docs
ms.custom: ''
ms.date: 01/18/2017
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
apiname:
- IDebugApplicationThread.SynchronousCallIntoThread
apilocation:
- pdm.dll
helpviewer_keywords:
- IDebugApplicationThread::SynchronousCallIntoThread
ms.assetid: 8a91157f-dade-418a-ad02-5607ce12c95c
caps.latest.revision: 8
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: f0c9b89332b55a180220820e8ffe1e030d37a848
ms.sourcegitcommit: d3a485d47c6ba01b0fc9878cbbb7fe88755b29af
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/18/2019
ms.locfileid: "58146714"
---
# <a name="idebugapplicationthreadsynchronouscallintothread"></a>IDebugApplicationThread::SynchronousCallIntoThread
Çağıran uygulama iş parçacığında kodu çalıştırmak bir mekanizma sağlar.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp
HRESULT SynchronousCallIntoThread(  
   IDebugThreadCall*  pstcb,  
   DWORD_PTR          dwParam1,  
   DWORD_PTR          dwParam2,  
   DWORD_PTR          dwParam3  
);  
```  
  
#### <a name="parameters"></a>Parametreler  
 `pstcb`  
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
 Bu yöntemi çağıran kod hata ayıklayıcı iş parçacığında çalıştırmak bir mekanizma sağlar. Genellikle dil altyapıları ve konakları ücretsiz iş parçacıklı nesneleri, tek iş parçacıklı uygulamalar üzerinde uygulamak için bu yöntemi kullanın.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Idebugapplicationthread arabirimi](../../winscript/reference/idebugapplicationthread-interface.md)   
 [IDebugThreadCall Arabirimi](../../winscript/reference/idebugthreadcall-interface.md)
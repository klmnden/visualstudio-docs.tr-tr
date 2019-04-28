---
title: IDebugApplication::CreateAsyncDebugOperation | Microsoft Docs
ms.custom: ''
ms.date: 01/18/2017
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
apiname:
- IDebugApplication.CreateAsyncDebugOperation
apilocation:
- pdm.dll
helpviewer_keywords:
- IDebugApplication::CreateAsyncDebugOperation
ms.assetid: bc32b101-6364-4498-8458-bd5f3ab5ad94
caps.latest.revision: 8
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: c60c84dbd3be9248e2bd075e65d53f7f9361d0b5
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62991012"
---
# <a name="idebugapplicationcreateasyncdebugoperation"></a>IDebugApplication::CreateAsyncDebugOperation
Belirli bir zaman uyumlu hata ayıklama işlemi zaman uyumsuz erişim sağlar.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp
HRESULT CreateAsyncDebugOperation(  
   IDebugSyncOperation*    psdo,  
   IDebugAsyncOperation**  ppado  
);  
```  
  
#### <a name="parameters"></a>Parametreler  
 `psdo`  
 [in] Zaman uyumlu hata ayıklama işlemi nesnesi.  
  
 `ppado`  
 [out] Zaman uyumsuz hata ayıklama işlemi nesnesi.  
  
## <a name="return-value"></a>Dönüş Değeri  
 Yöntem döndürür bir `HRESULT`. Olası değerler aşağıdaki tablodakileri içerir, ancak bunlarla da sınırlı değildir:  
  
|Değer|Açıklama|  
|-----------|-----------------|  
|`S_OK`|Yöntem başarılı oldu.|  
  
## <a name="remarks"></a>Açıklamalar  
 Bu yöntemi açıkça hata ayıklayıcı iş parçacığıyla eşitleme olmadan ifadeleri zaman uyumsuz olarak değerlendirilecek dil altyapısı sağlar. Daha fazla bilgi için [Idebugsyncoperation arabirimi](../../winscript/reference/idebugsyncoperation-interface.md) ve [Idebugasyncoperation arabirimi](../../winscript/reference/idebugasyncoperation-interface.md).  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Idebugapplication arabirimi](../../winscript/reference/idebugapplication-interface.md)   
 [Idebugsyncoperation arabirimi](../../winscript/reference/idebugsyncoperation-interface.md)   
 [IDebugAsyncOperation Arabirimi](../../winscript/reference/idebugasyncoperation-interface.md)
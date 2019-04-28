---
title: IDebugAsyncOperationCallBack::onComplete | Microsoft Docs
ms.custom: ''
ms.date: 01/18/2017
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
apiname:
- IDebugAsyncOperationCallBack.onComplete
apilocation:
- jscript.dll
helpviewer_keywords:
- IDebugAsyncOperationCallBack::onComplete
ms.assetid: d4023f5a-41f9-4948-b0dc-3317d61bb783
caps.latest.revision: 8
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: f9e5532a55901d8e29addfee58594645440991f6
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62821879"
---
# <a name="idebugasyncoperationcallbackoncomplete"></a>IDebugAsyncOperationCallBack::onComplete
Bir zaman uyumsuz hata ayıklama işleminin bir sonucu olduğunu bildirir.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp
HRESULT onComplete();  
```  
  
#### <a name="parameters"></a>Parametreler  
 Bu yöntem parametre almaz.  
  
## <a name="return-value"></a>Dönüş Değeri  
 Yöntem döndürür bir `HRESULT`. Olası değerler aşağıdaki tablodakileri içerir, ancak bunlarla da sınırlı değildir:  
  
|Değer|Açıklama|  
|-----------|-----------------|  
|`S_OK`|Yöntem başarılı oldu.|  
  
## <a name="remarks"></a>Açıklamalar  
 Bu yöntem bir sonuç kullanılabilir olduğundan emin sinyalleri bir `IDebugAsyncOperation` nesne. Hata ayıklayıcı iş parçacığında olay harekete geçirilir.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Idebugasyncoperationcallback arabirimi](../../winscript/reference/idebugasyncoperationcallback-interface.md)   
 [IDebugAsyncOperation Arabirimi](../../winscript/reference/idebugasyncoperation-interface.md)
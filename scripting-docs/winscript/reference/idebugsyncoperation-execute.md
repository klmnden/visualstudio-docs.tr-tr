---
title: IDebugSyncOperation::Execute | Microsoft Docs
ms.custom: ''
ms.date: 01/18/2017
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
apiname:
- IDebugSyncOperation.Execute
apilocation:
- jscript.dll
helpviewer_keywords:
- IDebugSyncOperation::Execute
ms.assetid: a45b8c7d-c51a-4098-877f-fbec2f1f6947
caps.latest.revision: 8
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: a2bc204169ff94a240e363eb8caa35ec8c7de9be
ms.sourcegitcommit: d3a485d47c6ba01b0fc9878cbbb7fe88755b29af
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/18/2019
ms.locfileid: "58146363"
---
# <a name="idebugsyncoperationexecute"></a>IDebugSyncOperation::Execute
Zaman uyumlu işlem gerçekleştirir ve döndürür.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp
HRESULT Execute(  
   IUnknown**  ppunkResult  
);  
```  
  
#### <a name="parameters"></a>Parametreler  
 `ppunkResult`  
 [out] İşlem tarafından döndürülen nesne parametresi.  
  
## <a name="return-value"></a>Dönüş Değeri  
 Yöntem döndürür bir `HRESULT`. Olası değerler aşağıdaki tablodakileri içerir, ancak bunlarla da sınırlı değildir:  
  
|Değer|Açıklama|  
|-----------|-----------------|  
|`S_OK`|Yöntem başarılı oldu.|  
|`E_ABORT`|Çağırarak işlemi iptal edildi `IDebugSyncOperation::InProgressAbort` yöntemi.|  
  
## <a name="remarks"></a>Açıklamalar  
 İşlem Hata Ayıklama Yöneticisi'nde hedef iş parçacığı çağrı `Execute` yöntem zaman uyumlu olarak.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [IDebugSyncOperation Arabirimi](../../winscript/reference/idebugsyncoperation-interface.md)
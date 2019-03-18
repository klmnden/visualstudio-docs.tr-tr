---
title: IDebugSyncOperation::InProgressAbort | Microsoft Docs
ms.custom: ''
ms.date: 01/18/2017
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
apiname:
- IDebugSyncOperation.InProgressAbort
apilocation:
- jscript.dll
helpviewer_keywords:
- IDebugSyncOperation::InProgressAbort
ms.assetid: bfd0889c-b627-4843-b1c6-b6b918f42d61
caps.latest.revision: 8
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: a794ea70d6d2fe937afb311e6961d53f22bd7ac2
ms.sourcegitcommit: d3a485d47c6ba01b0fc9878cbbb7fe88755b29af
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/18/2019
ms.locfileid: "58159731"
---
# <a name="idebugsyncoperationinprogressabort"></a>IDebugSyncOperation::InProgressAbort
Bir başka bir iş parçacığı üzerinde devam eden işlemi iptal eder.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp
HRESULT InProgressAbort();  
```  
  
#### <a name="parameters"></a>Parametreler  
 Bu yöntem parametre almaz.  
  
## <a name="return-value"></a>Dönüş Değeri  
 Yöntem döndürür bir `HRESULT`. Olası değerler aşağıdaki tablodakileri içerir, ancak bunlarla da sınırlı değildir:  
  
|Değer|Açıklama|  
|-----------|-----------------|  
|`S_OK`|Yöntem başarılı oldu.|  
|`E_NOTIMPL`|İşlem iptal edilemez.|  
|`E_ABORT`|İşlem tamamlanamadı.|  
  
## <a name="remarks"></a>Açıklamalar  
 Hata ayıklama işlem yöneticisi, hata ayıklayıcı iş parçacığı başka bir iş parçacığı sürmekte olan bir işlemi iptal etmek için bu yöntemi çağırır.  
  
 Varsa `InProgressAbort` yöntemi işlemini tamamlayamıyor döndürür `E_ABORT` olabildiğince çabuk. Bu yöntem döndürebilir `E_NOTIMPL` , işlem iptal edilemez.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [IDebugSyncOperation Arabirimi](../../winscript/reference/idebugsyncoperation-interface.md)
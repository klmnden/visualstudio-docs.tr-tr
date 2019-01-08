---
title: IDebugSyncOperation::InProgressAbort | Microsoft Docs
ms.custom: ''
ms.date: 01/18/2017
ms.prod: windows-script-interfaces
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
ms.openlocfilehash: cab8bae7f131d24c1a2c7272dc8d1178e12bf0e6
ms.sourcegitcommit: 116e9614867e0b3c627ce9001012a4c39435a42b
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/08/2019
ms.locfileid: "54095530"
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
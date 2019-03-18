---
title: Ijsenumdebugproperty::Next yöntemi | Microsoft Docs
ms.custom: ''
ms.date: 01/18/2017
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
apiname:
- IJsEnumDebugProperty.Next
apilocation:
- jscript9diag.dll
ms.assetid: 9fad1893-483a-440c-88c1-469494212300
caps.latest.revision: 4
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: 3ec6a1dded8c24de06a5746261a19b6609a97ada
ms.sourcegitcommit: d3a485d47c6ba01b0fc9878cbbb7fe88755b29af
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/18/2019
ms.locfileid: "58147091"
---
# <a name="ijsenumdebugpropertynext-method"></a>IJsEnumDebugProperty::Next Yöntemi
Bu nesnenin özelliklerini okur.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp
HRESULT Next(  
   ULONG count,  
   IJsDebugProperty **ppDebugProperty,  
   ULONG *pActualCount  
);  
```  
  
#### <a name="parameters"></a>Parametreler  
 `count`  
 [in] Okunacak özellik sayısı.  
  
 `ppDebugProperty`  
 [out] Özellik tarayıcısını temsil eden nesne.  
  
 `pActualCount`  
 [out] Nesne özelliklerinin gerçek sayısı.  
  
## <a name="return-value"></a>Dönüş Değeri  
  
## <a name="requirements"></a>Gereksinimler  
 **Başlık:** jscript9diag.h  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [IJsEnumDebugProperty Arabirimi](../../winscript/reference/ijsenumdebugproperty-interface.md)
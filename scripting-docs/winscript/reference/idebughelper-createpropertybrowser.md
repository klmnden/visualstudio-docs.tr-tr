---
title: IDebugHelper::CreatePropertyBrowser | Microsoft Docs
ms.custom: ''
ms.date: 01/18/2017
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
apiname:
- IDebugHelper.CreatePropertyBrowser
apilocation:
- pdm.dll
helpviewer_keywords:
- IDebugHelper::CreatePropertyBrowser
ms.assetid: 2fa819cf-c7f7-4bd7-b018-ea33b804ba8f
caps.latest.revision: 8
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: 4fc1e4365deea4a3981d9cf457a2c0af37edcd43
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62979259"
---
# <a name="idebughelpercreatepropertybrowser"></a>IDebugHelper::CreatePropertyBrowser
Bir değişken sarmalayan bir özellik tarayıcısı döndürür.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp
HRESULT CreatePropertyBrowser(  
   VARIANT*                  pvar,  
   LPCOLESTR                 bstrName,  
   IDebugApplicationThread*  pdat,  
   IDebugProperty**          ppdob  
);  
```  
  
#### <a name="parameters"></a>Parametreler  
 `pvar`  
 [in] Göz atmak için kök değişken.  
  
 `bstrName`  
 [in] Kök vermek adı.  
  
 `pdat`  
 [in] Hangi özellikleri istemek iş parçacığı. Bu parametre NULL ise, hiçbir taşıma gerçekleştirilir.  
  
 `ppdob`  
 [out] Özellik tarayıcısı.  
  
## <a name="return-value"></a>Dönüş Değeri  
 Yöntem döndürür bir `HRESULT`. Olası değerler aşağıdaki tablodakileri içerir, ancak bunlarla da sınırlı değildir:  
  
|Değer|Açıklama|  
|-----------|-----------------|  
|`S_OK`|Yöntem başarılı oldu.|  
  
## <a name="remarks"></a>Açıklamalar  
 Bu yöntem, bir değişken sarmalayan bir özellik tarayıcısı döndürür.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [IDebugHelper::CreatePropertyBrowserEx](../../winscript/reference/idebughelper-createpropertybrowserex.md)   
 [Idebughelper arabirimi](../../winscript/reference/idebughelper-interface.md)   
 [IDebugProperty Arabirimi](../../winscript/reference/idebugproperty-interface.md)
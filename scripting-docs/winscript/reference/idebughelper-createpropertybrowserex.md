---
title: IDebugHelper::CreatePropertyBrowserEx | Microsoft Docs
ms.custom: ''
ms.date: 01/18/2017
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
apiname:
- IDebugHelper.CreatePropertyBrowserEx
apilocation:
- pdm.dll
helpviewer_keywords:
- IDebugHelper::CreatePropertyBrowserEx
ms.assetid: 87ad322f-09da-4ce8-bb68-0b0bbeec645b
caps.latest.revision: 8
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: 01e63d1588fd1e25f3415f22450ed5145752d711
ms.sourcegitcommit: d3a485d47c6ba01b0fc9878cbbb7fe88755b29af
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/18/2019
ms.locfileid: "58144582"
---
# <a name="idebughelpercreatepropertybrowserex"></a>IDebugHelper::CreatePropertyBrowserEx
Bir değişken sarmalar ve değişken değerlerini VARTYPE türleri veya özel dönüştürme dizeleri için sağlayan bir özellik tarayıcısı döndürür.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp
HRESULT CreatePropertyBrowserEx(  
   VARIANT*                  pvar,  
   LPCOLESTR                 bstrName,  
   IDebugApplicationThread*  pdat,  
   IDebugFormatter*          pdf,  
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
  
 `pdf`  
 [in] Çeşitleri için özel biçimlendirme sağlayan nesne.  
  
 `ppdob`  
 [out] Özellik tarayıcısı.  
  
## <a name="return-value"></a>Dönüş Değeri  
 Yöntem döndürür bir `HRESULT`. Olası değerler aşağıdaki tablodakileri içerir, ancak bunlarla da sınırlı değildir:  
  
|Değer|Açıklama|  
|-----------|-----------------|  
|`S_OK`|Yöntem başarılı oldu.|  
  
## <a name="remarks"></a>Açıklamalar  
 Bu yöntem, bir değişken sarmalar ve değişken değerlerini VARTYPE türleri veya özel dönüştürme dizeleri için sağlayan bir özellik tarayıcısı döndürür.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [IDebugHelper::CreatePropertyBrowser](../../winscript/reference/idebughelper-createpropertybrowser.md)   
 [Idebughelper arabirimi](../../winscript/reference/idebughelper-interface.md)   
 [IDebugProperty Arabirimi](../../winscript/reference/idebugproperty-interface.md)
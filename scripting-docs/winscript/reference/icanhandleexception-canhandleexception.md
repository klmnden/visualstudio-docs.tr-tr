---
title: ICanHandleException::CanHandleException | Microsoft Docs
ms.custom: ''
ms.date: 01/18/2017
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
apiname:
- ICanHandleException.CanHandleException
apilocation:
- scrobj.dll
helpviewer_keywords:
- ICanHandleException::CanHandleException
ms.assetid: 0fc703bf-9518-487e-af20-00e073b640f1
caps.latest.revision: 8
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: 406787d5ee6811b80f9e6831e5a67cab8367e7d0
ms.sourcegitcommit: d3a485d47c6ba01b0fc9878cbbb7fe88755b29af
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/18/2019
ms.locfileid: "58146493"
---
# <a name="icanhandleexceptioncanhandleexception"></a>ICanHandleException::CanHandleException
Komut dosyası altyapısı çağıran bir belirtilen bir özel durumu işleyebilir belirler.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp
HRESULT CanHandleException(  
   EXCEPINFO*  pExcepInfo,  
   VARIANT*    pvar  
);  
```  
  
#### <a name="parameters"></a>Parametreler  
 `pExcepInfo`  
 [in] İşaretçi bir `EXCEPINFO` hiçbir özel durum işleyicisi bulunursa bildirilir bilgileri içeren yapısı.  
  
 `pvar`  
 [in] Tarafından oluşturulan değeri gibi bir özel durumla ilişkili bir değer bir `throw` deyimi. Bu parametre olabilir `NULL`.  
  
## <a name="return-value"></a>Dönüş Değeri  
 Yöntem döndürür bir `HRESULT`. Olası değerler aşağıdaki tablodakileri içerir, ancak bunlarla da sınırlı değildir:  
  
|Değer|Açıklama|  
|-----------|-----------------|  
|`S_OK`|Çağıran özel durumu işleyebilecek|  
|`E_FAIL`|Çağıran özel durum işleyemiyor.|  
  
## <a name="remarks"></a>Açıklamalar  
 Bir çağrı, `IDispatchEx::InvokeEx`, veya benzer bir yöntem, bir özel durum, bir çağıranın destekleyen betiğin arayan zincirindeki betik altyapısı denetler sonuçlanıyor `ICanHandleException` arabirim ve özel durum işleyebileceğini belirtir. Hiçbir çağıran özel durumu işleyebilecek, komut dosyası altyapısı durdurur.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Icanhandleexception arabirimi](../../winscript/reference/icanhandleexception-interface.md)   
 [IDispatchEx::InvokeEx](../../winscript/reference/idispatchex-invokeex.md)
---
title: IDispatchEx::GetMemberProperties | Microsoft Docs
ms.custom: ''
ms.date: 01/18/2017
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
apiname:
- IDispatchEx.GetMemberProperties
apilocation:
- scrobj.dll
helpviewer_keywords:
- GetMemberProperties method
ms.assetid: 20d43209-12e2-472a-9bf3-81eced137b71
caps.latest.revision: 8
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: f607e06fe3c898a6839c0bbd2d51edee1f0ffb2c
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "63000809"
---
# <a name="idispatchexgetmemberproperties"></a>IDispatchEx::GetMemberProperties
Bir üyenin özellikleri alır.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp
HRESULT GetMemberProperties(  
   DISPID id,  
   DWORD grfdexFetch,  
   DWORD *pgrfdex  
);  
```  
  
#### <a name="parameters"></a>Parametreler  
 `id`  
 Üyeyi tanımlar. Kullanan `GetDispID` veya `GetNextDispID` gönderme tanımlayıcısının elde edilir.  
  
 `grfdexFetch`  
 Almak için hangi özellikleri belirler. Bunun altında listelenen değerleri bir birleşimi olabilir `pgrfdex` ve/veya aşağıdaki değerleri birleşimi:  
  
|Değer|Açıklama|  
|-----------|-------------|  
|grfdexPropCanAll|FdexPropCanGet, fdexPropCanPut, fdexPropCanPutRef, fdexPropCanCall, fdexPropCanConstruct ve fdexPropCanSourceEvents birleştirir.|  
|grfdexPropCannotAll|FdexPropCannotGet, fdexPropCannotPut, fdexPropCannotPutRef, fdexPropCannotCall, fdexPropCannotConstruct ve fdexPropCannotSourceEvents birleştirir.|  
|grfdexPropExtraAll|FdexPropNoSideEffects ve fdexPropDynamicType birleştirir.|  
|grfdexPropAll|GrfdexPropCanAll ve grfdexPropCannotAll grfdexPropExtraAll birleştirir.|  
  
 `pgrfdex`  
 Adresi bir `DWORD` , istenen özellikleri alır. Bu, aşağıdaki değerleri birleşimi olabilir:  
  
|Değer|Açıklama|  
|-----------|-------------|  
|fdexPropCanGet|Üye DISPATCH_PROPERTYGET kullanılarak edinilebilir.|  
|fdexPropCannotGet|Üye DISPATCH_PROPERTYGET kullanarak elde edilemiyor.|  
|fdexPropCanPut|Üye DISPATCH_PROPERTYPUT kullanarak ayarlayabilirsiniz.|  
|fdexPropCannotPut|Üye DISPATCH_PROPERTYPUT kullanarak ayarlanamaz.|  
|fdexPropCanPutRef|Üye DISPATCH_PROPERTYPUTREF kullanarak ayarlayabilirsiniz.|  
|fdexPropCannotPutRef|Üye DISPATCH_PROPERTYPUTREF kullanarak ayarlanamaz.|  
|fdexPropNoSideEffects|Yan etkileri üye yok. Örneğin, bir hata ayıklayıcı güvenli bir şekilde alma/ayarlama/çağrısı olabilir ayıklanan betik durumunu değiştirmeden bu üye.|  
|fdexPropDynamicType|Üye dinamiktir ve nesne yaşam süresi boyunca değiştirebilirsiniz.|  
|fdexPropCanCall|Üye DISPATCH_METHOD'ı kullanarak bir yöntem çağrılabilir.|  
|fdexPropCannotCall|Üye DISPATCH_METHOD'ı kullanarak bir yöntem çağrılamaz.|  
|fdexPropCanConstruct|Üye DISPATCH_CONSTRUCT kullanarak bir oluşturucu olarak çağrılabilir.|  
|fdexPropCannotConstruct|Üye DISPATCH_CONSTRUCT kullanarak bir oluşturucu olarak çağrılamaz.|  
|fdexPropCanSourceEvents|Üyeye olayları tetikleyebilir.|  
|fdexPropCannotSourceEvents|Üye olay başlatamaz.|  
  
## <a name="return-value"></a>Dönüş Değeri  
 Aşağıdaki değerlerden birini döndürür:  
  
|||  
|-|-|  
|`S_OK`|Başarılı.|  
|`DISP_E_UNKNOWNNAME`|Adı bilinmiyor.|  
  
## <a name="example"></a>Örnek  
  
```cpp
BSTR bstrName;  
   DISPID dispid;  
   IDispatchEx *pdex;   
   DWORD dwProps;  
  
   // Assign to pdex and bstrName  
   if (SUCCEEDED(pdex->GetDispID(bstrName, fdexNameCaseSensitive, &dispid)) &&  
      SUCCEEDED(pdex->GetMemberProperties(dispid, grfdexPropAll, &dwProps)) &&  
         (dwProps & fdexPropCanPut))  
   {  
      // Assign to member  
   }  
```  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Idispatchex arabirimi](../../winscript/reference/idispatchex-interface.md)   
 [IDispatchEx::GetDispID](../../winscript/reference/idispatchex-getdispid.md)   
 [IDispatchEx::GetNextDispID](../../winscript/reference/idispatchex-getnextdispid.md)
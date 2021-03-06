---
title: IDispatchEx::DeleteMemberByDispID | Microsoft Docs
ms.custom: ''
ms.date: 01/18/2017
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
apiname:
- IDispatchEx.DeleteMemberByDispID
apilocation:
- scrobj.dll
helpviewer_keywords:
- DeleteMemberByDispID method
ms.assetid: f61231e5-ba93-4ac3-bde8-d363548356b3
caps.latest.revision: 8
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: 36eeeb4c28286bb5712be3908b47a5145e460597
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "63000944"
---
# <a name="idispatchexdeletememberbydispid"></a>IDispatchEx::DeleteMemberByDispID
DISPID bir üyesine siler.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp
HRESULT DeleteMemberByDispID(  
    DISPID id  
);  
```  
  
#### <a name="parameters"></a>Parametreler  
 `id`  
 Üye tanımlayıcısı. Kullanan `GetDispID` veya `GetNextDispID` gönderme tanımlayıcısının elde edilir.  
  
## <a name="return-value"></a>Dönüş Değeri  
 Aşağıdaki değerlerden birini döndürür:  
  
|||  
|-|-|  
|`S_OK`|Başarılı.|  
|`S_FALSE`|Üye var, ancak silinemez.|  
  
## <a name="remarks"></a>Açıklamalar  
 DISPID üye silinirse, için geçerli kalır gerekiyor `GetNextDispID`.  
  
 Belirli bir ada sahip bir üye silinir ve aynı ada sahip bir üye daha sonra yeniden oluşturulur, DISPID aynı olmalıdır. (Yalnızca harfe göre farklılık üye adları "aynı" olup olmadığını nesne bağlıdır.)  
  
## <a name="example"></a>Örnek  
  
```cpp
BSTR bstrName;  
DISPID dispid;  
IDispatchEx *pdex;   
  
// Assign to pdex and bstrName  
if (SUCCEEDED(pdex->GetDispID(bstrName, fdexNameCaseSensitive, &dispid)))  
    pdex->DeleteMemberByDispID(dispid);  
```  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Idispatchex arabirimi](../../winscript/reference/idispatchex-interface.md)   
 [IDispatchEx::GetDispID](../../winscript/reference/idispatchex-getdispid.md)   
 [IDispatchEx::GetNextDispID](../../winscript/reference/idispatchex-getnextdispid.md)
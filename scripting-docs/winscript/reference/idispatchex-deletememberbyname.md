---
title: IDispatchEx::DeleteMemberByName | Microsoft Docs
ms.custom: ''
ms.date: 01/18/2017
ms.prod: windows-script-interfaces
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
apiname:
- IDispatchEx.DeleteMemberByName
apilocation:
- scrobj.dll
helpviewer_keywords:
- DeleteMemberByName method
ms.assetid: a01b4e6a-d989-4b29-bb3f-04554f8c39f7
caps.latest.revision: 8
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: 1866b5135d2c98ccacb34c2c776c69dd7d25db3f
ms.sourcegitcommit: 116e9614867e0b3c627ce9001012a4c39435a42b
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/08/2019
ms.locfileid: "54096440"
---
# <a name="idispatchexdeletememberbyname"></a>IDispatchEx::DeleteMemberByName
Bir üye adıyla siler.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp
HRESULT DeleteMemberByName(  
   BSTR bstrName,  
   DWORD grfdex  
  
```  
  
#### <a name="parameters"></a>Parametreler  
 `bstrName`  
 Silinecek üyenin adı.  
  
 `grfdex`  
 Üye adı büyük küçük harfe duyarlı olup olmadığını belirler. Bu, aşağıdaki değerlerden biri olabilir:  
  
|Değer|Açıklama|  
|-----------|-------------|  
|fdexNameCaseSensitive|Ad arama, büyük küçük harfe duyarlı bir şekilde yapılması istekler. Büyük küçük harfe duyarlı arama desteği olmayan nesne tarafından göz ardı edilebilir.|  
|fdexNameCaseInsensitive|Ad arama, büyük küçük harf duyarsız bir şekilde yapılması istekler. Büyük küçük harf duyarsız arama desteği olmayan nesne tarafından göz ardı edilebilir.|  
  
## <a name="return-value"></a>Dönüş Değeri  
 Aşağıdaki değerlerden birini döndürür:  
  
|||  
|-|-|  
|`S_OK`|Başarılı.|  
|`S_FALSE`|Üye var, ancak silinemez.|  
  
## <a name="remarks"></a>Açıklamalar  
 DISPID üye silinirse, için geçerli kalır gerekiyor `GetNextDispID`.  
  
 Belirli bir ada sahip bir üye silinir ve aynı ada sahip bir üye daha sonra yeniden oluşturulur, DISPID aynı olmalıdır. (Yalnızca harfe göre farklılık üyeleri "aynı" olup olmadığını nesne bağlıdır.)  
  
## <a name="example"></a>Örnek  
  
```cpp
BSTR bstrName;  
IDispatchEx *pdex;  
  
// Assign to pdex and bstrName  
pdex->DeleteMemberByName(bstrName, fdexNameCaseSensitive);  
```  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [IDispatchEx Arabirimi](../../winscript/reference/idispatchex-interface.md)
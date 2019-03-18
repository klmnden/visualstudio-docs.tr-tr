---
title: IDispatchEx::DeleteMemberByName | Microsoft Docs
ms.custom: ''
ms.date: 01/18/2017
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
ms.openlocfilehash: dc7c8db4ab28e0bd0fcb48f352cb07595f72fd17
ms.sourcegitcommit: d3a485d47c6ba01b0fc9878cbbb7fe88755b29af
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/18/2019
ms.locfileid: "58153831"
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
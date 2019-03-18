---
title: IObjectIdentity::IsEqualObject | Microsoft Docs
ms.custom: ''
ms.date: 01/18/2017
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
apiname:
- IObjectIdentity.IsEqualObject
apilocation:
- scrobj.dll
helpviewer_keywords:
- IsEqualObject method
ms.assetid: 78c5c5c2-d299-4036-986c-7c1d87cbe7cd
caps.latest.revision: 8
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: c215a15a1239f07272079783366a1617c3a626e2
ms.sourcegitcommit: d3a485d47c6ba01b0fc9878cbbb7fe88755b29af
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/18/2019
ms.locfileid: "58156040"
---
# <a name="iobjectidentityisequalobject"></a>IObjectIdentity::IsEqualObject
Bir nesne geçerli nesneye eşit olup olmadığını belirler.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp
HRESULT IsEqualObject(  
  IUnknown*punk  
);  
```  
  
#### <a name="parameters"></a>Parametreler  
 `punk`  
 [in] Adresi geçerli nesneyle Karşılaştırılacak nesne.  
  
## <a name="return-value"></a>Dönüş Değeri  
 Yöntem döndürür bir `HRESULT`. Olası değerler aşağıdaki tablodakileri içerir, ancak bunlarla da sınırlı değildir:  
  
|Değer|Açıklama|  
|-----------|-----------------|  
|`S_OK`|Nesneler eşit olur.|  
|`S_FALSE`|Nesneler eşit değildir.|  
  
## <a name="remarks"></a>Açıklamalar  
 Uygulanışı `IsEqualObject` yöntemi döndürmelidir `S_OK` yalnızca nesnenin aynı olup olmadığını.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [IObjectIdentity Arabirimi](../../winscript/reference/iobjectidentity-interface.md)
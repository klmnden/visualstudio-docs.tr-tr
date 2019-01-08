---
title: ISimpleConnectionPoint::Advise | Microsoft Docs
ms.custom: ''
ms.date: 01/18/2017
ms.prod: windows-script-interfaces
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
apiname:
- ISimpleConnectionPoint.Advise
apilocation:
- pdm.dll
helpviewer_keywords:
- ISimpleConnectionPoint::Advise
ms.assetid: 59ded60d-b938-4110-aca3-e69ba234ca9a
caps.latest.revision: 8
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: b3c0ea37e6fabb051458a11c4838061126bd98bf
ms.sourcegitcommit: 116e9614867e0b3c627ce9001012a4c39435a42b
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/08/2019
ms.locfileid: "54091747"
---
# <a name="isimpleconnectionpointadvise"></a>ISimpleConnectionPoint::Advise
Basit bir bağlantı noktası nesnesi ve istemcinin havuzu arasında bir bağlantı kurar.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp
HRESULT Advise(  
   IDispatch*  pdisp,  
   DWORD*      pdwCookie  
);  
```  
  
#### <a name="parameters"></a>Parametreler  
 `pdisp`  
 [in] İşaretçi `IDispatch` arabirimi istemciye havuz önerisi kullanıcının. İstemcinin havuzu basit bağlantı noktasından giden çağrıları alır.  
  
 `pdwCookie`  
 [out] Bu bağlantı benzersiz olarak tanımlayan bir döndürülen belirteç işaretçisi. Çağıranın Bu belirteci daha sonra aktararak bağlantıyı silmek için kullandığı `ISimpleConnectionPoint::Unadvise` yöntemi. Bağlantı başarıyla oluşturulmadı, bu değeri sıfırdır.  
  
## <a name="return-value"></a>Dönüş Değeri  
 Yöntem döndürür bir `HRESULT`. Olası değerler aşağıdaki tablodakileri içerir, ancak bunlarla da sınırlı değildir:  
  
|Değer|Açıklama|  
|-----------|-----------------|  
|`S_OK`|Yöntem başarılı oldu.|  
  
## <a name="remarks"></a>Açıklamalar  
 Bu yöntem, basit bir bağlantı noktası nesnesi ve istemcinin havuzu arasında bir bağlantı kurar.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Isimpleconnectionpoint arabirimi](../../winscript/reference/isimpleconnectionpoint-interface.md)   
 [ISimpleConnectionPoint::Unadvise](../../winscript/reference/isimpleconnectionpoint-unadvise.md)
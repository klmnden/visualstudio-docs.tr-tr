---
title: ISimpleConnectionPoint::Advise | Microsoft Docs
ms.custom: ''
ms.date: 01/18/2017
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
ms.openlocfilehash: 98db9c92f682808ce8ecc9f6aa382a2eb2bd8495
ms.sourcegitcommit: d3a485d47c6ba01b0fc9878cbbb7fe88755b29af
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/18/2019
ms.locfileid: "58153116"
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
---
title: IPerPropertyBrowsing2::GetDisplayString | Microsoft Docs
ms.custom: ''
ms.date: 01/18/2017
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
apiname:
- IPerPropertyBrowsing2.GetDisplayString
apilocation:
- scrobj.dll
helpviewer_keywords:
- IPerPropertyBrowsing2::GetDisplayString
ms.assetid: 8f75c6a9-86a9-4e2d-8cb4-74e7b1c0a524
caps.latest.revision: 8
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: f6f63db8d9c032b8e880f05d4d21e50fd56c74e2
ms.sourcegitcommit: d3a485d47c6ba01b0fc9878cbbb7fe88755b29af
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/18/2019
ms.locfileid: "58147988"
---
# <a name="iperpropertybrowsing2getdisplaystring"></a>IPerPropertyBrowsing2::GetDisplayString
Alır kendiliğinden görüntülenebilir olmayan türleri döndürülen metni görüntülemek için bir dize özelliği açıklayan bir addır ve arayanın kullanıcı arabiriminde görüntülenen.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp
HRESULT GetDisplayString(  
   DISPID  dispid,  
   BSTR*  pBstr  
);  
```  
  
#### <a name="parameters"></a>Parametreler  
 `dispid`  
 [in] Görünen adı istenen özellik tanımlayıcısı gönderme.  
  
 `pBstr`  
 [out] İşaretçi `BSTR` tarafından tanımlanan bir özellik için görünen ad içeren `dispID`.  
  
## <a name="return-value"></a>Dönüş Değeri  
 Geçerli bir döndürür `HRESULT`, genellikle `S_OK`.  
  
## <a name="remarks"></a>Açıklamalar  
 Döndürülen dize özelliği geçerli bir değer değil. Bu yalnızca bir dize özelliği görüntülenir.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [IPerPropertyBrowsing2 Arabirimi 1](../../winscript/reference/iperpropertybrowsing2-interface-1.md)
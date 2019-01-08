---
title: IPerPropertyBrowsing2::GetPredefinedStrings | Microsoft Docs
ms.custom: ''
ms.date: 01/18/2017
ms.prod: windows-script-interfaces
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
apiname:
- IPerPropertyBrowsing2.GetPredefinedStrings
apilocation:
- scrobj.dll
helpviewer_keywords:
- IPerPropertyBrowsing2::GetPredefinedStrings
ms.assetid: d2fa30f7-a566-4dbd-8b47-ffdc00419771
caps.latest.revision: 8
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: 3bec9643a89d40a7b1e37d019d4211bd7167ee65
ms.sourcegitcommit: 116e9614867e0b3c627ce9001012a4c39435a42b
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/08/2019
ms.locfileid: "54088614"
---
# <a name="iperpropertybrowsing2getpredefinedstrings"></a>IPerPropertyBrowsing2::GetPredefinedStrings
Bu özellik için olası değeri temsil eden dize işaretçilerini sayılan bir dizi liste kutusunu doldurmak çağıranın izin verir.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp
HRESULT GetPredefinedStrings(  
   DISPID  dispid,  
   CALPOLESTR*  pCaStrings,  
   CADWORD*  pCaCookies  
);  
```  
  
#### <a name="parameters"></a>Parametreler  
 `dispid`  
 [in] Çağıranın dize listesi isteyen özellik tanımlayıcısı gönderme.  
  
 `pCaStrings`  
 [out] Öğe sayısı ve dize işaretçilerini yöntemi olarak ayrılan dizi adresini içeren sayılan, arayana ayrılan dizi yapısı işaretçisi. Yöntem başarısız olursa, bellek tahsis edilir ve yapısı içeriğini tanımsızdır.  
  
 `pCaCookies`  
 [out] Öğe sayısı ve DWORD yöntemi olarak ayrılan dizi adresini içeren sayılan, arayana ayrılan dizi yapısı işaretçisi. Yöntem başarısız olursa, bellek tahsis edilir ve yapısı içeriğini tanımsızdır.  
  
## <a name="return-value"></a>Dönüş Değeri  
 Geçerli bir döndürür `HRESULT`, genellikle `S_OK`.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [IPerPropertyBrowsing2 Arabirimi 1](../../winscript/reference/iperpropertybrowsing2-interface-1.md)
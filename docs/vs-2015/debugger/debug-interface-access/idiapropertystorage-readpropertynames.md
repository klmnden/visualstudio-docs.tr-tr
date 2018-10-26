---
title: IDiaPropertyStorage::ReadPropertyNames | Microsoft Docs
ms.custom: ''
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.reviewer: ''
ms.suite: ''
ms.technology:
- vs-ide-debug
ms.tgt_pltfrm: ''
ms.topic: article
dev_langs:
- C++
helpviewer_keywords:
- IDiaPropertyStorage::ReadPropertyNames
ms.assetid: f8bcab77-afca-4a8f-8710-697842f8a518
caps.latest.revision: 13
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: f285ea61252d23fd27397e846fed7b10f05fd651
ms.sourcegitcommit: 240c8b34e80952d00e90c52dcb1a077b9aff47f6
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/23/2018
ms.locfileid: "49892616"
---
# <a name="idiapropertystoragereadpropertynames"></a>IDiaPropertyStorage::ReadPropertyNames
[!INCLUDE[vs2017banner](../../includes/vs2017banner.md)]

Dize adları için karşılık gelen alır, özellik tanımlayıcıları verilir.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp  
HRESULT ReadPropertyNames (  
   ULONG         cpropid,  
   PROPID const* rgpropid,  
   BSTR*         rglpwstrName  
);  
```  
  
#### <a name="parameters"></a>Parametreler  
 `cpropid`  
 [in] Özellik kimlikleri sayısı `rgpropid`.  
  
 `rgpropid`  
 [in] Adları alınacağı özellik kimlikleri dizisi (`PROPID` WTypes.h tanımlanan bir `ULONG`).  
  
 `rglpwstrName`  
 [out içinde] Belirtilen özellik kimliklerinin özellik adları dizisi. Dizi istenen sayıda özellik adları tutacak önceden ayrılmış olmalıdır ve en az tutabilecek özellikte `cpropid``BSTR` dizeleri.  
  
## <a name="return-value"></a>Dönüş Değeri  
 Başarılı olursa döndürür `S_OK`; Aksi takdirde bir hata kodu döndürür.  
  
## <a name="remarks"></a>Açıklamalar  
 Döndürülen özellik adlarının serbest (çağırarak `SysFreeString` işlevi) artık gerektiğinde.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [IDiaPropertyStorage](../../debugger/debug-interface-access/idiapropertystorage.md)




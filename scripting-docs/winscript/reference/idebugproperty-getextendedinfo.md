---
title: IDebugProperty::GetExtendedInfo | Microsoft Docs
ms.custom: ''
ms.date: 01/18/2017
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
apiname:
- IDebugProperty.GetExtendedInfo
apilocation:
- scrobj.dll
helpviewer_keywords:
- IDebugProperty::GetExtendedInfo
ms.assetid: a989ade5-16d5-4ee6-8d8a-8dcbfad24034
caps.latest.revision: 8
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: 707474f786a8f88c0e08d887f2c2b09c8aaedc8e
ms.sourcegitcommit: d3a485d47c6ba01b0fc9878cbbb7fe88755b29af
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/18/2019
ms.locfileid: "58144868"
---
# <a name="idebugpropertygetextendedinfo"></a>IDebugProperty::GetExtendedInfo
Genişletilmiş özelliği bilgilerini.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp
HRESULT GetExtendedInfo (  
   ULONG  cInfos,  
   GUID*  rgguidExtendedInfo,  
   VARIANT* pExtendedInfo  
);  
```  
  
#### <a name="parameters"></a>Parametreler  
 `cInfos`  
 [in] Genişletilmiş bilgi nesnelerinin sayısı.  
  
 `rgguidExtendedInfo`  
 [in] Bir dizi `GUID`s, böylece aynı anda birden çok öğe genişletilmiş bilgisi alınabilir geçirilir.  
  
 `pExtendedInfo`  
 [out] Bir dizi döndürür `VARIANT`genişletilmiş özellik bilgileri almak için kullanılan s.  
  
## <a name="return-value"></a>Dönüş Değeri  
 Geçerli bir döndürür `HRESULT`, genellikle `S_OK`.  
  
## <a name="remarks"></a>Açıklamalar  
 Bu arabirim genişletilmiş bu nesne için bilgileri. API var. yalnızca kendisi tarafından kullanımını alınan için uygun olmayan bilgi almak amacıyla `IDebugProperty::GetPropertyInfo`).  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [IDebugProperty Arabirimi](../../winscript/reference/idebugproperty-interface.md)
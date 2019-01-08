---
title: IDebugProperty::GetExtendedInfo | Microsoft Docs
ms.custom: ''
ms.date: 01/18/2017
ms.prod: windows-script-interfaces
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
ms.openlocfilehash: 6dc3fc90b8f5fa465715bc4b9466da472cbbb580
ms.sourcegitcommit: 116e9614867e0b3c627ce9001012a4c39435a42b
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/08/2019
ms.locfileid: "54086547"
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
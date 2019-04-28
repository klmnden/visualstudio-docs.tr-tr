---
title: IEnumDebugExtendedPropertyInfo::Next | Microsoft Docs
ms.custom: ''
ms.date: 01/18/2017
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
apiname:
- IEnumDebugExtendedPropertyInfo.Next
apilocation:
- scrobj.dll
helpviewer_keywords:
- IEnumDebugExtendedPropertyInfo::Next
ms.assetid: ac41c9a3-19d1-4596-8a87-01c10b131be3
caps.latest.revision: 8
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: 65e734d1cf57fe9387407a80c9d3e76d7f53ada8
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62963502"
---
# <a name="ienumdebugextendedpropertyinfonext"></a>IEnumDebugExtendedPropertyInfo::Next
Belirtilen sayıda alır`ExtendedDebugPropertyInfo` yapıları, bir sabit listesi sırası.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp
HRESULT Next (  
   ULONGcelt,  
   ExtendedDebugPropertyInfo *rgelt,  
   ULONG* pceltFetched  
);  
```  
  
#### <a name="parameters"></a>Parametreler  
 `celt`  
 [in] Sayısını `ExtendedDebugPropertyInfo`yapılar alınamıyor.  
  
 `rgelt`  
 [out] Bir dizi `ExtendedDebugPropertyInfo` yapıları alınır.  
  
 `pceltFetched`  
 [out] Sayısını `ExtendedDebugPropertyInfo` yapıları gerçekten alınır.  
  
## <a name="return-value"></a>Dönüş Değeri  
 Geçerli bir döndürür `HRESULT`, genellikle `S_OK`.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Ienumdebugextendedpropertyınfo arabirimi](../../winscript/reference/ienumdebugextendedpropertyinfo-interface.md)   
 [ExtendedDebugPropertyInfo Yapısı](../../winscript/reference/extendeddebugpropertyinfo-structure.md)
---
title: IDebugExtendedProperty::GetExtendedPropertyInfo | Microsoft Docs
ms.custom: ''
ms.date: 01/18/2017
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
apiname:
- IDebugExtendedProperty.GetExtendedPropertyInfo
apilocation:
- scrobj.dll
helpviewer_keywords:
- IDebugExtendedProperty::GetExtendedPropertyInfo
ms.assetid: 56edf538-5082-4653-82b6-e6640d6f61ba
caps.latest.revision: 8
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: 89067720b6643c8c187e6340fb529989f2439933
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62946108"
---
# <a name="idebugextendedpropertygetextendedpropertyinfo"></a>IDebugExtendedProperty::GetExtendedPropertyInfo
Daha fazla bilgiyi daha basit bir genişletilmiş özelliği için genişletilmiş bilgileri getirir `IDebugProperty`.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp
HRESULT GetExtendedPropertyInfo(  
   EX_DBGPROP_INFO_FLAGS  dwFieldSpec,  
   UINT  nRadix,  
   ExtendedDebugPropertyInfo*  pExtendedPropertyInfo  
);  
```  
  
#### <a name="parameters"></a>Parametreler  
 `dwFieldSpec`  
 [in] İçinde doldurulması için alanları belirlemek EX_DBGPROP_INFO_FLAGS sabitlerini belirtir `ExtendedDebugPropertyInfo` yapısı.  
  
 `nRadix`  
 [in] Sayısal yedeklenmesine yorumlama içinde kullanılacak sayı tabanı.  
  
 `pExtendedPropertyInfo`  
 [out] Döndürür `ExtendedDebugPropertyInfo` yapı özelliği tanımlar.  
  
## <a name="return-value"></a>Dönüş Değeri  
 Geçerli bir döndürür `HRESULT`, genellikle `S_OK`.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Idebugextendedproperty arabirimi](../../winscript/reference/idebugextendedproperty-interface.md)   
 [EX_DBGPROP_INFO_FLAGS](../../winscript/reference/ex-dbgprop-info-flags.md)   
 [ExtendedDebugPropertyInfo Yapısı](../../winscript/reference/extendeddebugpropertyinfo-structure.md)
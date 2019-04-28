---
title: IDebugProperty::EnumMembers | Microsoft Docs
ms.custom: ''
ms.date: 01/18/2017
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
apiname:
- IDebugProperty.EnumMembers
apilocation:
- scrobj.dll
helpviewer_keywords:
- IDebugProperty::EnumMembers
ms.assetid: 8ce398a5-6452-4804-ae8f-5c54cd11c661
caps.latest.revision: 8
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: 527bf9d3c51dad8ffe1645dc42081dc54189ad7b
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62979168"
---
# <a name="idebugpropertyenummembers"></a>IDebugProperty::EnumMembers
Bir özellik üyesi numaralandırır.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp
HRESULT EnumMembers (  
   DBGPROP_INFO_FLAGSdwFieldSpec,  
   UINTnRadix,  
   REFIIDrefiid,  
   IEnumDebugPropertyInfo**ppEnum  
);  
```  
  
#### <a name="parameters"></a>Parametreler  
 `dwFieldSpec`  
 [in] Belirtir `DBGPROP_INFO_FLAGS` numaralandırılmış hata ayıklama özelliği yapılardaki hangi alanların doldurulması belirlemek sabitler.  
  
 `nRadix`  
 [in] Sayısal yedeklenmesine yorumlama içinde kullanılacak sayı tabanı.  
  
 `refiid`  
 [in] Bu IID, numaralandırıcı filtreleme için geçirilir. IID biridir `IDebugPropertyEnumType` devralacak arabirimleri `IDebugPropertyEnumType_All`.  
  
 `ppEnum`  
 [out] Döndürür `IEnumDebugPropertyInfo` arabirim üyesi özellikleri listeler.  
  
## <a name="return-value"></a>Dönüş Değeri  
 Geçerli bir döndürür `HRESULT`, genellikle `S_OK`.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Idebugproperty arabirimi](../../winscript/reference/idebugproperty-interface.md)   
 [DBGPROP_INFO_FLAGS](../../winscript/reference/dbgprop-info-flags.md)   
 [Idebugpropertyenumtype_all arabirimi](../../winscript/reference/idebugpropertyenumtype-all-interface.md)   
 [IEnumDebugPropertyInfo Arabirimi](../../winscript/reference/ienumdebugpropertyinfo-interface.md)
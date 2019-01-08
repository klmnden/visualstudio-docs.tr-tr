---
title: IDebugProperty::EnumMembers | Microsoft Docs
ms.custom: ''
ms.date: 01/18/2017
ms.prod: windows-script-interfaces
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
ms.openlocfilehash: 7edf2d2f94519146a81cf94b3bf30946af59bbe9
ms.sourcegitcommit: 116e9614867e0b3c627ce9001012a4c39435a42b
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/08/2019
ms.locfileid: "54097038"
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
---
title: Extendeddebugpropertyınfo yapısı | Microsoft Docs
ms.custom: ''
ms.date: 01/18/2017
ms.prod: windows-script-interfaces
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
apiname:
- ExtendedDebugPropertyInfo
apilocation:
- scrobj.dll
helpviewer_keywords:
- ExtendedDebugPropertyInfo structure
ms.assetid: f2cf6477-454b-4d13-95da-ae4c90daa175
caps.latest.revision: 8
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: e0251d4b578a33a9eb5448c1ceb2b2607f82d43a
ms.sourcegitcommit: 116e9614867e0b3c627ce9001012a4c39435a42b
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/08/2019
ms.locfileid: "54096778"
---
# <a name="extendeddebugpropertyinfo-structure"></a>ExtendedDebugPropertyInfo Yapısı
Genişletir `DebugPropertyInfo` yapısı ile genişletilmiş özelliği nitelemek için ek üyeler.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp
typedef struct ExtendedDebugPropertyInfo{  
   DBGPROP_INFO_FLAGS  dwValidFields;  
   LPOLESTR  bstrName;  
   LPOLESTR  bstrType;  
   LPOLESTR  bstrValue;  
   LPOLESTR  bstrFullName;  
   DBGPROP_ATTRIB_FLAGS  dwAttrib;  
   IDebugProperty*  pDebugProp;  
   DWORD  nDISPID;  
   DWORD  nType;  
   VARIANT  varValue;  
   ILockBytes*  plbValue;  
   IDebugExtendedProperty*  pDebugExtProp;  
};  
```  
  
## <a name="members"></a>Üyeler  
 `dwValidFields`  
 Hangi alanların başlatılır belirtmek için kullanılan bir listelenmiş veri türü.  
  
 `bstrName`  
 Bir bağlam içinde özellik adı.  
  
 `bstrType`  
 Özelliği, biçimlendirilmiş dize olarak yazın.  
  
 `bstrValue`  
 Özellik değeri olarak biçimlendirilmiş bir dize.  
  
 `bstrFullName`  
 Özelliğin tam adı.  
  
 `dwAttrib`  
 Hata ayıklama özellik öznitelikleri için bayrakları belirtir bir sabit listesi.  
  
 `pDebugProp`  
 `IDebugProperty` Bunun için karşılık gelen nesne `ExtendedDebugPropertyInfo`.  
  
 `nDISPID`  
 Dağıtım kimliği.  
  
 `nType`  
 Genişletilmiş özellik türü.  
  
 `varValue`  
 VARIANT sığabilen, genişletilmiş özellik değeri.  
  
 `plbValue`  
 Özellik değerinin gerçek veri baytı.  
  
 `pDebugExtProp`  
 `IDebugExtendedProperty` Bunun için karşılık gelen nesne `ExtendedDebugPropertyInfo`.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Debugpropertyınfo yapısı](../../winscript/reference/debugpropertyinfo-structure.md)   
 [Idebugproperty arabirimi](../../winscript/reference/idebugproperty-interface.md)   
 [Idebugextendedproperty arabirimi](../../winscript/reference/idebugextendedproperty-interface.md)   
 [DBGPROP_ATTRIB_FLAGS](../../winscript/reference/dbgprop-attrib-flags.md)   
 [DBGPROP_INFO_FLAGS](../../winscript/reference/dbgprop-info-flags.md)
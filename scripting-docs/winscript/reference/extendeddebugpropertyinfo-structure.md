---
title: Extendeddebugpropertyınfo yapısı | Microsoft Docs
ms.custom: ''
ms.date: 01/18/2017
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
ms.openlocfilehash: 1fe0eef00d2bf064a8a002925f4ba5607d36f31c
ms.sourcegitcommit: d3a485d47c6ba01b0fc9878cbbb7fe88755b29af
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/18/2019
ms.locfileid: "58160478"
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
---
title: Debugpropertyınfo yapısı | Microsoft Docs
ms.custom: ''
ms.date: 01/18/2017
ms.prod: windows-script-interfaces
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
apiname:
- DebugPropertyInfo
apilocation:
- scrobj.dll
helpviewer_keywords:
- DebugPropertyInfo structure
ms.assetid: 3246efbc-c212-4024-8f07-6414c2f85e75
caps.latest.revision: 8
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: 47c0f6a359341d19b99c1ce8c099ebf1c6d6a1ff
ms.sourcegitcommit: 116e9614867e0b3c627ce9001012a4c39435a42b
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/08/2019
ms.locfileid: "54088991"
---
# <a name="debugpropertyinfo-structure"></a>DebugPropertyInfo Yapısı
Bir nesnenin adı, türü ve değeri içeren bir hiyerarşik yapısını açıklar. Yerel değişkenler, Parametreler, izleme değişkenleri ve ifadeleri hata ayıklama özelliklerini tanımlamak için kullanılır ve kaydeder.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp
typedef struct DebugPropertyInfo{  
   DBGPROP_INFO_FLAGS  dwValidFields;  
   BSTR  bstrName;  
   BSTR  bstrType;  
   BSTR  bstrValue;  
   BSTR  bstrFullName;  
   DBGPROP_ATTRIB_FLAGS  dwAttrib;  
   IDebugProperty*  pDebugProp;  
};  
```  
  
## <a name="members"></a>Üyeler  
 dwValidFields  
 Hangi alanların başlatılır belirtmek için kullanılan bir listelenmiş veri türü.  
  
 bstrName  
 Bir bağlam içinde özellik adı.  
  
 bstrType  
 Biçimlendirilmiş dize olarak özellik türü.  
  
 bstrValue  
 Biçimlendirilmiş dize olarak özellik değeri.  
  
 bstrFullName  
 Özelliğin tam adı.  
  
 dwAttrib  
 Hata ayıklama özellik öznitelikleri için bayrakları belirtir bir sabit listesi.  
  
 pDebugProp  
 `IDebugProperty` Bu bilgileri tarafından açıklanan `DebugPropertyInfo` yapısı.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Idebugproperty arabirimi](../../winscript/reference/idebugproperty-interface.md)   
 [DBGPROP_ATTRIB_FLAGS](../../winscript/reference/dbgprop-attrib-flags.md)   
 [DBGPROP_INFO_FLAGS](../../winscript/reference/dbgprop-info-flags.md)
---
title: Debugpropertyınfo yapısı | Microsoft Docs
ms.custom: ''
ms.date: 01/18/2017
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
ms.openlocfilehash: 99208626b41f2463178bccecf73c21a1d15fa765
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62955269"
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
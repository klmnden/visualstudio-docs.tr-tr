---
title: IEnumDebugPropertyInfo::Skip | Microsoft Docs
ms.custom: ''
ms.date: 01/18/2017
ms.prod: windows-script-interfaces
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
apiname:
- IEnumDebugPropertyInfo.Skip
apilocation:
- scrobj.dll
helpviewer_keywords:
- IEnumDebugPropertyInfo::Skip
ms.assetid: 2f6361fb-d66d-4fc0-8fe0-c859593a183f
caps.latest.revision: 8
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: 72445473a1fe090a468010b33381e8751f1bbc65
ms.sourcegitcommit: 8bf9e51c77a5a602fab9513b9187e59e57dfebad
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/16/2019
ms.locfileid: "54344752"
---
# <a name="ienumdebugpropertyinfoskip"></a>IEnumDebugPropertyInfo::Skip
Belirtilen sayıda atlar `DebugPropertyInfo` yapıları, bir sabit listesi sırası.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp
HRESULT Skip(  
   ULONGcelt  
);  
```  
  
#### <a name="parameters"></a>Parametreler  
 `celt`  
 [in] Sayısını `DebugPropertyInfo` yapılarını atlamak için sabit listesi sırası.  
  
## <a name="return-value"></a>Dönüş Değeri  
 Geçerli bir döndürür `HRESULT`, genellikle `S_OK`. Döndürür `S_FALSE` ve geçerli öğe işaretçisi sabit listesinin sonuna ayarlar `celt` bir numaralandırıcı öğeleri sola sayısından büyüktür.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Ienumdebugpropertyınfo arabirimi](../../winscript/reference/ienumdebugpropertyinfo-interface.md)   
 [DebugPropertyInfo Yapısı](../../winscript/reference/debugpropertyinfo-structure.md)
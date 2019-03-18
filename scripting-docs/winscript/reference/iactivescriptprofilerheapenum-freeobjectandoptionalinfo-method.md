---
title: Iactivescriptprofilerheapenum::freeobjectandoptionalınfo yöntemi | Microsoft Docs
ms.custom: ''
ms.date: 01/18/2017
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
ms.assetid: fdd5f7cc-be4e-4c13-a181-6320d26b44eb
caps.latest.revision: 3
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: c6023ca95b3e861b7bf57db3d37c7949e650419b
ms.sourcegitcommit: d3a485d47c6ba01b0fc9878cbbb7fe88755b29af
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/18/2019
ms.locfileid: "58145349"
---
# <a name="iactivescriptprofilerheapenumfreeobjectandoptionalinfo-method"></a>IActiveScriptProfilerHeapEnum::FreeObjectAndOptionalInfo Yöntemi
Belirtilen boşaltır [profıler_heap_object yapısı](../../winscript/reference/profiler-heap-object-structure.md) yapıları ve bunların ilişkili [profıler_heap_object_optıonal_ınfo yapısı](../../winscript/reference/profiler-heap-object-optional-info-structure.md) öğeleri.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp
HRESULT FreeObjectAndOptionalInfo (    [in] ULONG celt,    [in, size_is(celt)] PROFILER_HEAP_OBJECT** heapObjects);  
```  
  
#### <a name="parameters"></a>Parametreler  
 `celt`  
 Ücretsiz nesnelerin sayısı.  
  
 `heapObjects`  
 Bir dizi [profıler_heap_object yapısı](../../winscript/reference/profiler-heap-object-structure.md) yapıları.  
  
## <a name="return-value"></a>Dönüş Değeri  
 HRESULT.
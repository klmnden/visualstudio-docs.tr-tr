---
title: Iactivescriptprofilerheapenum::freeobjectandoptionalınfo yöntemi | Microsoft Docs
ms.custom: ''
ms.date: 01/18/2017
ms.prod: windows-script-interfaces
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
ms.assetid: fdd5f7cc-be4e-4c13-a181-6320d26b44eb
caps.latest.revision: 3
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: 8dd2b827deba31af1958842cf0dacd2a85f4260d
ms.sourcegitcommit: 116e9614867e0b3c627ce9001012a4c39435a42b
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/08/2019
ms.locfileid: "54095699"
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
---
title: Iactivescriptprofilerheapenum::getoptionalınfo metodu | Microsoft Docs
ms.custom: ''
ms.date: 01/18/2017
ms.prod: windows-script-interfaces
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
ms.assetid: 99ed9df5-71cf-4c25-b189-af9accc466ee
caps.latest.revision: 6
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: bcba1214a0c57e738dec41cdc4976f478802fedc
ms.sourcegitcommit: 116e9614867e0b3c627ce9001012a4c39435a42b
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/08/2019
ms.locfileid: "54088809"
---
# <a name="iactivescriptprofilerheapenumgetoptionalinfo-method"></a>IActiveScriptProfilerHeapEnum::GetOptionalInfo Metodu
Belirtilen nesnenin isteğe bağlı bilgi alır (yığın nesnelerini döndürüldüğü kümesinden [Iactivescriptprofilercontrol3::enumheap yöntemi](../../winscript/reference/iactivescriptprofilercontrol3-enumheap-method.md)).  
  
 Döndürülen nesneye atanmış döndürülen bellek serbest değil. Bunun yerine, çağırmalıdır [Iactivescriptprofilerheapenum::freeobjectandoptionalınfo yöntemi](../../winscript/reference/iactivescriptprofilerheapenum-freeobjectandoptionalinfo-method.md).  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp
HRESULT GetOptionalInfo (    [in] PROFILER_HEAP_OBJECT* heapObject,    [in] ULONG celt,    [out, size_is(celt)] PROFILER_HEAP_OBJECT_OPTIONAL_INFO* optionalInfo);  
```  
  
#### <a name="parameters"></a>Parametreler  
 `heapObject`  
 [Profıler_heap_object yapısı](../../winscript/reference/profiler-heap-object-structure.md) bilgileri döndürülecek.  
  
 `celt`  
 Sayısını [profıler_heap_object_optıonal_ınfo yapısı](../../winscript/reference/profiler-heap-object-optional-info-structure.md) yapılarını döndürmek için.  
  
 `optionalInfo`  
 [out] Bir dizi [profıler_heap_object_optıonal_ınfo yapısı](../../winscript/reference/profiler-heap-object-optional-info-structure.md) yapıları için belirtilen nesne.  
  
## <a name="return-value"></a>Dönüş Değeri  
 HRESULT.
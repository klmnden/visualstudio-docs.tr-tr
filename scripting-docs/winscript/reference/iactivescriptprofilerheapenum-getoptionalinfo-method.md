---
title: Iactivescriptprofilerheapenum::getoptionalınfo metodu | Microsoft Docs
ms.custom: ''
ms.date: 01/18/2017
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
ms.assetid: 99ed9df5-71cf-4c25-b189-af9accc466ee
caps.latest.revision: 6
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: ab8096b79cfbb91e4b65256c84ab1ba01207d9ed
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62992850"
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
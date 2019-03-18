---
title: Profıler_heap_object_flags sabit listesi | Microsoft Docs
ms.custom: ''
ms.date: 01/18/2017
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
ms.assetid: 0f517743-cc4a-4911-add3-a43680071a1f
caps.latest.revision: 6
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: f7fde5ed275691d78e534cd7b8d8e958a8f20325
ms.sourcegitcommit: d3a485d47c6ba01b0fc9878cbbb7fe88755b29af
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/18/2019
ms.locfileid: "58149425"
---
# <a name="profilerheapobjectflags-enumeration"></a>PROFILER_HEAP_OBJECT_FLAGS Numaralandırması
Yığın nesnesi hakkında temel bilgiler sunulmayacağını belirten bayrak. Kullanılan [profıler_heap_object yapısı](../../winscript/reference/profiler-heap-object-structure.md).  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp
typedef [v1_enum] enum {    PROFILER_HEAP_OBJECT_FLAGS_NEW_OBJECT            = 0x00000001,    PROFILER_HEAP_OBJECT_FLAGS_IS_ROOT               = 0x00000002,    PROFILER_HEAP_OBJECT_FLAGS_SITE_CLOSED           = 0x00000004,    PROFILER_HEAP_OBJECT_FLAGS_EXTERNAL              = 0x00000008,    PROFILER_HEAP_OBJECT_FLAGS_EXTERNAL_UNKNOWN      = 0x00000010,    PROFILER_HEAP_OBJECT_FLAGS_EXTERNAL_DISPATCH     = 0x00000020,    PROFILER_HEAP_OBJECT_FLAGS_SIZE_APPROXIMATE      = 0x00000040,    PROFILER_HEAP_OBJECT_FLAGS_SIZE_UNAVAILABLE      = 0x00000080,    PROFILER_HEAP_OBJECT_FLAGS_NEW_STATE_UNAVAILABLE = 0x00000100,    PROFILER_HEAP_OBJECT_FLAGS_WINRT_INSTANCE        = 0x00000200,    PROFILER_HEAP_OBJECT_FLAGS_WINRT_RUNTIMECLASS    = 0x00000400,    PROFILER_HEAP_OBJECT_FLAGS_WINRT_DELEGATE        = 0x00000800,    PROFILER_HEAP_OBJECT_FLAGS_WINRT_NAMESPACE       = 0x00001000,} PROFILER_HEAP_OBJECT_FLAGS;  
```  
  
## <a name="members"></a>Üyeler  
  
|Üye|Değer|Açıklama|  
|------------|-----------|-----------------|  
|PROFILER_HEAP_OBJECT_FLAGS_NEW_OBJECT|0x00000001|Bu yığın nesnesi, önceki yığın numaralandırma istekten sonra ayrıldı. [Profıler_heap_object_ıd türü](../../winscript/reference/profiler-heap-object-id-type.md) nesne toplanırsa değerleri yeniden kullanılabilir.|  
|PROFILER_HEAP_OBJECT_FLAGS_IS_ROOT|0x00000002|Bu yığın nesnesi bir nesne grafiğinin kök nesnesidir.|  
|PROFILER_HEAP_OBJECT_FLAGS_SITE_CLOSED|0x00000004|Bu yığın nesnesi bir betik siteden kapatıldı ' dir.|  
|PROFILER_HEAP_OBJECT_FLAGS_EXTERNAL|0x00000008|Bu yığın nesnesi, JavaScript atık toplama yığınındaki dışında ayrıldı.|  
|PROFILER_HEAP_OBJECT_FLAGS_EXTERNAL_UNKNOWN|0x00000010|Bu yığın nesnesi, IUnknown uygular ve çöp toplama yığınındaki dışında ayrıldı.|  
|PROFILER_HEAP_OBJECT_FLAGS_EXTERNAL_DISPATCH|0x00000020|Bu yığın nesnesi, çöp toplama yığınındaki dışında ayrıldı ve IDİSPATCH arabirimi uygular.|  
|PROFILER_HEAP_OBJECT_FLAGS_SIZE_APPROXIMATE|0x00000040|Bu yığın nesnesi yaklaşık boyutudur.|  
|PROFILER_HEAP_OBJECT_FLAGS_SIZE_UNAVAILABLE|x00000080|Bu yığın nesnesi boyutu kullanılamıyor.|  
|PROFILER_HEAP_OBJECT_FLAGS_WINRT_INSTANCE|0x00000200|Yığın nesnesi, bir Windows çalışma zamanı örneğidir.|  
|PROFILER_HEAP_OBJECT_FLAGS_WINRT_RUNTIMECLASS|0x00000400|Yığın nesnesi bir Windows Çalışma Zamanı Modülü çalışma zamanı sınıftır.|  
|PROFILER_HEAP_OBJECT_FLAGS_WINRT_DELEGATE|0x00000800|Yığın nesnesi, bir Windows çalışma zamanı temsilcisidir.|  
|PROFILER_HEAP_OBJECT_FLAGS_WINRT_NAMESPACE|0x00001000|Yığın nesnesi, Windows çalışma zamanı ad alanındadır.|
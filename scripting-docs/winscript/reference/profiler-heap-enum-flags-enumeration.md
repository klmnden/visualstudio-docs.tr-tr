---
title: Profıler_heap_enum_flags sabit listesi | Microsoft Docs
ms.custom: ''
ms.date: 01/18/2017
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
ms.assetid: 17936b7a-40d5-4774-b92b-b24ee391591e
caps.latest.revision: 6
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: d613ed3bcb4699f20d521f08b6c34d55d8363ba4
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62830363"
---
# <a name="profilerheapenumflags-enumeration"></a>PROFILER_HEAP_ENUM_FLAGS Numaralandırması
İçin bir nesne ilişkisini işaret eden yığın nesnesi hakkında ek bilgilerin kullanıma sunulup sunulmayacağını belirten bayrak. Kullanılan [EnumHeap2](../../winscript/reference/iactivescriptprofilercontrol5-enumheap2-method.md) yöntemi.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp
typedef [v1_enum] enum {    PROFILER_HEAP_ENUM_FLAGS_NONE                      = 0x00000000,    PROFILER_HEAP_ENUM_FLAGS_STORE_RELATIONSHIP_FLAGS  = 0x00000001,} PROFILER_HEAP_ENUM_FLAGS;  
```  
  
## <a name="members"></a>Üyeler  
  
|Üye|Değer|Açıklama|  
|------------|-----------|-----------------|  
|PROFILER_HEAP_ENUM_FLAGS_NONE|0x00000000|Bu yığın nesnesi bir nesne ilişkisi hakkında ek bilgilerin kullanıma sunmuyor. Bu yığın nesnesi aynı şekilde davranır [IActiveScriptProfilerControl3::HeapEnum](../../winscript/reference/iactivescriptprofilercontrol3-enumheap-method.md).|  
|PROFILER_HEAP_ENUM_ENUM_ STORE_RELATIONSHIP_FLAGS|0x00000001|Bu yığın nesnesi olup olmadığı için bir nesne ilişkisini işaret eden bir nesnenin alıcı veya ayarlayıcı yöntemlerinden olduğu konusunda bilgi içerir. Bu bilgiler, 2 baytında (16 bit) depolanır [profıler_heap_object_relatıonshıp.relationshipınfo](../../winscript/reference/profiler-heap-object-relationship-structure.md) biri olarak alan [profıler_heap_object_relatıonshıp_flags](../../winscript/reference/profiler-heap-object-relationship-flags-enumeration.md) sabit listesi değerleri.|  
|PROFILER_HEAP_ENUM_FLAGS_SUBSTRINGS|0x00000002|Bu yığın nesnesi, alt dizenin düzgün görüntülenmesi için kullanılır.|  
|PROFILER_HEAP_ENUM_FLAGS_RELATIONSHIP_SUBSTRINGS|PROFILER_HEAP_ENUM_FLAGS_STORE_RELATIONSHIP_FLAGS &AMP;#124; PROFILER_HEAP_ENUM_FLAGS_SUBSTRINGS|Bu yığın nesnesi, alt dizenin düzgün görüntülenmesi için kullanılır.|
---
title: Profıler_heap_object_relatıonshıp_flags numaralandırması | Microsoft Docs
ms.custom: ''
ms.date: 01/18/2017
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
ms.assetid: 1a41b642-c9a9-4d83-b943-d59b232eebf6
caps.latest.revision: 4
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: 322f6f3352c1b0dfad4572d55e1ebe2388c8cc4a
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62823640"
---
# <a name="profilerheapobjectrelationshipflags-enumeration"></a>PROFILER_HEAP_OBJECT_RELATIONSHIP_FLAGS Numaralandırması
Bir yığın nesnesi bir nesne ilişkisini işaret olduğunu belirten bayrak alıcı veya ayarlayıcı yöntemidir. Kullanılan [EnumHeap2](../../winscript/reference/iactivescriptprofilercontrol5-enumheap2-method.md) profıler_heap_object_relatıonshıp_flags değeri belirtildiğinde yöntemi `enumFlags` parametresi.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp
typedef [v1_enum] enum {    PROFILER_HEAP_OBJECT_RELATIONSHIP_FLAGS_NONE                      = 0x00000000,    PROFILER_HEAP_OBJECT_RELATIONSHIP_FLAGS_IS_GET_ACCESSOR           = 0x00010000,    PROFILER_HEAP_OBJECT_RELATIONSHIP_FLAGS_IS_SET_ACCESSOR           = 0x00020000,} PROFILER_HEAP_OBJECT_RELATIONSHIP_FLAGS;  
```  
  
## <a name="members"></a>Üyeler  
  
|Üye|Değer|Açıklama|  
|------------|-----------|-----------------|  
|PROFILER_HEAP_OBJECT_RELATIONSHIP_FLAGS_NONE|0x00000000|İçin bir nesne ilişkisini işaret eden Bu yığın nesnesi bir alıcı veya ayarlayıcı yöntemi olarak tanımlanmamış.|  
|PROFILER_HEAP_OBJECT_RELATIONSHIP_FLAGS_IS_GET_ACCESSOR|0x00010000|İçin bir nesne ilişkisini işaret eden yığın nesnesi bir alıcı yöntemidir. Bu bilgiler, 2 baytında (16 bit) depolanır [profıler_heap_object_relatıonshıp.relationshipınfo](../../winscript/reference/profiler-heap-object-relationship-structure.md) alan.|  
|PROFILER_HEAP_OBJECT_RELATIONSHIP_FLAGS_IS_SET_ACCESSOR|0x00020000|İçin bir nesne ilişkisini işaret eden yığın nesnesi bir ayarlayıcı yöntemidir. Bu bilgiler, 2 baytında (16 bit) depolanır `PROFILER_HEAP_OBJECT_RELATIONSHIP.relationshipInfo` alan.|
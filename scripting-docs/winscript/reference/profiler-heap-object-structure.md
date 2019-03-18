---
title: Profıler_heap_object yapısı | Microsoft Docs
ms.custom: ''
ms.date: 01/18/2017
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
ms.assetid: 9f35362c-6856-4cfb-b990-031a156a58eb
caps.latest.revision: 4
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: a1652c6ebffff88782ffcc879158a5142f22395d
ms.sourcegitcommit: d3a485d47c6ba01b0fc9878cbbb7fe88755b29af
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/18/2019
ms.locfileid: "58151199"
---
# <a name="profilerheapobject-structure"></a>PROFILER_HEAP_OBJECT Yapısı
Yığın nesnelerini toplanan tarafından temsil [Iactivescriptprofilercontrol3::enumheap yöntemi](../../winscript/reference/iactivescriptprofilercontrol3-enumheap-method.md).  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp
typedef struct _PROFILER_HEAP_OBJECT  
{  
    UINT size;    union {        PROFILER_HEAP_OBJECT_ID objectId;        PROFILER_EXTERNAL_OBJECT_ADDRESS externalObjectAddress;    };    PROFILER_HEAP_OBJECT_NAME_ID typeNameId;    USHORT flags;     USHORT optionalInfoCount;} PROFILER_HEAP_OBJECT;  
```  
  
## <a name="members"></a>Üyeler  
  
|Üye|Tür|Açıklama|  
|------------|----------|-----------------|  
|objectId|[PROFILER_HEAP_OBJECT_ID Türü](../../winscript/reference/profiler-heap-object-id-type.md)|Yığın nesnesinin kimliği.|  
|externalObjectAddress|[PROFILER_EXTERNAL_OBJECT_ADDRESS Türü](../../winscript/reference/profiler-external-object-address-type.md)|JavaScript yığın dışında bir C++ ayrılmış bir nesne gibi bir nesne dış nesne adresi.|  
|typeNameId|[PROFILER_HEAP_OBJECT_NAME_ID Türü](../../winscript/reference/profiler-heap-object-name-id-type.md)|Yığın nesnesi türü adı kimliği öğesinden alınan [IActiveScriptProfilerHeapEnum::GetNameIdMap](../../winscript/reference/iactivescriptprofilerheapenum-getnameidmap.md). Yalnızca biri `externalObjectAddress` veya `typeName` bağlı olarak mevcut olduğundan `flags` değeri.|  
|bayraklar|[PROFILER_HEAP_OBJECT_FLAGS Sabit Listesi](../../winscript/reference/profiler-heap-object-flags-enumeration.md)|Yığın nesnesi hakkında temel bilgiler içeren bayraklar.|  
|optionalInfoCount|USHORT|Sayısını [profıler_heap_object_optıonal_ınfo yapısı](../../winscript/reference/profiler-heap-object-optional-info-structure.md) yığın nesnesi için kullanılabilir olan kayıtları.|
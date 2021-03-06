---
title: Profıler_heap_object_relatıonshıp yapısı | Microsoft Docs
ms.custom: ''
ms.date: 01/18/2017
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
ms.assetid: 3ab3d986-3314-4c7b-a1c8-18ed691a8b9c
caps.latest.revision: 7
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: 7a905a44f2ef686181c5a859699277d16f6cd374
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62823627"
---
# <a name="profilerheapobjectrelationship-structure"></a>PROFILER_HEAP_OBJECT_RELATIONSHIP Yapısı
Bir yığın nesnesinin bir ilişkiyi temsil eder.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp
typedef struct _PROFILER_HEAP_OBJECT_RELATIONSHIP{    PROFILER_HEAP_OBJECT_NAME_ID relationshipId;    PROFILER_RELATIONSHIP_INFO relationshipInfo;    [switch_type(PROFILER_RELATIONSHIP_INFO), switch_is(relationshipInfo)] union    {        [case(PROFILER_PROPERTY_TYPE_NUMBER)] double numberValue;        [case(PROFILER_PROPERTY_TYPE_STRING)] LPCWSTR stringValue;        [case(PROFILER_PROPERTY_TYPE_HEAP_OBJECT)] PROFILER_HEAP_OBJECT_ID objectId;        [case(PROFILER_PROPERTY_TYPE_EXTERNAL_OBJECT)] PROFILER_EXTERNAL_OBJECT_ADDRESS externalObjectAddress;    };} PROFILER_HEAP_OBJECT_RELATIONSHIP;  
```  
  
## <a name="members"></a>Üyeler  
  
|Üye|Değer|Açıklama|  
|------------|-----------|-----------------|  
|RelationshipID|[PROFILER_HEAP_OBJECT_NAME_ID Türü](../../winscript/reference/profiler-heap-object-name-id-type.md)|İlişki kimliği ad alanından [IActiveScriptProfilerHeapEnum::GetNameIdMap](../../winscript/reference/iactivescriptprofilerheapenum-getnameidmap.md).|  
|Relationshipınfo|[PROFILER_RELATIONSHIP_INFO Sabit Listesi](../../winscript/reference/profiler-relationship-info-enumeration.md)|İlişki hakkında bilgi sağlar.|  
|numberValue|çift|Sayı değeri. Yalnızca biri `numberValue` / `stringValue` / `objectId` / `externalObjectAddress` ayarlayın, temel `relationshipInfo` değeri.|  
|stringValue|LPCWSTR|Dize değeri.|  
|objectId|[PROFILER_HEAP_OBJECT_ID Türü](../../winscript/reference/profiler-heap-object-id-type.md)|Yığın nesnesinin kimliği.|  
|externalObjectAddress|[PROFILER_EXTERNAL_OBJECT_ADDRESS Türü](../../winscript/reference/profiler-external-object-address-type.md)|Dış nesnesi adresi.|  
|alt dize|[PROFILER_PROPERTY_TYPE_SUBSTRING_INFO Yapısı](../../winscript/reference/profiler-property-type-substring-info-structure.md)|Alt dize türü hakkındaki bilgiler.|
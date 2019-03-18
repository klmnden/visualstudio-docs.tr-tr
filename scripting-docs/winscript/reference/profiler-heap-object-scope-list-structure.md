---
title: Profıler_heap_object_scope_lıst yapısı | Microsoft Docs
ms.custom: ''
ms.date: 01/18/2017
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
ms.assetid: 33ebaa31-0a35-47d5-a4e3-afd83e16f53e
caps.latest.revision: 5
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: b1285e4efa3db8a7ec99808f5888d3dbf948e589
ms.sourcegitcommit: d3a485d47c6ba01b0fc9878cbbb7fe88755b29af
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/18/2019
ms.locfileid: "58152528"
---
# <a name="profilerheapobjectscopelist-structure"></a>PROFILER_HEAP_OBJECT_SCOPE_LIST Yapısı
Bu yapı, işlev nesneleri ile ilişkilidir. Kapsam listesi, her kapsam her verilen kapsam içinde değişkenlere temsil eden bir ilişkili özelliğin listesiyle bir yığın nesnesi olduğu kapsamların listesini olarak işlevin kabini temsil eder. Bazı durumlarda, kapsam kullanılamayabilir nesneleri ve özellik listesi yalnızca kendi dizine adları kullanılabilir.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp
typedef struct _PROFILER_HEAP_OBJECT_SCOPE_LIST{    UINT count;    [size_is(count)] PROFILER_HEAP_OBJECT_ID scopes[];} PROFILER_HEAP_OBJECT_SCOPE_LIST;  
```  
  
## <a name="members"></a>Üyeler  
  
|Üye|Tür|Açıklama|  
|------------|----------|-----------------|  
|count|UINT|Kapsamların sayısı|  
|kapsamlar|[PROFILER_HEAP_OBJECT_ID Türü](../../winscript/reference/profiler-heap-object-id-type.md)|Kapsamları dizisi.|
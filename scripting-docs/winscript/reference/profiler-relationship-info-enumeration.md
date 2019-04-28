---
title: Profıler_relatıonshıp_ınfo sabit listesi | Microsoft Docs
ms.custom: ''
ms.date: 01/18/2017
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
ms.assetid: fae69317-6224-4a6a-8e9e-ccaa6a330818
caps.latest.revision: 6
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: 0aa0a94668d06f75b959de2ee933ab079feba596
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62808899"
---
# <a name="profilerrelationshipinfo-enumeration"></a>PROFILER_RELATIONSHIP_INFO Numaralandırması
İlişki nesnesinde ilgili bilgileri temsil eder. Kullanılan [profıler_heap_object_relatıonshıp yapısı](../../winscript/reference/profiler-heap-object-relationship-structure.md).  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp
typedef [v1_enum] enum {    PROFILER_PROPERTY_TYPE_NUMBER = 0x01,    PROFILER_PROPERTY_TYPE_STRING = 0x02,    PROFILER_PROPERTY_TYPE_HEAP_OBJECT = 0x03,    PROFILER_PROPERTY_TYPE_EXTERNAL_OBJECT = 0x04,    PROFILER_PROPERTY_TYPE_BSTR = 0x05,} PROFILER_RELATIONSHIP_INFO;  
```  
  
## <a name="members"></a>Üyeler  
  
|Üye|Değer|Açıklama|  
|------------|-----------|-----------------|  
|PROFILER_PROPERTY_TYPE_NUMBER|0x01|Nesne bir sayıdır.|  
|PROFILER_PROPERTY_TYPE_STRING|0x02|Nesne bir dizedir.|  
|PROFILER_PROPERTY_TYPE_HEAP_OBJECT|0x03|Yığın nesnesi bir nesnedir.|  
|PROFILER_PROPERTY_TYPE_EXTERNAL_OBJECT|0x04|Nesnesi diğer bir deyişle, çöp toplama yığını üzerinde dış değil.|  
|PROFILER_PROPERTY_TYPE_BSTR|0x05|BSTR nesnedir.|  
|PROFILER_PROPERTY_TYPE_SUBSTRING|0x06|Bir alt DİZESİ nesnedir.|
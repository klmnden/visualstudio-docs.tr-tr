---
title: Profıler_relatıonshıp_ınfo sabit listesi | Microsoft Docs
ms.custom: ''
ms.date: 01/18/2017
ms.prod: windows-script-interfaces
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
ms.assetid: fae69317-6224-4a6a-8e9e-ccaa6a330818
caps.latest.revision: 6
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: e95b11537873d3bfe02bf3fa793b61ace10938aa
ms.sourcegitcommit: 116e9614867e0b3c627ce9001012a4c39435a42b
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/08/2019
ms.locfileid: "54095816"
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
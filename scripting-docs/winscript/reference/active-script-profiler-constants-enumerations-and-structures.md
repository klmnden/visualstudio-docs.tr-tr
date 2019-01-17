---
title: Etkin komut dosyası Profiler sabitleri, numaralandırmaları ve yapıları | Microsoft Docs
ms.custom: ''
ms.date: 01/18/2017
ms.prod: windows-script-interfaces
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
ms.assetid: 6e079d84-9dde-46fc-8a6a-18e902f60ecc
caps.latest.revision: 12
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: 6d367374e4402da2d30cd8a855a509299363f882
ms.sourcegitcommit: 8bf9e51c77a5a602fab9513b9187e59e57dfebad
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/16/2019
ms.locfileid: "54349133"
---
# <a name="active-script-profiler-constants-enumerations-and-structures"></a>Etkin Komut Dosyası Profil Oluşturucu Sabitleri, Numaralandırmaları ve Yapıları 
Aşağıdaki numaralandırmalar etkin komut dosyası Profiler arabirimleri tarafından kullanılır.  
  
## <a name="constants-enumerations-and-structures"></a>Sabitler, Listelemeler ve Yapılar  
  
|Sabitler|Açıklama|  
|---------------|-----------------|  
|[PROFILER_EXTERNAL_OBJECT_ADDRESS Türü](../../winscript/reference/profiler-external-object-address-type.md)|Profil Oluşturucu dış nesnesi adresi. Kullanılan [profıler_heap_object yapısı](../../winscript/reference/profiler-heap-object-structure.md) ve [profıler_heap_object_relatıonshıp yapısı](../../winscript/reference/profiler-heap-object-relationship-structure.md).|  
|[PROFILER_HEAP_OBJECT_ID Türü](../../winscript/reference/profiler-heap-object-id-type.md)|Yığın nesnesinin kimliği. Kullanılan [profıler_heap_object yapısı](../../winscript/reference/profiler-heap-object-structure.md)[profıler_heap_object_scope_lıst yapısı](../../winscript/reference/profiler-heap-object-scope-list-structure.md), [profıler_heap_object_optıonal_ınfo yapısı](../../winscript/reference/profiler-heap-object-optional-info-structure.md)ve [Profıler_heap_object_relatıonshıp yapısı](../../winscript/reference/profiler-heap-object-relationship-structure.md).|  
|[PROFILER_HEAP_OBJECT_NAME_ID Türü](../../winscript/reference/profiler-heap-object-name-id-type.md)|Yığın nesnesi adı kimliği. Kullanılan [profıler_heap_object yapısı](../../winscript/reference/profiler-heap-object-structure.md).|  
  
|Numaralandırmalar|Açıklama|  
|------------------|-----------------|  
|[PROFILER_EVENT_MASK Sabit Listesi](../../winscript/reference/profiler-event-mask-enumeration.md)|Profili oluşturulması olay türlerini belirtir.|  
|[PROFILER_HEAP_ENUM_FLAGS Sabit Listesi](../../winscript/reference/profiler-heap-enum-flags-enumeration.md)|İçin bir nesne ilişkisini işaret eden yığın nesnesi hakkında ek bilgilerin kullanıma sunulup sunulmayacağını belirten bayrak. Kullanılan [Iactivescriptprofilercontrol5::enumheap2 yöntemi](../../winscript/reference/iactivescriptprofilercontrol5-enumheap2-method.md).|  
|[PROFILER_HEAP_OBJECT_FLAGS Sabit Listesi](../../winscript/reference/profiler-heap-object-flags-enumeration.md)|Yığın nesnesi hakkında temel bilgiler sunulmayacağını belirten bayrak. Kullanılan [profıler_heap_object yapısı](../../winscript/reference/profiler-heap-object-structure.md).|  
|[PROFILER_HEAP_OBJECT_OPTIONAL_INFO_TYPE Sabit Listesi](../../winscript/reference/profiler-heap-object-optional-info-type-enumeration.md)|Farklı tür isteğe bağlı bilgileri temsil eder. Kullanılan [profıler_heap_object_optıonal_ınfo yapısı](../../winscript/reference/profiler-heap-object-optional-info-structure.md).|  
|[PROFILER_RELATIONSHIP_INFO Sabit Listesi](../../winscript/reference/profiler-relationship-info-enumeration.md)|İlişki nesnesinde ilgili bilgileri temsil eder. Kullanılan [profıler_heap_object_relatıonshıp yapısı](../../winscript/reference/profiler-heap-object-relationship-structure.md).|  
|[PROFILER_SCRIPT_TYPE Sabit Listesi](../../winscript/reference/profiler-script-type-enumeration.md)|Betik türünü belirtir.|  
  
|Yapılar|Açıklama|  
|----------------|-----------------|  
|[PROFILER_HEAP_OBJECT Yapısı](../../winscript/reference/profiler-heap-object-structure.md)|Yığın nesnelerini toplanan tarafından temsil [Iactivescriptprofilercontrol3::enumheap yöntemi](../../winscript/reference/iactivescriptprofilercontrol3-enumheap-method.md).|  
|[PROFILER_HEAP_OBJECT_OPTIONAL_INFO Yapısı](../../winscript/reference/profiler-heap-object-optional-info-structure.md)|Yığın nesneleri hakkında isteğe bağlı bilgileri temsil eder.|  
|[PROFILER_HEAP_OBJECT_RELATIONSHIP Yapısı](../../winscript/reference/profiler-heap-object-relationship-structure.md)|Bir yığın nesnesinin bir ilişkiyi temsil eder.|  
|[PROFILER_HEAP_OBJECT_RELATIONSHIP_LIST Yapısı](../../winscript/reference/profiler-heap-object-relationship-list-structure.md)|Bir yığın nesnesine ait bir ilişki listesini temsil eder.|  
|[PROFILER_HEAP_OBJECT_SCOPE_LIST Yapısı](../../winscript/reference/profiler-heap-object-scope-list-structure.md)|Bu yapı, işlev nesneleri ile ilişkilidir. Kapsam listesi, her kapsam her verilen kapsam içinde değişkenlere temsil eden bir ilişkili özelliğin listesiyle bir yığın nesnesi olduğu kapsamların listesini olarak işlevin kabini temsil eder. Bazı durumlarda, söz konusu kapsamındaki nesnelerin adlarını, kullanılamayabilir yalnızca kimlikleri.|  
|[PROFILER_PROPERTY_TYPE_SUBSTRING_INFO Yapısı](../../winscript/reference/profiler-property-type-substring-info-structure.md)|Alt dizenin türü ile ilgili bilgileri temsil eder.|  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Etkin Betik Profil Oluşturucu Arabirimleri](../../winscript/reference/active-script-profiler-interfaces.md)
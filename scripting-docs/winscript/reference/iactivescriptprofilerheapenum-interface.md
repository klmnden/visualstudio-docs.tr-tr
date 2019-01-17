---
title: Iactivescriptprofilerheapenum arabirimi | Microsoft Docs
ms.custom: ''
ms.date: 01/18/2017
ms.prod: windows-script-interfaces
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
ms.assetid: 16756d0e-547a-4825-8b7b-a7e0e4708a04
caps.latest.revision: 6
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: 14562654e0fd3f3567d6f598f84cf2c966b1b8cb
ms.sourcegitcommit: 8bf9e51c77a5a602fab9513b9187e59e57dfebad
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/16/2019
ms.locfileid: "54344895"
---
# <a name="iactivescriptprofilerheapenum-interface"></a>IActiveScriptProfilerHeapEnum Arabirimi
Yığın üzerinde bir yineleyici nesneleri tarafından toplanan, bir komut dosyası altyapısı ile ilişkili [Iactivescriptprofilercontrol3::enumheap yöntemi](../../winscript/reference/iactivescriptprofilercontrol3-enumheap-method.md).  
  
## <a name="syntax"></a>Sözdizimi  
  
```vb  
interface IActiveScriptProfilerHeapEnum : IUnknown  
```  
  
## <a name="methods"></a>Yöntemler  
 [IActiveScriptProfilerHeapEnum::Next Metodu](../../winscript/reference/iactivescriptprofilerheapenum-next-method.md)  
 Sonraki nesne veya nesneler tarafından toplanan yığında nesne kümesini alır [Iactivescriptprofilercontrol3::enumheap yöntemi](../../winscript/reference/iactivescriptprofilercontrol3-enumheap-method.md).  
  
 [IActiveScriptProfilerHeapEnum::GetOptionalInfo Metodu](../../winscript/reference/iactivescriptprofilerheapenum-getoptionalinfo-method.md)  
 Belirtilen nesne üzerindeki isteğe bağlı bilgileri tarafından toplanan yığında nesne kümesini alır [Iactivescriptprofilercontrol3::enumheap yöntemi](../../winscript/reference/iactivescriptprofilercontrol3-enumheap-method.md).  
  
 [IActiveScriptProfilerHeapEnum::FreeObjectAndOptionalInfo Metodu](../../winscript/reference/iactivescriptprofilerheapenum-freeobjectandoptionalinfo-method.md)  
 Belirtilen boşaltır [profıler_heap_object yapısı](../../winscript/reference/profiler-heap-object-structure.md) yapıları ve bunların ilişkili [profıler_heap_object_optıonal_ınfo yapısı](../../winscript/reference/profiler-heap-object-optional-info-structure.md) öğeleri.  
  
 [IActiveScriptProfilerHeapEnum::GetNameIdMap](../../winscript/reference/iactivescriptprofilerheapenum-getnameidmap.md)  
 Karşılık gelen dize adlarını döndürür [profıler_heap_object_name_ıd türü](../../winscript/reference/profiler-heap-object-name-id-type.md) değerleri...
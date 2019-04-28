---
title: Iactivescriptprofilercontrol5::enumheap2 yöntemi | Microsoft Docs
ms.custom: ''
ms.date: 01/18/2017
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
ms.assetid: a25859eb-ac28-4a97-bcb3-33788982a76b
caps.latest.revision: 4
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: 0c90c536dee76d67fdb93dd205e8f6eedff6dcc7
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62992945"
---
# <a name="iactivescriptprofilercontrol5enumheap2-method"></a>IActiveScriptProfilerControl5::EnumHeap2 Yöntemi
Bir arabirim döndürür ([Iactivescriptprofilerheapenum arabirimi](../../winscript/reference/iactivescriptprofilerheapenum-interface.md)) üzerinden ilişkili komut dosyası motoru bağlamında GC yığın nesnelerini yinelemek için kullanılabilecek.  
  
 Bu yöntem çağrısı hata ayıklama veya yayınlama modunda. UI iş parçacığı boşta olduğunda bu yöntem çağrılmalıdır. Dışında betik altyapısına karşı yöntemi çağrıldıktan sonra hiçbir işlem gerçekleştirilmelidir [Iactivescriptprofilerheapenum::Next yöntemi](../../winscript/reference/iactivescriptprofilerheapenum-next-method.md) kadar [Iactivescriptprofilerheapenum::Next yöntemi](../../winscript/reference/iactivescriptprofilerheapenum-next-method.md)S_FALSE döndürür veya [Iactivescriptprofilerheapenum arabirimi](../../winscript/reference/iactivescriptprofilerheapenum-interface.md) arabirim işaretçisi serbest.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp
HRESULT EnumHeap2(    [in] PROFILER_HEAP_ENUM_FLAGS enumFlags,    [out] IActiveScriptProfilerHeapEnum** ppEnum);  
```  
  
#### <a name="parameters"></a>Parametreler  
 enumFlags  
 İçin bir nesne ilişkisini işaret eden bir nesne hakkında ek bilgilerin kullanıma sunulan olup olmadığını belirten değer. Ek bilgiler, işaret edilen nesnenin alıcı veya ayarlayıcı yöntemi olup olmadığını gösterebilir. Daha fazla bilgi için bkz. [profıler_heap_enum_flags numaralandırması](../../winscript/reference/profiler-heap-enum-flags-enumeration.md).  
  
 ppEnum  
 [out] Döndürür [Iactivescriptprofilerheapenum arabirimi](../../winscript/reference/iactivescriptprofilerheapenum-interface.md).  
  
## <a name="return-value"></a>Dönüş Değeri  
 HRESULT döndürür. Olası değerler aşağıdaki gibidir:  
  
|Dönüş Değeri|Açıklama|  
|------------------|-------------|  
|`S_OK`|Bir yığın numaralandırma başarıyla tamamlandı.|  
|`E_OUTOFMEMORY`|Yığın numaralandırma gerçekleştirmek yeterli bellek yoktu.|  
|`E_FAIL`|Bir iç hata oluştu.|
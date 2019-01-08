---
title: Iactivescriptprofilercontrol5::enumheap2 yöntemi | Microsoft Docs
ms.custom: ''
ms.date: 01/18/2017
ms.prod: windows-script-interfaces
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
ms.assetid: a25859eb-ac28-4a97-bcb3-33788982a76b
caps.latest.revision: 4
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: 21661953edbdba2314b88aad5fb55451b06b51a8
ms.sourcegitcommit: 116e9614867e0b3c627ce9001012a4c39435a42b
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/08/2019
ms.locfileid: "54097636"
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
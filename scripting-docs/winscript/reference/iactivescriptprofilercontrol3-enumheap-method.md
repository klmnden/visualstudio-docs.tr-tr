---
title: Iactivescriptprofilercontrol3::enumheap yöntemi | Microsoft Docs
ms.custom: ''
ms.date: 01/18/2017
ms.prod: windows-script-interfaces
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
ms.assetid: 2799d06d-20dd-4c12-9646-554c0ea3606e
caps.latest.revision: 5
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: 25e81a4aa631c142d4444c0578742f68001a108d
ms.sourcegitcommit: 8bf9e51c77a5a602fab9513b9187e59e57dfebad
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/16/2019
ms.locfileid: "54347378"
---
# <a name="iactivescriptprofilercontrol3enumheap-method"></a>IActiveScriptProfilerControl3::EnumHeap Yöntemi
Bir arabirim döndürür ([Iactivescriptprofilerheapenum arabirimi](../../winscript/reference/iactivescriptprofilerheapenum-interface.md)) üzerinden ilişkili komut dosyası motoru bağlamında GC yığın nesnelerini yinelemek için kullanılabilecek.  
  
 Bu yöntem çağrısı hata ayıklama veya yayınlama modunda. UI iş parçacığı boşta olduğunda bu yöntem çağrılmalıdır. Dışında betik altyapısına karşı yöntemi çağrıldıktan sonra hiçbir işlem gerçekleştirilmelidir [Iactivescriptprofilerheapenum::Next yöntemi](../../winscript/reference/iactivescriptprofilerheapenum-next-method.md) kadar [Iactivescriptprofilerheapenum::Next yöntemi](../../winscript/reference/iactivescriptprofilerheapenum-next-method.md)S_FALSE döndürür veya [Iactivescriptprofilerheapenum arabirimi](../../winscript/reference/iactivescriptprofilerheapenum-interface.md) arabirim işaretçisi serbest.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp
HRESULT EnumHeap([out] IActiveScriptProfilerHeapEnum** ppEnum);  
```  
  
#### <a name="parameters"></a>Parametreler  
 ppEnum  
 [out] Döndürür [Iactivescriptprofilerheapenum arabirimi](../../winscript/reference/iactivescriptprofilerheapenum-interface.md).  
  
## <a name="return-value"></a>Dönüş Değeri  
 HRESULT.
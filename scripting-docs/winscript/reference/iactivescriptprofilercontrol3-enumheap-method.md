---
title: Iactivescriptprofilercontrol3::enumheap yöntemi | Microsoft Docs
ms.custom: ''
ms.date: 01/18/2017
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
ms.assetid: 2799d06d-20dd-4c12-9646-554c0ea3606e
caps.latest.revision: 5
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: 6120b8fdd913b4acee2e3ee6774d770aa75b1f5a
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62992968"
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
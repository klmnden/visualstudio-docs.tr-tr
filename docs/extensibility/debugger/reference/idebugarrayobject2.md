---
title: IDebugArrayObject2 | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
helpviewer_keywords:
- IDebugArrayObject2 interface
ms.assetid: be6e504d-4ab3-4141-a61b-0953ee0e038e
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: 5cd54edc7696876bd942a4529261f7dc06885c94
ms.sourcegitcommit: 2193323efc608118e0ce6f6b2ff532f158245d56
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/25/2019
ms.locfileid: "55017948"
---
# <a name="idebugarrayobject2"></a>IDebugArrayObject2
> [!IMPORTANT]
>  Visual Studio 2015'te, bu şekilde ifade değerlendiricisi uygulama kullanım dışı bırakılmıştır. CLR ifade değerlendiricisi uygulama hakkında daha fazla bilgi için lütfen bkz [CLR ifade Değerlendiricilerini](https://github.com/Microsoft/ConcordExtensibilitySamples/wiki/CLR-Expression-Evaluators) ve [yönetilen ifade değerlendiricisi örnek](https://github.com/Microsoft/ConcordExtensibilitySamples/wiki/Managed-Expression-Evaluator-Sample).  
  
 Yönetilen dizi nesnesini temsil eder ve bir ifade değerlendiricisi dizisi için temel dizin (alt sınırı) belirlemek için (EE) sağlar.  
  
## <a name="syntax"></a>Sözdizimi  
  
```  
IDebugArrayObject2 : IDebugArrayObject  
```  
  
## <a name="notes-for-implementers"></a>Uygulayanlar için Notlar  
 Bu yönetilen hata ayıklama altyapısı (DE) tarafından uygulanır.  
  
## <a name="methods"></a>Yöntemler  
 Yöntemlere ek olarak [IDebugArrayObject](../../../extensibility/debugger/reference/idebugarrayobject.md) arabirimi bu arabirim, aşağıdaki yöntemleri uygular:  
  
|Yöntem|Açıklama|  
|------------|-----------------|  
|[GetBaseIndices](../../../extensibility/debugger/reference/idebugarrayobject2-getbaseindices.md)|Dizideki boyutların sayısı verilen her dizin için temel dizin (alt sınırı) alır.|  
|[HasBaseIndices](../../../extensibility/debugger/reference/idebugarrayobject2-hasbaseindices.md)|Dizi tanımlı temel dizin (alt sınırı) olup olmadığını belirler.|  
  
## <a name="remarks"></a>Açıklamalar  
 İfade değerlendiricisi, ayrıştırma ağacı içindeki yönetilen diziler temsil etmek için bu arabirimi kullanır.  
  
## <a name="requirements"></a>Gereksinimler  
 Üst bilgi: Ee.h  
  
 Ad alanı: Microsoft.VisualStudio.Debugger.Interop  
  
 Derleme: Microsoft.VisualStudio.Debugger.Interop.dll
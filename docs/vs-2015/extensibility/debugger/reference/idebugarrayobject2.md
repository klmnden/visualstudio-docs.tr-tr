---
title: IDebugArrayObject2 | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-sdk
ms.topic: reference
helpviewer_keywords:
- IDebugArrayObject2 interface
ms.assetid: be6e504d-4ab3-4141-a61b-0953ee0e038e
caps.latest.revision: 11
ms.author: gregvanl
manager: jillfra
ms.openlocfilehash: 7de86c1560f511f684daa7f6029a54865460c62e
ms.sourcegitcommit: 8b538eea125241e9d6d8b7297b72a66faa9a4a47
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54765696"
---
# <a name="idebugarrayobject2"></a>IDebugArrayObject2
[!INCLUDE[vs2017banner](../../../includes/vs2017banner.md)]

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

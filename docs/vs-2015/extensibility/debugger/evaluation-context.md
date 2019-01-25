---
title: Değerlendirme bağlamı | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-sdk
ms.topic: conceptual
helpviewer_keywords:
- debugging [Debugging SDK], expression evaluation
- expression evaluation, context
ms.assetid: 008a20c7-1b27-4013-bf96-d6a3f510da02
caps.latest.revision: 12
ms.author: gregvanl
manager: jillfra
ms.openlocfilehash: 28b36cfcb66dc4345843f9bcb1e7c7461b0fc6bf
ms.sourcegitcommit: 8b538eea125241e9d6d8b7297b72a66faa9a4a47
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54793535"
---
# <a name="evaluation-context"></a>Değerlendirme Bağlamı
[!INCLUDE[vs2017banner](../../includes/vs2017banner.md)]

> [!IMPORTANT]
>  Visual Studio 2015'te, bu şekilde ifade değerlendiricisi uygulama kullanım dışı bırakılmıştır. CLR ifade değerlendiricisi uygulama hakkında daha fazla bilgi için lütfen bkz [CLR ifade Değerlendiricilerini](https://github.com/Microsoft/ConcordExtensibilitySamples/wiki/CLR-Expression-Evaluators) ve [yönetilen ifade değerlendiricisi örnek](https://github.com/Microsoft/ConcordExtensibilitySamples/wiki/Managed-Expression-Evaluator-Sample).  
  
 Hata ayıklama altyapısı (DE) ifade değerlendiricisi (EE) çağırdığında, üç bağımsız değişken geçirilen [EvaluateSync](../../extensibility/debugger/reference/idebugparsedexpression-evaluatesync.md) bulma ve değerlendirme sembolleri bağlam aşağıdaki tabloda gösterildiği gibi belirleyin.  
  
## <a name="arguments"></a>Arguments  
  
|Bağımsız Değişken|Açıklama|  
|--------------|-----------------|  
|`pSymbolProvider`|Bir [IDebugSymbolProvider](../../extensibility/debugger/reference/idebugsymbolprovider.md) sembolü tanımlamak için kullanılacak sembol işleyici (SH) belirten arabirimi.|  
|`pAddress`|Bir [IDebugAddress](../../extensibility/debugger/reference/idebugaddress.md) arabirimi geçerli yürütme noktasını belirtir. Yürütülen kod içeren yöntemi bulmak için kullanılabilir.|  
|`pBinder`|Bir [IDebugBinder](../../extensibility/debugger/reference/idebugbinder.md) adı verilen bir simgenin türünü ve değerini bulmak için kullanılan arabirim.|  
  
 `IDebugParsedExpression::EvaluateSync` döndürür bir [IDebugProperty2](../../extensibility/debugger/reference/idebugproperty2.md) sonuç değerini ve türünü temsil eden arabirim.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Anahtar ifade değerlendiricisi arabirimleri](../../extensibility/debugger/key-expression-evaluator-interfaces.md)   
 [Yerel öğeleri görüntüleme](../../extensibility/debugger/displaying-locals.md)   
 [EvaluateSync](../../extensibility/debugger/reference/idebugparsedexpression-evaluatesync.md)   
 [IDebugProperty2](../../extensibility/debugger/reference/idebugproperty2.md)   
 [IDebugSymbolProvider](../../extensibility/debugger/reference/idebugsymbolprovider.md)   
 [IDebugAddress](../../extensibility/debugger/reference/idebugaddress.md)   
 [IDebugBinder](../../extensibility/debugger/reference/idebugbinder.md)

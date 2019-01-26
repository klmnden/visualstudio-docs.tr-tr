---
title: IDebugParsedExpression | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
f1_keywords:
- IDebugParsedExpression
helpviewer_keywords:
- IDebugParsedExpression interface
ms.assetid: be6486ed-b070-4898-95b1-58581bcb4447
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: 13f2477223f7cf1cf312d1b5ac1cadbff818b80b
ms.sourcegitcommit: 2193323efc608118e0ce6f6b2ff532f158245d56
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/25/2019
ms.locfileid: "54971942"
---
# <a name="idebugparsedexpression"></a>IDebugParsedExpression
> [!IMPORTANT]
>  Visual Studio 2015'te, bu şekilde ifade değerlendiricisi uygulama kullanım dışı bırakılmıştır. CLR ifade değerlendiricisi uygulama hakkında daha fazla bilgi için lütfen bkz [CLR ifade Değerlendiricilerini](https://github.com/Microsoft/ConcordExtensibilitySamples/wiki/CLR-Expression-Evaluators) ve [yönetilen ifade değerlendiricisi örnek](https://github.com/Microsoft/ConcordExtensibilitySamples/wiki/Managed-Expression-Evaluator-Sample).  
  
 Bu arabirim, değerlendirilecek hazır ayrıştırılmış bir ifade temsil eder.  
  
## <a name="syntax"></a>Sözdizimi  
  
```  
IDebugParsedExpression : IUnknown  
```  
  
## <a name="notes-for-implementers"></a>Uygulayanlar için Notlar  
 İfade değerlendiricisi, değerlendirme için hazır ayrıştırılmış bir ifade temsil etmek için bu arabirimi uygular.  
  
## <a name="notes-for-callers"></a>Arayanlar İçin Notlar  
 Bir çağrı [ayrıştırma](../../../extensibility/debugger/reference/idebugexpressionevaluator-parse.md) bu arabirimi döndürür.  
  
## <a name="methods-in-vtable-order"></a>Vtable sırayla yöntemleri  
 Yöntemini aşağıdaki tabloda gösterilmektedir `IDebugParsedExpression`.  
  
|Yöntem|Açıklama|  
|------------|-----------------|  
|[EvaluateSync](../../../extensibility/debugger/reference/idebugparsedexpression-evaluatesync.md)|Ayrıştırılmış ifadeyi değerlendirir.|  
  
## <a name="remarks"></a>Açıklamalar  
 Arayan ifadeyi değerlendirmek hazır olduğunda, çağrı [EvaluateSync](../../../extensibility/debugger/reference/idebugparsedexpression-evaluatesync.md) döndürmek için bir [IDebugProperty2](../../../extensibility/debugger/reference/idebugproperty2.md) , değerlendirme sonucunu içerir. Bu iki bölümden yaklaşımı değerlendirirken, sağlayan sonra birden çok kez değerlendirilecek ayrıştırılmış ifade ayrıştırma, zaman alıcı ifade ayrıştırma işleminin atlayarak değerlendirme için.  
  
## <a name="requirements"></a>Gereksinimler  
 Üstbilgi: ee.h  
  
 Ad alanı: Microsoft.VisualStudio.Debugger.Interop  
  
 Derleme: Microsoft.VisualStudio.Debugger.Interop.dll  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Ayrıştırma](../../../extensibility/debugger/reference/idebugexpressionevaluator-parse.md)   
 [EvaluateSync](../../../extensibility/debugger/reference/idebugparsedexpression-evaluatesync.md)   
 [IDebugProperty2](../../../extensibility/debugger/reference/idebugproperty2.md)
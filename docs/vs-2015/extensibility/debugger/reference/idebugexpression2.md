---
title: IDebugExpression2 | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-sdk
ms.topic: reference
f1_keywords:
- IDebugExpression2
helpviewer_keywords:
- IDebugExpression2 interface
ms.assetid: f5e4b124-1e30-47c8-a511-80084a02dba5
caps.latest.revision: 15
ms.author: gregvanl
manager: jillfra
ms.openlocfilehash: ec8b26f422ca39b771a47f8eb60ee862d7d388f9
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62568375"
---
# <a name="idebugexpression2"></a>IDebugExpression2
[!INCLUDE[vs2017banner](../../../includes/vs2017banner.md)]

Bu arabirim bağlama ve değerlendirmek için ayrıştırılmış ifade hazır temsil eder.  
  
## <a name="syntax"></a>Sözdizimi  
  
```  
IDebugExpression2 : IUnknown  
```  
  
## <a name="notes-for-implementers"></a>Uygulayanlar için Notlar  
 Hata ayıklama altyapısı (DE) uyumluluğunun değerlendirilebilmesi hazır bir ayrıştırılmış ifadesini göstermek için bu arabirimi uygular.  
  
## <a name="notes-for-callers"></a>Arayanlar İçin Notlar  
 Bir çağrı [ParseText](../../../extensibility/debugger/reference/idebugexpressioncontext2-parsetext.md) bu arabirimi döndürür. [GetExpressionContext](../../../extensibility/debugger/reference/idebugstackframe2-getexpressioncontext.md) döndürür [IDebugExpressionContext2](../../../extensibility/debugger/reference/idebugexpressioncontext2.md) arabirimi. Bu arabirimler yalnızca hata ayıklanan programa duraklatıldı ve bir yığın çerçevesini kullanılabilir erişilebilir.  
  
## <a name="methods-in-vtable-order"></a>Vtable sırayla yöntemleri  
 Aşağıdaki tabloda yöntemlerini gösterilmektedir `IDebugExpression2`.  
  
|Yöntem|Açıklama|  
|------------|-----------------|  
|[EvaluateAsync](../../../extensibility/debugger/reference/idebugexpression2-evaluateasync.md)|Bu ifade zaman uyumsuz olarak değerlendirilir.|  
|[Abort](../../../extensibility/debugger/reference/idebugexpression2-abort.md)|Zaman uyumsuz bir ifade değerlendirme sona erer.|  
|[EvaluateSync](../../../extensibility/debugger/reference/idebugexpression2-evaluatesync.md)|Bu ifade zaman uyumlu olarak değerlendirilir.|  
  
## <a name="remarks"></a>Açıklamalar  
 Bir program durdu, oturum hata ayıklama Yöneticisi (SDM) bir yığın çerçevesi bir çağrı ile DE elde [EnumFrameInfo](../../../extensibility/debugger/reference/idebugthread2-enumframeinfo.md). SDM sonra çağıran [GetExpressionContext](../../../extensibility/debugger/reference/idebugstackframe2-getexpressioncontext.md) almak için [IDebugExpressionContext2](../../../extensibility/debugger/reference/idebugexpressioncontext2.md) arabirimi. Bu çağrı takip [ParseText](../../../extensibility/debugger/reference/idebugexpressioncontext2-parsetext.md) oluşturmak için `IDebugExpression2` değerlendirilecek hazır ayrıştırılmış ifadeyi temsil eden arabirim.  
  
 SDM ya da çağırır [EvaluateSync](../../../extensibility/debugger/reference/idebugexpression2-evaluatesync.md) veya [EvaluateAsync](../../../extensibility/debugger/reference/idebugexpression2-evaluateasync.md) gerçekten ifadeyi değerlendirir ve bir değer üretir.  
  
 Uygulaması içinde `IDebugExpressionContext2::ParseText`, DE COM'ın kullandığı `CoCreateInstance` ifade değerlendiricisi oluşturmak ve almak için işlevi bir [IDebugExpressionEvaluator](../../../extensibility/debugger/reference/idebugexpressionevaluator.md) arabirimi (örnekte bakın `IDebugExpressionEvaluator` arabirimi). Daha sonra DE çağırır [ayrıştırma](../../../extensibility/debugger/reference/idebugexpressionevaluator-parse.md) almak için bir [IDebugParsedExpression](../../../extensibility/debugger/reference/idebugparsedexpression.md) arabirimi. Bu arabirim uygulamasında kullanılan `IDebugExpression2::EvaluateSync` ve `IDebugExpression2::EvaluateAsync` değerlendirmeyi gerçekleştirmek için.  
  
## <a name="requirements"></a>Gereksinimler  
 Üstbilgi: msdbg.h  
  
 Ad alanı: Microsoft.VisualStudio.Debugger.Interop  
  
 Derleme: Microsoft.VisualStudio.Debugger.Interop.dll  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Temel arabirimler](../../../extensibility/debugger/reference/core-interfaces.md)   
 [GetExpression](../../../extensibility/debugger/reference/idebugexpressionevaluationcompleteevent2-getexpression.md)

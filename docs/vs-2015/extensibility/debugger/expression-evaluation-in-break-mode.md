---
title: Kesme modunda ifade değerlendirme | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-sdk
ms.topic: conceptual
helpviewer_keywords:
- break mode, expression evaluation
- debugging [Debugging SDK], expression evaluation
- expression evaluation, break mode
ms.assetid: 34fe5b58-15d5-4387-a266-72120f90a4b6
caps.latest.revision: 11
ms.author: gregvanl
manager: jillfra
ms.openlocfilehash: 362e50e20519c358564d13ba169f706fe384ca5c
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "68152754"
---
# <a name="expression-evaluation-in-break-mode"></a>Kesme Modunda İfade Değerlendirme
[!INCLUDE[vs2017banner](../../includes/vs2017banner.md)]

Hata ayıklayıcı kesme modundayken ve ifade değerlendirmesi gerçekleştirin gerekir oluşan süreci açıklanmaktadır.  
  
## <a name="expression-evaluation-process"></a>İfade değerlendirme işlemi  
 Bir ifadenin değerlendirilmesi ilgili temel adımlar şunlardır:  
  
1. Oturum hata ayıklama Yöneticisi (SDM) çağıran [IDebugStackFrame2::GetExpressionContext](../../extensibility/debugger/reference/idebugstackframe2-getexpressioncontext.md) bir ifade bağlam arabirimi almak için [IDebugExpressionContext2](../../extensibility/debugger/reference/idebugexpressioncontext2.md).  
  
2. SDM sonra çağıran [IDebugExpressionContext2::ParseText](../../extensibility/debugger/reference/idebugexpressioncontext2-parsetext.md) ayrıştırılacak dize ile.  
  
3. Hatanın nedenini ParseText S_OK döndürmezse döndürülür.  
  
     -Aksi takdirde-  
  
     ParseText S_OK döndürürse SDM sonra ya da çağırabilir [IDebugExpression2::EvaluateSync](../../extensibility/debugger/reference/idebugexpression2-evaluatesync.md) veya [IDebugExpression2::EvaluateAsync](../../extensibility/debugger/reference/idebugexpression2-evaluateasync.md) ayrıştırılmış ifadedeki son değer elde edilir.  
  
    - Kullanarak söz konusu olduğunda `IDebugExpression2::EvaluateSync`, belirtilen geri arama arabirimi değerlendirmeye devam eden işlemi iletişim kurmak için kullanılır. Son değeri döndürülür bir [IDebugProperty2](../../extensibility/debugger/reference/idebugproperty2.md) arabirimi.  
  
    - Kullanarak söz konusu olduğunda `IDebugExpression2::EvaluateAsync`, belirtilen geri arama arabirimi değerlendirmeye devam eden işlemi iletişim kurmak için kullanılır. Değerlendirme tamamlandıktan sonra EvaluateAsync gönderen bir [IDebugExpressionEvaluationCompleteEvent2](../../extensibility/debugger/reference/idebugexpressionevaluationcompleteevent2.md) arabirimi aracılığıyla geri çağırma. Bu olay arabirimi ile son değeri ile alınabilir [GetResult](../../extensibility/debugger/reference/idebugexpressionevaluationcompleteevent2-getresult.md).  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Hata Ayıklayıcısı Olaylarını Çağırma](../../extensibility/debugger/calling-debugger-events.md)

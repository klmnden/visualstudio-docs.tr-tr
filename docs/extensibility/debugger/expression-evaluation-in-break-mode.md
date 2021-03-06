---
title: Kesme modunda ifade değerlendirme | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
helpviewer_keywords:
- break mode, expression evaluation
- debugging [Debugging SDK], expression evaluation
- expression evaluation, break mode
ms.assetid: 34fe5b58-15d5-4387-a266-72120f90a4b6
author: madskristensen
ms.author: madsk
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: af231333981697705ba58fe505b0bf55304b8287
ms.sourcegitcommit: 40d612240dc5bea418cd27fdacdf85ea177e2df3
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/29/2019
ms.locfileid: "66353835"
---
# <a name="expression-evaluation-in-break-mode"></a>Kesme modunda ifade değerlendirme
Aşağıdaki bölümde hata ayıklayıcı kesme modundayken ve ifade değerlendirmesi gerçekleştirin gerekir oluşan işlemi açıklanmaktadır.

## <a name="expression-evaluation-process"></a>İfade değerlendirme işlemi
 Bir ifadenin değerlendirilmesi ilgili temel adımlar şunlardır:

1. Oturum hata ayıklama Yöneticisi (SDM) çağıran [IDebugStackFrame2::GetExpressionContext](../../extensibility/debugger/reference/idebugstackframe2-getexpressioncontext.md) bir ifade bağlam arabirimi almak için [IDebugExpressionContext2](../../extensibility/debugger/reference/idebugexpressioncontext2.md).

2. SDM sonra çağıran [IDebugExpressionContext2::ParseText](../../extensibility/debugger/reference/idebugexpressioncontext2-parsetext.md) ayrıştırılacak dize ile.

3. Hatanın nedenini ParseText S_OK döndürmezse döndürülür.

     -Aksi takdirde-

     ParseText S_OK döndürürse SDM sonra ya da çağırabilir [IDebugExpression2::EvaluateSync](../../extensibility/debugger/reference/idebugexpression2-evaluatesync.md) veya [IDebugExpression2::EvaluateAsync](../../extensibility/debugger/reference/idebugexpression2-evaluateasync.md) ayrıştırılmış ifadedeki son değer alınamıyor.

    - Kullanırken `IDebugExpression2::EvaluateSync`, değerlendirme devam eden işlemi belirtilen geri arama arabirimini iletişim kurar. Son değeri döndürülür bir [IDebugProperty2](../../extensibility/debugger/reference/idebugproperty2.md) arabirimi.

    - Kullanırken `IDebugExpression2::EvaluateAsync`, değerlendirme devam eden işlemi belirtilen geri arama arabirimini iletişim kurar. Değerlendirme tamamlandıktan sonra EvaluateAsync gönderen bir [IDebugExpressionEvaluationCompleteEvent2](../../extensibility/debugger/reference/idebugexpressionevaluationcompleteevent2.md) arabirimi aracılığıyla geri çağırma. Bu olay arabirimi ile son değeri sonuçları ile [GetResult](../../extensibility/debugger/reference/idebugexpressionevaluationcompleteevent2-getresult.md).

## <a name="see-also"></a>Ayrıca bkz.
- [Hata ayıklayıcı olayları çağırma](../../extensibility/debugger/calling-debugger-events.md)
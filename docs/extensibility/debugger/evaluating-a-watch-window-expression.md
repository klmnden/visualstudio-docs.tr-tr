---
title: Bir Gözcü penceresi ifadesini değerlendirme | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
helpviewer_keywords:
- Watch window expressions
- Watch window, expressions
- expression evaluation, Watch window expressions
ms.assetid: b07e72c7-60d3-4b30-8e3f-6db83454c348
author: madskristensen
ms.author: madsk
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: 6fe575cf0db9f6f1c2dd15da96d3d0a17648aee4
ms.sourcegitcommit: 40d612240dc5bea418cd27fdacdf85ea177e2df3
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/29/2019
ms.locfileid: "66315511"
---
# <a name="evaluate-a-watch-window-expression"></a>Gözcü penceresi ifadesini değerlendirme
> [!IMPORTANT]
> Visual Studio 2015'te, bu şekilde ifade değerlendiricisi uygulama kullanım dışı bırakılmıştır. CLR ifade değerlendiricisi uygulama hakkında daha fazla bilgi için bkz: [CLR ifade değerlendiricilerini](https://github.com/Microsoft/ConcordExtensibilitySamples/wiki/CLR-Expression-Evaluators) ve [yönetilen ifade değerlendiricisi örnek](https://github.com/Microsoft/ConcordExtensibilitySamples/wiki/Managed-Expression-Evaluator-Sample).

 Yürütme durakladığında Visual Studio hata ayıklama altyapısı kendi izleme listesindeki her bir ifadenin geçerli değerini belirlemek için (DE) çağırır. DE (EE) ifade değerlendiricisi'ni kullanarak her bir ifade değerlendirir ve Visual Studio görüntüler değeriyle **Watch** penceresi.

 Bir izleme listesi ifade nasıl değerlendirilir genel bir bakış aşağıdadır:

1. Visual Studio DE'ın çağıran [GetExpressionContext](../../extensibility/debugger/reference/idebugstackframe2-getexpressioncontext.md) ifadeleri değerlendirmek için kullanılan bir ifade içeriği almak için.

2. İzleme listesi içinde her bir ifade için Visual Studio çağırır [ParseText](../../extensibility/debugger/reference/idebugexpressioncontext2-parsetext.md) ifade metin ayrıştırılmış bir ifadeye dönüştürmek için.

3. `IDebugExpressionContext2::ParseText` çağrıları [ayrıştırma](../../extensibility/debugger/reference/idebugexpressionevaluator-parse.md) üretebilir ve metin ayrıştırma asıl işi yapmak için bir [IDebugParsedExpression](../../extensibility/debugger/reference/idebugparsedexpression.md) nesne.

4. `IDebugExpressionContext2::ParseText` oluşturur bir [IDebugExpression2](../../extensibility/debugger/reference/idebugexpression2.md) nesne ve puts `IDebugParsedExpression` içine bir nesne. Bu ben`DebugExpression2` Visual Studio'ya döndürülen nesne.

5. Visual Studio çağrıları [EvaluateSync](../../extensibility/debugger/reference/idebugexpression2-evaluatesync.md) ayrıştırılmış ifade değerlendirilemiyor.

6. `IDebugExpression2::EvaluateSync` Çağrı başarılı [EvaluateSync](../../extensibility/debugger/reference/idebugparsedexpression-evaluatesync.md) gerçek değerlendirmesi yapmak ve üretmek için bir [IDebugProperty2](../../extensibility/debugger/reference/idebugproperty2.md) Visual Studio'ya döndürülen nesne.

7. Visual Studio çağrıları [GetPropertyInfo](../../extensibility/debugger/reference/idebugproperty2-getpropertyinfo.md) ardından izleme listesinde görüntülenen ifade değeri elde edilir.

## <a name="parse-then-evaluate"></a>Ayrıştırma sonra değerlendir
 Karmaşık bir ifade ayrıştırma değerlendirme daha çok daha uzun sürebilir olduğundan bir ifade değerlendirme işlemi iki adımlamayla ayrılmıştır: ifade (1) ayrıştırma ve 2) ayrıştırılmış ifadeyi değerlendirir. Bu şekilde, birden çok kez değerlendirme oluşabilir, ancak yalnızca bir kez ayrıştırılacak ifade gerekiyor. Ara ayrıştırılmış ifade içinde EE döndürüldüğü bir [IDebugParsedExpression](../../extensibility/debugger/reference/idebugparsedexpression.md) sırayla kapsüllenmiş ve DE döndürülen nesne bir [IDebugExpression2](../../extensibility/debugger/reference/idebugexpression2.md) nesne. `IDebugExpression` Nesne için tüm değerlendirmesi erteler `IDebugParsedExpression` nesne.

> [!NOTE]
> Bir EE rağmen bu Visual Studio varsayar, bu iki adımlı işleme uyması gerekli değildir; EE ayrıştırabilir ve aynı adımda değerlendirme zaman [EvaluateSync](../../extensibility/debugger/reference/idebugparsedexpression-evaluatesync.md) çağrılır (MyCEE örnek, örneğin işleyişi budur). Dilinizi karmaşık ifadeleri biçimlendiriyorsa ayrıştırma adım değerlendirme adımdan ayırmak isteyebilirsiniz. Çoğu ifadeleri izlerken bu Visual Studio hata ayıklayıcısında performans artırabilir gösterilir.

## <a name="in-this-section"></a>Bu bölümde
 [Örnek İfade değerlendirme uygulaması](../../extensibility/debugger/sample-implementation-of-expression-evaluation.md) MyCEE örnek ifade değerlendirme işlemi için kullanır.

 [Bir Gözcü ifadesini değerlendirme](../../extensibility/debugger/evaluating-a-watch-expression.md) bir başarılı ifade ayrıştırma sonra ne olacağını açıklar.

## <a name="related-sections"></a>İlgili bölümler
 [Değerlendirme bağlamı](../../extensibility/debugger/evaluation-context.md) ifade değerlendiricisi (EE) hata ayıklama altyapısı (DE) çağırdığında, geçirilen bağımsız değişkenler sağlar.

## <a name="see-also"></a>Ayrıca bkz.
 [Bir CLR ifade değerlendiricisi yazma](../../extensibility/debugger/writing-a-common-language-runtime-expression-evaluator.md)
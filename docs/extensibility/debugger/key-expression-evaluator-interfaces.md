---
title: Anahtar ifade değerlendiricisi arabirimleri | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
helpviewer_keywords:
- debugging [Debugging SDK], expression evaluation
- expression evaluation, interfaces
ms.assetid: 1cac9aa3-0867-4e12-a16e-1e90abbc0fb6
author: madskristensen
ms.author: madsk
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: 4f633d1b3bba5fbd5ecbfb44051740a0bc4bb09f
ms.sourcegitcommit: 40d612240dc5bea418cd27fdacdf85ea177e2df3
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/29/2019
ms.locfileid: "66344225"
---
# <a name="key-expression-evaluator-interfaces"></a>Anahtar ifade değerlendiricisi arabirimleri
> [!IMPORTANT]
> Visual Studio 2015'te, bu şekilde ifade değerlendiricisi uygulama kullanım dışı bırakılmıştır. CLR ifade değerlendiricisi uygulama hakkında daha fazla bilgi için lütfen bkz [CLR ifade değerlendiricilerini](https://github.com/Microsoft/ConcordExtensibilitySamples/wiki/CLR-Expression-Evaluators) ve [yönetilen ifade değerlendiricisi örnek](https://github.com/Microsoft/ConcordExtensibilitySamples/wiki/Managed-Expression-Evaluator-Sample).

 Değerlendirme bağlamı birlikte ifade değerlendiricisi (EE) yazarken aşağıdaki arabirimleriyle ilgili bilgi sahibi olması gerekir.

## <a name="interface-descriptions"></a>Arabirimi açıklamaları

- [IDebugAddress](../../extensibility/debugger/reference/idebugaddress.md)

     Tek bir yöntemi, [GetAddress](../../extensibility/debugger/reference/idebugaddress-getaddress.md), geçerli yürütme noktasını temsil eder, veri yapısını alır. Hata ayıklama altyapısı (DE) geçirir üç bağımsız değişken, bu veri yapısını biridir [EvaluateSync](../../extensibility/debugger/reference/idebugparsedexpression-evaluatesync.md) bir ifadeyi değerlendirmek için yöntemi. Bu arabirim, genellikle sembol sağlayıcısı tarafından uygulanır.

- [IDebugBinder](../../extensibility/debugger/reference/idebugbinder.md)

     Sahip [bağlama](../../extensibility/debugger/reference/idebugbinder-bind.md) yöntemi bir simge geçerli değerini içeren bellek alanını alır. Tarafından temsil edilen her iki içeren yöntem, verilen bir [IDebugObject](../../extensibility/debugger/reference/idebugobject.md) nesnesi ve tarafından temsil edilen simgenin kendisine bir [IDebugField](../../extensibility/debugger/reference/idebugfield.md) nesnesi `IDebugBinder::Bind` sembolün değerini döndürür. `IDebugBinder` Genel DE uygulanır.

- [IDebugField](../../extensibility/debugger/reference/idebugfield.md)

     Basit veri türünü temsil eder. Diziler ve yöntemler gibi daha karmaşık türler kullanmak türetilmiş [IDebugArrayField](../../extensibility/debugger/reference/idebugarrayfield.md) ve [IDebugMethodField](../../extensibility/debugger/reference/idebugmethodfield.md) arabirimleri, sırasıyla. [IDebugContainerField](../../extensibility/debugger/reference/idebugcontainerfield.md) yöntemleri veya sınıfları gibi diğer semboller içeren sembolleri temsil eden başka bir önemli türetilmiş arabirimidir. `IDebugField` Arabirimi (ve CIM'in) sembol sağlayıcısı tarafından uygulanan genellikle.

     Bir `IDebugField` nesne bir simgenin türünü ve adını bulmak için kullanılan ve, birlikte olabilir bir [IDebugBinder](../../extensibility/debugger/reference/idebugbinder.md) nesne, değerini bulmak için kullanılabilir.

- [IDebugObject](../../extensibility/debugger/reference/idebugobject.md)

     Gerçek bitlik bir simgenin çalışma zamanı değerini temsil eder. [Bağlama](../../extensibility/debugger/reference/idebugbinder-bind.md) götüren bir [IDebugField](../../extensibility/debugger/reference/idebugfield.md) temsil eden bir simge ve döndüren bir nesne bir [IDebugObject](../../extensibility/debugger/reference/idebugobject.md) nesne. [GetValue](../../extensibility/debugger/reference/idebugobject-getvalue.md) yöntemi, bir bellek arabellek sembolün değerini döndürür. Bir DE genellikle bellekte bir özelliğin değerini temsil etmek için bu arabirimi uygular.

- [IDebugExpressionEvaluator](../../extensibility/debugger/reference/idebugexpressionevaluator.md)

     Bu arabirim, ifade değerlendiricisi temsil eder. Anahtar yöntemi [ayrıştırma](../../extensibility/debugger/reference/idebugexpressionevaluator-parse.md), döndüren bir [IDebugParsedExpression](../../extensibility/debugger/reference/idebugparsedexpression.md) arabirimi.

- [IDebugParsedExpression](../../extensibility/debugger/reference/idebugparsedexpression.md)

     Bu arabirim, değerlendirilecek hazır ayrıştırılmış bir ifade temsil eder. Anahtar yöntemi [EvaluateSync](../../extensibility/debugger/reference/idebugparsedexpression-evaluatesync.md) IDebugProperty2 bir ifadenin türü ve değeri temsil eden döndürür.

- [IDebugProperty2](../../extensibility/debugger/reference/idebugproperty2.md)

     Bu arabirim, değer ve türünü temsil eder ve bir ifade değerlendirme sonucu.

## <a name="see-also"></a>Ayrıca bkz.
- [Değerlendirme bağlamı](../../extensibility/debugger/evaluation-context.md)
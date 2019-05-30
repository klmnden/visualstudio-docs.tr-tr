---
title: İfade değerlendiricisi uygulama stratejisi | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
helpviewer_keywords:
- expression evaluation, implementation strategy
- debug engines, implementation strategies
ms.assetid: 1bccaeb3-8109-4128-ae79-16fd8fbbaaa2
author: madskristensen
ms.author: madsk
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: ee0842f8375faeca7e715d4b20c73ca13598dbc3
ms.sourcegitcommit: 40d612240dc5bea418cd27fdacdf85ea177e2df3
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/29/2019
ms.locfileid: "66353748"
---
# <a name="expression-evaluator-implementation-strategy"></a>İfade değerlendiricisi uygulama stratejisi
> [!IMPORTANT]
> Visual Studio 2015'te, bu şekilde ifade değerlendiricisi uygulama kullanım dışı bırakılmıştır. CLR ifade değerlendiricisi uygulama hakkında daha fazla bilgi için bkz: [CLR ifade değerlendiricilerini](https://github.com/Microsoft/ConcordExtensibilitySamples/wiki/CLR-Expression-Evaluators) ve [yönetilen ifade değerlendiricisi örnek](https://github.com/Microsoft/ConcordExtensibilitySamples/wiki/Managed-Expression-Evaluator-Sample).

 İfade değerlendiricisi (EE) hızlı bir şekilde oluşturmak için bir yaklaşım ise ilk yerel değişkenlerle göstermek için gerekli en düşük kod uygulamak için **Yereller** penceresi. Fark yararlıdır her satırında **Yereller** penceresi adı, türü ve yerel bir değişken değerini görüntüler ve üç tarafından temsil edilen bir [IDebugProperty2](../../extensibility/debugger/reference/idebugproperty2.md) nesne. Adı, türü ve bir yerel değişken değeri öğesinden alınan bir `IDebugProperty2` çağırarak kendi [GetPropertyInfo](../../extensibility/debugger/reference/idebugproperty2-getpropertyinfo.md) yöntemi. Yerel değişkenlerle görüntüleme hakkında daha fazla bilgi için **Yereller** penceresinde görmek [görüntüleme Yereller](../../extensibility/debugger/displaying-locals.md).

## <a name="discussion"></a>Tartışma
 Uygulanmasıyla bir olası uygulama dizisini başlatır [IDebugExpressionEvaluator](../../extensibility/debugger/reference/idebugexpressionevaluator.md). [Ayrıştırma](../../extensibility/debugger/reference/idebugexpressionevaluator-parse.md) ve [GetMethodProperty](../../extensibility/debugger/reference/idebugexpressionevaluator-getmethodproperty.md) yöntemleri uygulanan, yerel öğeler görüntülenecek. Çağırma `IDebugExpressionEvaluator::GetMethodProperty` döndürür bir `IDebugProperty2` bir yöntemi temsil eden nesne: diğer bir deyişle, bir [IDebugMethodField](../../extensibility/debugger/reference/idebugmethodfield.md) nesne. İçinde kendilerini yöntemleri görüntülenmez **Yereller** penceresi.

 [EnumChildren](../../extensibility/debugger/reference/idebugproperty2-enumchildren.md) yönteminin uygulanmasını sonraki. Hata ayıklama altyapısı (DE) geçirerek yerel değişkenleri ve bağımsız değişkenler listesini almak için bu yöntemi çağıran `IDebugProperty2::EnumChildren` bir `guidFilter` bağımsız değişkeni `guidFilterLocalsPlusArgs`. `IDebugProperty2::EnumChildren` çağrıları [EnumArguments](../../extensibility/debugger/reference/idebugmethodfield-enumarguments.md) ve [EnumLocals](../../extensibility/debugger/reference/idebugmethodfield-enumlocals.md), tek bir sabit listesi sonuçları birleştirme. Bkz: [görüntüleme Yereller](../../extensibility/debugger/displaying-locals.md) daha fazla ayrıntı için.

## <a name="see-also"></a>Ayrıca bkz.
- [İfade değerlendiricisi uygulama](../../extensibility/debugger/implementing-an-expression-evaluator.md)
- [Görüntü yerel öğeler](../../extensibility/debugger/displaying-locals.md)
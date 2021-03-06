---
title: Değerlendirme bağlamı | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
helpviewer_keywords:
- debugging [Debugging SDK], expression evaluation
- expression evaluation, context
ms.assetid: 008a20c7-1b27-4013-bf96-d6a3f510da02
author: madskristensen
ms.author: madsk
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: b6a3d74c26b6ca94e0a4052df4810e407313a6cd
ms.sourcegitcommit: 40d612240dc5bea418cd27fdacdf85ea177e2df3
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/29/2019
ms.locfileid: "66315497"
---
# <a name="evaluation-context"></a>Değerlendirme bağlamı
> [!IMPORTANT]
> Visual Studio 2015'te, bu şekilde ifade değerlendiricisi uygulama kullanım dışı bırakılmıştır. CLR ifade değerlendiricisi uygulama hakkında daha fazla bilgi için bkz: [CLR ifade değerlendiricilerini](https://github.com/Microsoft/ConcordExtensibilitySamples/wiki/CLR-Expression-Evaluators) ve [yönetilen ifade değerlendiricisi örnek](https://github.com/Microsoft/ConcordExtensibilitySamples/wiki/Managed-Expression-Evaluator-Sample).

 Hata ayıklama altyapısı (DE) (EE) üç bağımsız değişken ifade değerlendiricisi, çağırdığında geçirilir [EvaluateSync](../../extensibility/debugger/reference/idebugparsedexpression-evaluatesync.md) bulma ve değerlendirme sembolleri bağlam aşağıdaki tabloda gösterildiği gibi belirleyin.

## <a name="arguments"></a>Arguments

|Bağımsız Değişken|Açıklama|
|--------------|-----------------|
|`pSymbolProvider`|Bir [IDebugSymbolProvider](../../extensibility/debugger/reference/idebugsymbolprovider.md) sembolü tanımlamak için kullanılacak sembol işleyici (SH) belirten arabirimi.|
|`pAddress`|Bir [IDebugAddress](../../extensibility/debugger/reference/idebugaddress.md) arabirimi geçerli yürütme noktasını belirtir. Bu arabirim, yürütülen kod içeren yöntemi bulur.|
|`pBinder`|Bir [IDebugBinder](../../extensibility/debugger/reference/idebugbinder.md) arabirim adı verilen bir simgenin türünü ve değerini bulur.|

 `IDebugParsedExpression::EvaluateSync` döndürür bir [IDebugProperty2](../../extensibility/debugger/reference/idebugproperty2.md) sonuç değerini ve türünü temsil eden arabirim.

## <a name="see-also"></a>Ayrıca bkz.
- [Anahtar ifade değerlendiricisi arabirimleri](../../extensibility/debugger/key-expression-evaluator-interfaces.md)
- [Yerel öğeleri görüntüleme](../../extensibility/debugger/displaying-locals.md)
- [EvaluateSync](../../extensibility/debugger/reference/idebugparsedexpression-evaluatesync.md)
- [IDebugProperty2](../../extensibility/debugger/reference/idebugproperty2.md)
- [IDebugSymbolProvider](../../extensibility/debugger/reference/idebugsymbolprovider.md)
- [IDebugAddress](../../extensibility/debugger/reference/idebugaddress.md)
- [IDebugBinder](../../extensibility/debugger/reference/idebugbinder.md)
---
title: IDebugExpressionEvaluator3 | Microsoft Docs
ms.date: 11/04/2016
ms.topic: reference
helpviewer_keywords:
- IDebugExpressionEvaluator3 interface
ms.assetid: c27c2a14-300b-4535-be22-767c83602f69
author: madskristensen
ms.author: madsk
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: 7d00f24505de763d85d4d454d6f3bde459653689
ms.sourcegitcommit: 40d612240dc5bea418cd27fdacdf85ea177e2df3
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/29/2019
ms.locfileid: "66352727"
---
# <a name="idebugexpressionevaluator3"></a>IDebugExpressionEvaluator3
> [!IMPORTANT]
> Visual Studio 2015'te, bu şekilde ifade değerlendiricisi uygulama kullanım dışı bırakılmıştır. CLR ifade değerlendiricisi uygulama hakkında daha fazla bilgi için lütfen bkz [CLR ifade Değerlendiricilerini](https://github.com/Microsoft/ConcordExtensibilitySamples/wiki/CLR-Expression-Evaluators) ve [yönetilen ifade değerlendiricisi örnek](https://github.com/Microsoft/ConcordExtensibilitySamples/wiki/Managed-Expression-Evaluator-Sample).

 İfade değerlendiricisi (EE) ile bir Gelişmiş ayrıştırıcı ağacı temsil eder.

## <a name="syntax"></a>Sözdizimi

```
IDebugExpressionEvaluator3 : IDebugExpressionEvaluator2
```

## <a name="notes-for-callers"></a>Arayanlar İçin Notlar
 Ayrıştırıcının'ın bu sürümü sembol sağlayıcısı ve değerlendirme çerçevesinin adresi geçirir.

## <a name="methods"></a>Yöntemler
 Yöntemlere ek olarak [IDebugExpressionEvaluator2](../../../extensibility/debugger/reference/idebugexpressionevaluator2.md) arabirimi bu arabirim, aşağıdaki yöntemi uygular:

|Yöntem|Açıklama|
|------------|-----------------|
|[Parse2](../../../extensibility/debugger/reference/idebugexpressionevaluator3-parse2.md)|Bir ifade dizesini verilen sembol sağlayıcısı ve değerlendirme çerçevesinin adres ayrıştırılmış bir ifade dönüştürür.|

## <a name="requirements"></a>Gereksinimler
 Üst bilgi: Ee.h

 Ad alanı: Microsoft.VisualStudio.Debugger.Interop

 Derleme: Microsoft.VisualStudio.Debugger.Interop.dll
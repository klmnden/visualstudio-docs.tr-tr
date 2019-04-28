---
title: IDebugBinder | Microsoft Docs
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- IDebugBinder
helpviewer_keywords:
- IDebugBinder interface
ms.assetid: d1f31e5b-c6e2-4e02-8959-b3e86041b29c
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: a4e5588006fb8991d5560ddfad95d41d39db7c33
ms.sourcegitcommit: 47eeeeadd84c879636e9d48747b615de69384356
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "63414054"
---
# <a name="idebugbinder"></a>IDebugBinder
> [!IMPORTANT]
> Visual Studio 2015'te, bu şekilde ifade değerlendiricisi uygulama kullanım dışı bırakılmıştır. CLR ifade değerlendiricisi uygulama hakkında daha fazla bilgi için lütfen bkz [CLR ifade Değerlendiricilerini](https://github.com/Microsoft/ConcordExtensibilitySamples/wiki/CLR-Expression-Evaluators) ve [yönetilen ifade değerlendiricisi örnek](https://github.com/Microsoft/ConcordExtensibilitySamples/wiki/Managed-Expression-Evaluator-Sample).

 Bu arabirim, genellikle bir bellek bağlamı veya sembolün geçerli değerini içeren nesne sembol sağlayıcısı tarafından döndürülen bir simge alanı bağlar.

## <a name="syntax"></a>Sözdizimi

```
IDebugBinder : IUnknown
```

## <a name="notes-for-implementers"></a>Uygulayanlar için Notlar
 Bu arabirim, ifade değerlendirme destekler ve hata ayıklama altyapısı (DE) uygulanmalıdır.

## <a name="notes-for-callers"></a>Arayanlar İçin Notlar
 Bu arabirim ifade değerlendirme aşamasında kullanılır ve genellikle uygulamasında kullanılan [EvaluateSync](../../../extensibility/debugger/reference/idebugexpression2-evaluatesync.md) ve [EvaluateAsync](../../../extensibility/debugger/reference/idebugexpression2-evaluateasync.md).

## <a name="methods-in-vtable-order"></a>Vtable sırayla yöntemleri
 Aşağıdaki tabloda yöntemlerini gösterilmektedir `IDebugBinder`.

|Yöntem|Açıklama|
|------------|-----------------|
|[Bind](../../../extensibility/debugger/reference/idebugbinder-bind.md)|Bellek bağlamı veya sembolün geçerli değerini içeren nesneyi alır.|
|[ResolveRuntimeType](../../../extensibility/debugger/reference/idebugbinder-resolveruntimetype.md)|Bir nesnenin çalışma zamanı türünü belirler.|
|[GetMemoryContext](../../../extensibility/debugger/reference/idebugbinder-getmemorycontext.md)|Bir nesne konumu veya bellek adresi bellek bağlamına dönüştürür.|
|[GetFunctionObject](../../../extensibility/debugger/reference/idebugbinder-getfunctionobject.md)|Alır bir [IDebugFunctionObject](../../../extensibility/debugger/reference/idebugfunctionobject.md) işlev parametreleri oluşturmak için kullanılan nesne.|
|[ResolveDynamicType](../../../extensibility/debugger/reference/idebugbinder-resolvedynamictype.md)|Tam türü için bir değişken alır.|

## <a name="remarks"></a>Açıklamalar
 Bu arabirim ifade değerlendiricide tarafından kullanılan nesneleri ayrıştırma ağaçlarını döndürür. İfade değerlendirici ifade sembolleri örneklerine dönüştürmek için Sembol sağlayıcısı kullanılarak bir ifade ayrıştırır [IDebugField](../../../extensibility/debugger/reference/idebugfield.md), her simge, türü ve konumu kaynak kodundaki açısından açıklar. [Bağlama](../../../extensibility/debugger/reference/idebugbinder-bind.md) yöntemi dönüştürür `IDebugField` nesneleri için [IDebugObject](../../../extensibility/debugger/reference/idebugobject.md) bağlanmak veya sembol bağlama nesnelerini türünü bellekte gerçek bir değer. Bunlar `IDebugObject` nesneleri sonraki değerlendirme için ayrıştırma ağacına ardından depolanır.

## <a name="requirements"></a>Gereksinimler
 Üstbilgi: ee.h

 Ad alanı: Microsoft.VisualStudio.Debugger.Interop

 Derleme: Microsoft.VisualStudio.Debugger.Interop.dll

## <a name="see-also"></a>Ayrıca Bkz.
- [İfade Değerlendirme Arabirimleri](../../../extensibility/debugger/reference/expression-evaluation-interfaces.md)
- [EvaluateSync](../../../extensibility/debugger/reference/idebugexpression2-evaluatesync.md)
- [EvaluateAsync](../../../extensibility/debugger/reference/idebugexpression2-evaluateasync.md)
- [IDebugFunctionObject](../../../extensibility/debugger/reference/idebugfunctionobject.md)
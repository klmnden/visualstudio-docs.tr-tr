---
title: IEEVisualizerDataProvider | Microsoft Docs
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- IEEVisualizerDataProvider
helpviewer_keywords:
- IEEVisualizerDataProvider interface
ms.assetid: 5fdfe6e3-b94e-4edb-acc5-41d8773d8ca5
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
dev_langs:
- CPP
- CSharp
ms.openlocfilehash: a4a070c17760ea8cf004b1fcc733f7fe38760db7
ms.sourcegitcommit: 6196d0b7fdcb08ba6d28a8151ad36b8d1139f2cc
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/07/2019
ms.locfileid: "65223955"
---
# <a name="ieevisualizerdataprovider"></a>IEEVisualizerDataProvider
> [!IMPORTANT]
> Visual Studio 2015'te, bu şekilde ifade değerlendiricisi uygulama kullanım dışı bırakılmıştır. CLR ifade değerlendiricisi uygulama hakkında daha fazla bilgi için lütfen bkz [CLR ifade Değerlendiricilerini](https://github.com/Microsoft/ConcordExtensibilitySamples/wiki/CLR-Expression-Evaluators) ve [yönetilen ifade değerlendiricisi örnek](https://github.com/Microsoft/ConcordExtensibilitySamples/wiki/Managed-Expression-Evaluator-Sample).

 Bu arabirim tür görselleştiricisi aracılığıyla bir nesnenin değerini değiştirme olanağı sağlar.

## <a name="syntax"></a>Sözdizimi

```
IEEVisualizerDataProvider : IUnknown
```

## <a name="notes-for-implementers"></a>Uygulayanlar için Notlar
 İfade değerlendirici değiştirme veri bir özellik nesnesi türü Görselleştirici aracılığıyla desteklemek için bu arabirimi uygular.

## <a name="notes-for-callers"></a>Arayanlar İçin Notlar
 Bu arabirim oluşturmak için kullanılan [IEEVisualizerService](../../../extensibility/debugger/reference/ieevisualizerservice.md) nesne yapılan bir çağrıyla [CreateVisualizerService](../../../extensibility/debugger/reference/ieevisualizerserviceprovider-createvisualizerservice.md). Bkz: [Visualizing ve verileri görüntüleme](../../../extensibility/debugger/visualizing-and-viewing-data.md) daha fazla ayrıntı için.

## <a name="methods-in-vtable-order"></a>Vtable sırayla yöntemleri

|Yöntem|Açıklama|
|------------|-----------------|
|[CanSetObjectForVisualizer](../../../extensibility/debugger/reference/ieevisualizerdataprovider-cansetobjectforvisualizer.md)|Nesne (ve sonuç olarak, değerini) güncelleştirmek mümkün olup olmadığını belirler, bu Görselleştirici temsil eden.|
|[GetNewObjectForVisualizer](../../../extensibility/debugger/reference/ieevisualizerdataprovider-getnewobjectforvisualizer.md)|Bir nesne değerlendirmeleri için bu Görselleştirici zorlar.|
|[GetObjectForVisualizer](../../../extensibility/debugger/reference/ieevisualizerdataprovider-getobjectforvisualizer.md)|Bu Görselleştirici (hiçbir değerlendirme gerçekleştirilir) için var olan bir nesneyi alır.|
|[SetObjectForVisualizer](../../../extensibility/debugger/reference/ieevisualizerdataprovider-setobjectforvisualizer.md)|Nesne, böylece görselleştiricisi sunan değeri değiştirmek için bu Görselleştirici güncelleştirir.|

## <a name="remarks"></a>Açıklamalar
 Görselleştirici hizmeti (tarafından temsil edilen [IEEVisualizerService](../../../extensibility/debugger/reference/ieevisualizerservice.md) arabirim ve tarafından döndürülen [CreateVisualizerService](../../../extensibility/debugger/reference/ieevisualizerserviceprovider-createvisualizerservice.md)) nesnesi uygulayan bir başvuru tutar `IEEVisualizerDataProvider` arabirimi . Sonuç olarak, `IEEVisualizerDataProvider` arabirimi değil uygulanmasını uygulayan aynı nesne üzerinde [IDebugProperty2](../../../extensibility/debugger/reference/idebugproperty2.md) bu nesneye bir başvuru tutuyorsa `IEEVisualizerService` nesne: bir döngüsel başvuru sonuçları ve Kilitlenme nesneleri kaldırıldığında gerçekleşir. Uygulamak için önerilen yaklaşımdır `IEEVisualizerDataProvider` ayrı bir nesne üzerinde `IDebugProperty2` nesne çağırmadan Temsilciler `IUnknown::AddRef` üzerindeki.

## <a name="requirements"></a>Gereksinimler
 Üstbilgi: ee.h

 Ad alanı: Microsoft.VisualStudio.Debugger.Interop

 Derleme: Microsoft.VisualStudio.Debugger.Interop.dll

## <a name="see-also"></a>Ayrıca bkz.
- [İfade Değerlendirme Arabirimleri](../../../extensibility/debugger/reference/expression-evaluation-interfaces.md)
- [IDebugProperty2](../../../extensibility/debugger/reference/idebugproperty2.md)
- [IEEVisualizerService](../../../extensibility/debugger/reference/ieevisualizerservice.md)
- [IEEVisualizerServiceProvider](../../../extensibility/debugger/reference/ieevisualizerserviceprovider.md)
- [Verileri Görselleştirme ve Görüntüleme](../../../extensibility/debugger/visualizing-and-viewing-data.md)
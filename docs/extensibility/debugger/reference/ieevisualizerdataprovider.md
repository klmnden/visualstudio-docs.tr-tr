---
title: IEEVisualizerDataProvider | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
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
ms.openlocfilehash: bc5c16d71fac3b52187b3e0392ed21bdd56a079f
ms.sourcegitcommit: 2193323efc608118e0ce6f6b2ff532f158245d56
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/25/2019
ms.locfileid: "54978327"
---
# <a name="ieevisualizerdataprovider"></a>IEEVisualizerDataProvider
> [!IMPORTANT]
>  Visual Studio 2015'te, bu şekilde ifade değerlendiricisi uygulama kullanım dışı bırakılmıştır. CLR ifade değerlendiricisi uygulama hakkında daha fazla bilgi için lütfen bkz [CLR ifade Değerlendiricilerini](https://github.com/Microsoft/ConcordExtensibilitySamples/wiki/CLR-Expression-Evaluators) ve [yönetilen ifade değerlendiricisi örnek](https://github.com/Microsoft/ConcordExtensibilitySamples/wiki/Managed-Expression-Evaluator-Sample).  
  
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
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [İfade değerlendirme arabirimleri](../../../extensibility/debugger/reference/expression-evaluation-interfaces.md)   
 [IDebugProperty2](../../../extensibility/debugger/reference/idebugproperty2.md)   
 [IEEVisualizerService](../../../extensibility/debugger/reference/ieevisualizerservice.md)   
 [IEEVisualizerServiceProvider](../../../extensibility/debugger/reference/ieevisualizerserviceprovider.md)   
 [Verileri Görselleştirme ve Görüntüleme](../../../extensibility/debugger/visualizing-and-viewing-data.md)
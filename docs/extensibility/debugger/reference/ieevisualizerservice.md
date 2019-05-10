---
title: IEEVisualizerService | Microsoft Docs
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- IEEVisualizerService
helpviewer_keywords:
- IEEVisualizerService interface
ms.assetid: 3bdb124b-c582-47ba-b465-13c6a1cdb702
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: 40941092fcfffe7e7d6340ba75842ef81383567d
ms.sourcegitcommit: 6196d0b7fdcb08ba6d28a8151ad36b8d1139f2cc
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/07/2019
ms.locfileid: "65223565"
---
# <a name="ieevisualizerservice"></a>IEEVisualizerService
> [!IMPORTANT]
> Visual Studio 2015'te, bu şekilde ifade değerlendiricisi uygulama kullanım dışı bırakılmıştır. CLR ifade değerlendiricisi uygulama hakkında daha fazla bilgi için lütfen bkz [CLR ifade Değerlendiricilerini](https://github.com/Microsoft/ConcordExtensibilitySamples/wiki/CLR-Expression-Evaluators) ve [yönetilen ifade değerlendiricisi örnek](https://github.com/Microsoft/ConcordExtensibilitySamples/wiki/Managed-Expression-Evaluator-Sample).

 İşlevsellik sağlayan anahtar yöntemleri bu arabirimi uygulayan [IDebugProperty3](../../../extensibility/debugger/reference/idebugproperty3.md) ve [IPropertyProxyEESide](../../../extensibility/debugger/reference/ipropertyproxyeeside.md) arabirimleri.

## <a name="syntax"></a>Sözdizimi

```
IEEVisualizerService : IUnknown
```

## <a name="notes-for-implementers"></a>Uygulayanlar için Notlar
 Visual Studio, bir ifade değerlendiricisi tür görselleştiricileri desteklemek için (EE) izin vermek için bu arabirimi uygular.

## <a name="notes-for-callers"></a>Arayanlar İçin Notlar
 EE çağrıları [CreateVisualizerService](../../../extensibility/debugger/reference/ieevisualizerserviceprovider-createvisualizerservice.md) bu arabirimi desteğini bir parçası olarak için tür görselleştiricileri elde edilir.

## <a name="methods-in-vtable-order"></a>Vtable sırayla yöntemleri

|Yöntem|Açıklama|
|------------|-----------------|
|[GetCustomViewerCount](../../../extensibility/debugger/reference/ieevisualizerservice-getcustomviewercount.md)|Bu hizmet hakkında bilen özel görüntüleyiciler sayısını alır.|
|[GetCustomViewerList](../../../extensibility/debugger/reference/ieevisualizerservice-getcustomviewerlist.md)|Özel görüntüleyiciler listesini alır.|
|[GetPropertyProxy](../../../extensibility/debugger/reference/ieevisualizerservice-getpropertyproxy.md)|Bir özellik için bir proxy nesnesi döndürür.|
|[GetValueDisplayStringCount](../../../extensibility/debugger/reference/ieevisualizerservice-getvaluedisplaystringcount.md)|Belirtilen özellik veya alan için görüntülenecek değer dizeleri sayısını alır.|

## <a name="remarks"></a>Açıklamalar
 IDE kullanır [IDebugProperty3](../../../extensibility/debugger/reference/idebugproperty3.md) herhangi bir özel görüntüleyiciler olup olmadığını belirlemek için arabirimi veya özelliği için görselleştiriciler yazın. Görselleştirici hizmeti oluşturarak (ile [CreateVisualizerService](../../../extensibility/debugger/reference/ieevisualizerserviceprovider-createvisualizerservice.md)), EE işlevsellik sağlayabilirsiniz `IDebugProperty3` ve [IPropertyProxyEESide](../../../extensibility/debugger/reference/ipropertyproxyeeside.md) (görüntüleme ve değiştirme destekleyen bir özelliğin değerini), arabirimleri ve böylece tür görselleştiricileri destekler.

 Bir EE özel görüntüleyiciler varsa, kendisini uygulayan, EE ekleyebilir `CLSID`s, bu özel görüntüleyiciler tarafından döndürülen listenin sonuna [GetCustomViewerList](../../../extensibility/debugger/reference/ieevisualizerservice-getcustomviewerlist.md). Bu tür görselleştiricileri hem kendi özel görüntüleyiciler desteklemek bir EE sağlar. Yalnızca olduğundan emin olun [GetCustomViewerCount](../../../extensibility/debugger/reference/idebugproperty3-getcustomviewercount.md) herhangi bir özel görüntüleyiciler eklenmesini yansıtır.

 Bkz: [tür görselleştiricisi ve özel Görüntüleyici](../../../extensibility/debugger/type-visualizer-and-custom-viewer.md) görselleştiriciler ve görüntüleyiciler arasındaki fark hakkında ayrıntılı bilgi için.

## <a name="requirements"></a>Gereksinimler
 Üstbilgi: ee.h

 Ad alanı: Microsoft.VisualStudio.Debugger.Interop

 Derleme: Microsoft.VisualStudio.Debugger.Interop.dll

## <a name="see-also"></a>Ayrıca bkz.
- [İfade Değerlendirme Arabirimleri](../../../extensibility/debugger/reference/expression-evaluation-interfaces.md)
- [IDebugProperty2](../../../extensibility/debugger/reference/idebugproperty2.md)
- [IDebugProperty3](../../../extensibility/debugger/reference/idebugproperty3.md)
- [IPropertyProxyEESide](../../../extensibility/debugger/reference/ipropertyproxyeeside.md)
- [CreateVisualizerService](../../../extensibility/debugger/reference/ieevisualizerserviceprovider-createvisualizerservice.md)
- [Tür Görselleştiricisi ve Özel Görüntüleyici](../../../extensibility/debugger/type-visualizer-and-custom-viewer.md)
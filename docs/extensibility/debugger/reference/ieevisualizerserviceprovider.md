---
title: IEEVisualizerServiceProvider | Microsoft Docs
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- IEEVisualizerServiceProvider
helpviewer_keywords:
- IEEVisualizerServiceProvider interface
ms.assetid: 859d1a51-1c65-4c8b-ae74-3b74b181ebcd
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: 63e6893d407ebcb26a62aeb038b0cf670659f536
ms.sourcegitcommit: b0d8e61745f67bd1f7ecf7fe080a0fe73ac6a181
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/22/2019
ms.locfileid: "56718386"
---
# <a name="ieevisualizerserviceprovider"></a>IEEVisualizerServiceProvider
> [!IMPORTANT]
>  Visual Studio 2015'te, bu şekilde ifade değerlendiricisi uygulama kullanım dışı bırakılmıştır. CLR ifade değerlendiricisi uygulama hakkında daha fazla bilgi için lütfen bkz [CLR ifade Değerlendiricilerini](https://github.com/Microsoft/ConcordExtensibilitySamples/wiki/CLR-Expression-Evaluators) ve [yönetilen ifade değerlendiricisi örnek](https://github.com/Microsoft/ConcordExtensibilitySamples/wiki/Managed-Expression-Evaluator-Sample).

 Bu arabirim tür görselleştiricisi görevleri için IDE işlemek için kullanılan bir görselleştiricisi hizmet oluşturabilmeniz için bir yöntem erişim sağlar.

## <a name="syntax"></a>Sözdizimi

```
IEEVisualizerServiceProvider : IUnknown
```

## <a name="notes-for-implementers"></a>Uygulayanlar için Notlar
 Visual Studio sırayla sınıfı kimliklerini sağlamak için kullanılan bir Görselleştirici hizmeti nesnesi oluşturmak için bu arabirimi uygulayan (`CLSID`s), Visual Studio IDE tür görselleştiricileri.

## <a name="notes-for-callers"></a>Arayanlar İçin Notlar
 İfade değerlendirici (EE) çağıran [GetEEService](../../../extensibility/debugger/reference/idebugbinder3-geteeservice.md) bu arabirimi elde edilir.

## <a name="methods-in-vtable-order"></a>Vtable sırayla yöntemleri

|Yöntem|Açıklama|
|------------|-----------------|
|[CreateVisualizerService](../../../extensibility/debugger/reference/ieevisualizerserviceprovider-createvisualizerservice.md)|Görselleştirici hizmeti oluşturur|

## <a name="remarks"></a>Açıklamalar
 `IEEVisualizerServiceProvider` Arabirim uygulamasını sırasında elde [EvaluateSync](../../../extensibility/debugger/reference/idebugparsedexpression-evaluatesync.md). Bu arabirim oluşturur Görselleştirici hizmeti işlevsellik sağlamak için kullanılan bir [IDebugProperty3](../../../extensibility/debugger/reference/idebugproperty3.md) , EE uygulamak için sorumlu olan arabirim. EE de uygulamak için sorumlu olduğu bir [IEEVisualizerDataProvider](../../../extensibility/debugger/reference/ieevisualizerdataprovider.md) görüntülemek ve bir özelliğin değerini değiştirmek tür görselleştiricileri arabirimi.

 Bkz: [Visualizing ve verileri görüntüleme](../../../extensibility/debugger/visualizing-and-viewing-data.md) Bu arabirimler nasıl etkileşime ilişkin ayrıntılar için.

## <a name="requirements"></a>Gereksinimler
 Üstbilgi: ee.h

 Ad alanı: Microsoft.VisualStudio.Debugger.Interop

 Derleme: Microsoft.VisualStudio.Debugger.Interop.dll

## <a name="see-also"></a>Ayrıca Bkz.
- [İfade Değerlendirme Arabirimleri](../../../extensibility/debugger/reference/expression-evaluation-interfaces.md)
- [EvaluateSync](../../../extensibility/debugger/reference/idebugparsedexpression-evaluatesync.md)
- [IEEVisualizerDataProvider](../../../extensibility/debugger/reference/ieevisualizerdataprovider.md)
- [GetEEService](../../../extensibility/debugger/reference/idebugbinder3-geteeservice.md)
- [IDebugProperty3](../../../extensibility/debugger/reference/idebugproperty3.md)
- [Verileri Görselleştirme ve Görüntüleme](../../../extensibility/debugger/visualizing-and-viewing-data.md)
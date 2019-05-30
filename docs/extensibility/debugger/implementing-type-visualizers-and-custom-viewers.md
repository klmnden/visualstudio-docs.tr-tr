---
title: Tür Görselleştiricileri ve özel görüntüleyiciler uygulama | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
helpviewer_keywords:
- debugging [Debugging SDK], custom viewer
- debugging [Debugging SDK], type visualizer
ms.assetid: abef18c0-8272-4451-b82a-b4624edaba7d
author: madskristensen
ms.author: madsk
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: 0f7e977df6236ea8c3310312114ba4fa30d5003a
ms.sourcegitcommit: 40d612240dc5bea418cd27fdacdf85ea177e2df3
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/29/2019
ms.locfileid: "66344195"
---
# <a name="implement-type-visualizers-and-custom-viewers"></a>Tür görselleştiricileri ve özel görüntüleyiciler uygulama
> [!IMPORTANT]
> Visual Studio 2015'te, bu şekilde ifade değerlendiricisi uygulama kullanım dışı bırakılmıştır. CLR ifade değerlendiricisi uygulama hakkında daha fazla bilgi için bkz: [CLR ifade değerlendiricilerini](https://github.com/Microsoft/ConcordExtensibilitySamples/wiki/CLR-Expression-Evaluators) ve [yönetilen ifade değerlendiricisi örnek](https://github.com/Microsoft/ConcordExtensibilitySamples/wiki/Managed-Expression-Evaluator-Sample).

 Tür görselleştiricileri ve özel görüntüleyiciler onaltılık sayı döküm basit daha anlamlı bir şekilde belirli bir türdeki veri görünümünde bir kullanıcı sağlar. İfade değerlendiricisi (EE) özel görüntüleyiciler belirli veri türlerine veya değişkenleri ile ilişkilendirebilirsiniz. Bu özel görüntüleyiciler EE tarafından uygulanır. Başka bir üçüncü taraf satıcı veya bile son kullanıcının gelebilir dış tür görselleştiriciler, EE de destekler.

## <a name="discussion"></a>Tartışma

### <a name="type-visualizers"></a>Tür görselleştiricileri
 Tür görselleştiricileri ve özel görüntüleyiciler Her nesne için izleme penceresinde görüntülenecek bir listesi için Visual Studio ister. İfade değerlendiricisi (EE) kendisi için tür görselleştiricileri ve özel görüntüleyiciler desteklemek istediği her türü için böyle bir liste sağlar. Çağrılar [GetCustomViewerCount](../../extensibility/debugger/reference/idebugproperty3-getcustomviewercount.md) ve [GetCustomViewerList](../../extensibility/debugger/reference/idebugproperty3-getcustomviewerlist.md) tür görselleştiricileri ve özel görüntüleyiciler erişen tüm işlemini başlatmak (bkz [Visualizing ve verileri görüntüleme](../../extensibility/debugger/visualizing-and-viewing-data.md)çağrı sırası hakkında ayrıntılı bilgi için).

### <a name="custom-viewers"></a>Özel görüntüleyiciler
 Özel görüntüleyiciler EE belirli bir tür için uygulanır ve tarafından temsil edilen [IDebugCustomViewer](../../extensibility/debugger/reference/idebugcustomviewer.md) arabirimi. Özel Görüntüleyici yalnızca bu belirli özel Görüntüleyici uygulayan EE çalıştırılırken kullanılabilir bir tür görselleştiricisi kadar esnek değildir. Özel Görüntüleyici uygulama tür görselleştiricileri desteği uygulamak daha kolaydır. Ancak, tür görselleştiricileri destekleyen maksimum esneklik için son kullanıcı verilerini görselleştirmek için sağlar. Bu tartışma geri kalanında, yalnızca tür görselleştiricileri ilgilidir.

## <a name="interfaces"></a>Arabirimler
 Tür görselleştiricileri, Visual Studio tarafından tüketilmesi desteklemek için aşağıdaki arabirimlerinden EE uygular:

- [IEEVisualizerDataProvider](../../extensibility/debugger/reference/ieevisualizerdataprovider.md)

- [IPropertyProxyEESide](../../extensibility/debugger/reference/ipropertyproxyeeside.md)

- [IPropertyProxyProvider](../../extensibility/debugger/reference/ipropertyproxyprovider.md)

- [IEEDataStorage](../../extensibility/debugger/reference/ieedatastorage.md)

- [IDebugProperty3](../../extensibility/debugger/reference/idebugproperty3.md)

- [IDebugObject](../../extensibility/debugger/reference/idebugobject.md)

  Tür görselleştiricileri desteklemek için aşağıdaki arabirimlerinden EE kullanır:

- [IEEVisualizerService](../../extensibility/debugger/reference/ieevisualizerservice.md)

- [IEEVisualizerServiceProvider](../../extensibility/debugger/reference/ieevisualizerserviceprovider.md)

- [IDebugBinder3](../../extensibility/debugger/reference/idebugbinder3.md)

## <a name="see-also"></a>Ayrıca bkz.
- [Bir CLR ifade değerlendiricisi yazma](../../extensibility/debugger/writing-a-common-language-runtime-expression-evaluator.md)
- [Verileri Görselleştirme ve görüntüleme](../../extensibility/debugger/visualizing-and-viewing-data.md)
- [IDebugCustomViewer](../../extensibility/debugger/reference/idebugcustomviewer.md)
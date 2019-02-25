---
title: Tür görselleştiricisi ve özel Görüntüleyici | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
helpviewer_keywords:
- debugging [Debugging SDK], custom viewer
- debugging [Debugging SDK], type visualizer
ms.assetid: fd3691e6-9c78-4767-846f-43f85ada4375
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: 219632bce50b6942d46e4061a3c7eaf8f70adfd5
ms.sourcegitcommit: b0d8e61745f67bd1f7ecf7fe080a0fe73ac6a181
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/22/2019
ms.locfileid: "56685969"
---
# <a name="type-visualizer-and-custom-viewer"></a>Tür görselleştiricisi ve özel Görüntüleyici
Tür görselleştiricisi bir veri parçasını belirli bir biçimde görüntüleyen bir bileşenidir. Tamamen biçimidir kimin Görselleştirici uygulayan kadar son kullanıcıya veya bir üçüncü taraf sağlayıcı görselleştiriciler, olması.

 Özel bir Görüntüleyici, bir veri parçasını belirli bir biçimde görüntüleyen bir özel ifade değerlendiricisi parçasıdır. Tamamen biçimi (EE) ifade değerlendiricisi ' uygulayan kadar olduğu anlamına gelir özel Görüntüleyici'nin uygulayan kadar bu biçimidir.

## <a name="support-for-type-visualizers-in-an-expression-evaluator"></a>İfade değerlendiricisi, tür görselleştiricileri desteği
 Görselleştiriciler için erişilebilir arabirimleri kümesi destekleyerek tür görselleştiricileri bir EE destekler: gibi arabirimleri [IEEVisualizerService](../../extensibility/debugger/reference/ieevisualizerservice.md) ve [IEEVisualizerDataProvider](../../extensibility/debugger/reference/ieevisualizerdataprovider.md). Ancak, EE tür görselleştiricisi uygulamak için sorumlu değildir: EE, dış görselleştiriciler yalnızca tür bilgisi erişmesine izin verir. Tür görselleştiricileri EE birlikte sevk ve uygun bir yerden başka bir üçüncü taraf satıcı veya bile son kullanıcı tarafından sağlanan Visual Studio yüklü.

## <a name="support-for-custom-viewers-in-an-expression-evaluator"></a>İfade değerlendiricisi, özel görüntüleyiciler için destek
 Özel görüntüleyiciler EE veri türünü görüntülemeye ilişkin kodu sağladığı bir EE de destekler. Özel bir Görüntüleyici uygulayan [IDebugCustomViewer](../../extensibility/debugger/reference/idebugcustomviewer.md) tüm görevleri, verileri hangi biçimde göstermenin işleyen arabirimi istenen; Görüntüleyici görünümü üzerinde tam denetime sahiptir ve değiştirilmesi veri bile izin verebilirsiniz. Ürün gönderildiğinde EE tarafından sağlanan herhangi bir özel görüntüleyiciler EE ile gelir.

## <a name="see-also"></a>Ayrıca bkz.
- [Hata ayıklayıcı bileşenleri](../../extensibility/debugger/debugger-components.md)
- [İfade değerlendirici](../../extensibility/debugger/expression-evaluator.md)
- [Hata ayıklama altyapısı](../../extensibility/debugger/debug-engine.md)
- [IDebugCustomViewer](../../extensibility/debugger/reference/idebugcustomviewer.md)
- [IEEVisualizerService](../../extensibility/debugger/reference/ieevisualizerservice.md)
- [IEEVisualizerDataProvider](../../extensibility/debugger/reference/ieevisualizerdataprovider.md)
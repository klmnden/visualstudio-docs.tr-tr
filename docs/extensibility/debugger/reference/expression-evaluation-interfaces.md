---
title: İfade değerlendirme arabirimleri | Microsoft Docs
ms.date: 11/04/2016
ms.topic: reference
helpviewer_keywords:
- expression evaluation, interfaces
ms.assetid: 2d259f60-2cd7-460e-b02d-24a8fb202850
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: 1a2dab234f56b9d6ab1368ac87f4da9c5fae4125
ms.sourcegitcommit: 1fc6ee928733e61a1f42782f832ead9f7946d00c
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/22/2019
ms.locfileid: "60113137"
---
# <a name="expression-evaluation-interfaces"></a>Expression Evaluation Interfaces
> [!IMPORTANT]
>  Visual Studio 2015'te, bu şekilde ifade değerlendiricisi uygulama kullanım dışı bırakılmıştır. CLR ifade değerlendiricisi uygulama hakkında daha fazla bilgi için lütfen bkz [CLR ifade Değerlendiricilerini](https://github.com/Microsoft/ConcordExtensibilitySamples/wiki/CLR-Expression-Evaluators) ve [yönetilen ifade değerlendiricisi örnek](https://github.com/Microsoft/ConcordExtensibilitySamples/wiki/Managed-Expression-Evaluator-Sample).

 İfade değerlendirme arabirimleri şunlardır [!INCLUDE[vsprvs](../../../code-quality/includes/vsprvs_md.md)] hata ayıklama SDK'sı.

## <a name="discussion"></a>Tartışma
 Bu arabirimler, kesme modu sırasında çağrı yığınını ifadelerinde değerlendirmek için kullanılır. Bunlar yalnızca ortak dil çalışma zamanı ifade değerlendiricilerini için (EE) uygulanır.

 Tablodaki her bir arabirim, aşağıdaki listeden uygulayabilirsiniz bileşeni gösterir:

- Hata ayıklama altyapısı (DE)

- İfade değerlendirici (EE)

- Visual Studio (VS)

|Arabirim|Uygulayan|Açıklama|
|---------------|--------------------|-----------------|
|[IDebugAlias](../../../extensibility/debugger/reference/idebugalias.md)|EE|Bir değişken için sayısal bir diğer adı temsil eder.|
|[IDebugAlias2](../../../extensibility/debugger/reference/idebugalias2.md)|EE|Bir değişken için sayısal bir diğer adı temsil eder ve bir ifade değerlendiricisi uygulama etki alanı diğer adı için elde edilir (EE) sağlar.|
|[IDebugArrayObject](../../../extensibility/debugger/reference/idebugarrayobject.md)|EE|Bir dizi nesnesi temsil eder.|
|[IDebugArrayObject2](../../../extensibility/debugger/reference/idebugarrayobject2.md)|EE|Yönetilen dizi nesnesini temsil eder ve bir ifade değerlendiricisi dizisi için temel dizin (alt sınırı) belirlemek için (EE) sağlar.|
|[IDebugBinder](../../../extensibility/debugger/reference/idebugbinder.md)|DE|Hata ayıklama simgeleri gerçek bellek adresleri için bağlamalar bir bağlayıcı temsil eder.|
|[IDebugBinder3](../../../extensibility/debugger/reference/idebugbinder3.md)|DE|Aynı [IDebugBinder](../../../extensibility/debugger/reference/idebugbinder.md) arabirim türleri, diğer adlar ve özel görselleştiriciler erişim ancak sağlar.|
|[IDebugExpressionEvaluator](../../../extensibility/debugger/reference/idebugexpressionevaluator.md)|EE|İfade değerlendirici temsil eder.|
|[IDebugExpressionEvaluator2](../../../extensibility/debugger/reference/idebugexpressionevaluator2.md)|EE|Gelişmiş bir ifade değerlendiricisi (EE) sürümünü temsil eder.|
|[IDebugExpressionEvaluator3](../../../extensibility/debugger/reference/idebugexpressionevaluator3.md)|EE|İfade değerlendiricisi (EE) ile bir Gelişmiş ayrıştırıcı ağacı temsil eder.|
|[IDebugFunctionObject](../../../extensibility/debugger/reference/idebugfunctionobject.md)|EE|Bir işlevi temsil eder.|
|[IDebugFunctionObject2](../../../extensibility/debugger/reference/idebugfunctionobject2.md)|EE|Bir işlevi temsil eder ve geliştirir [IDebugFunctionObject](../../../extensibility/debugger/reference/idebugfunctionobject.md) arabirimi.|
|[IDebugIDECallback](../../../extensibility/debugger/reference/idebugidecallback.md)|DE|Hata ayıklayıcının çıkış penceresinde bir ileti görüntülemek bir ifade değerlendiricisi (EE) sağlar.|
|[IDebugManagedObject](../../../extensibility/debugger/reference/idebugmanagedobject.md)|EE|Yönetilen kod nesnesini temsil eder.|
|[IDebugObject](../../../extensibility/debugger/reference/idebugobject.md)|EE|Herhangi bir simge temsil eden temel arabirim bir bellek adresini bağlı.|
|[IDebugObject2](../../../extensibility/debugger/reference/idebugobject2.md)|EE|Aynı [IDebugObject](../../../extensibility/debugger/reference/idebugobject.md) arabirimi, ancak ek bilgilere erişim sağlar.|
|[IDebugParsedExpression](../../../extensibility/debugger/reference/idebugparsedexpression.md)|EE|Değerlendirilecek hazır ayrıştırılmış bir ifade temsil eder.|
|[IDebugPointerObject](../../../extensibility/debugger/reference/idebugpointerobject.md)|EE|Bir işaretçiyi temsil eder.|
|[IDebugPointerObject3](../../../extensibility/debugger/reference/idebugpointerobject3.md)|EE|Bir ayrıştırma ağacı bir işaretçiyi temsil eder ve genişleten **IDebugPointerObject** arabirimi.|
|[IEEVisualizerDataProvider](../../../extensibility/debugger/reference/ieevisualizerdataprovider.md)|EE|Türün değeri bir tür görselleştiricisi ile değiştirme olanağı sağlar.|
|[IEEVisualizerService](../../../extensibility/debugger/reference/ieevisualizerservice.md)|VS|Özel görüntüleyiciler ve tür görselleştiricileri erişim sağlar.|
|[IEEVisualizerServiceProvider](../../../extensibility/debugger/reference/ieevisualizerserviceprovider.md)|VS|Oluşturma olanağı sağlayan bir [IEEVisualizerService](../../../extensibility/debugger/reference/ieevisualizerservice.md) nesne.|
|[IEnumDebugObjects](../../../extensibility/debugger/reference/ienumdebugobjects.md)|EE|Bir koleksiyonunu temsil eder [IDebugObject](../../../extensibility/debugger/reference/idebugobject.md) nesneleri.|

## <a name="see-also"></a>Ayrıca Bkz.
- [API Başvurusu](../../../extensibility/debugger/reference/api-reference-visual-studio-debugging.md)
- [CLR İfade Değerlendirici Yazma](../../../extensibility/debugger/writing-a-common-language-runtime-expression-evaluator.md)
- [Tür Görselleştiricisi ve Özel Görüntüleyici](../../../extensibility/debugger/type-visualizer-and-custom-viewer.md)
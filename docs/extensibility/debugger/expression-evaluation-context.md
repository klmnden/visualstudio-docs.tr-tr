---
title: İfade değerlendirme bağlamının | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
helpviewer_keywords:
- expression evaluation, context
ms.assetid: a2fd3758-09bd-45ae-8ecc-2d276c0036ba
author: madskristensen
ms.author: madsk
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: efaa678b5cbee763fabc9ccaf82c9322176b9102
ms.sourcegitcommit: 40d612240dc5bea418cd27fdacdf85ea177e2df3
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/29/2019
ms.locfileid: "66315233"
---
# <a name="expression-evaluation-context"></a>İfade değerlendirme bağlamı
İçinde [!INCLUDE[vsprvs](../../code-quality/includes/vsprvs_md.md)] hata ayıklama, bir **ifade değerlendirme bağlamının**:

- İfade değerlendirme bağlamının temsil eder. Genellikle, bir değerlendirme bağlam değişkenleri, parametreleri, İşlevler ve yöntemleri değerlendirileceği sözlü kapsamda karşılık gelir. Örneğin, bir yığın çerçevesiyle ilgili bir ifade değerlendirme bağlamı, yerel değişkenler, yöntem parametreleri ve sınıf üyeleri (varsa) değerlendirmesi için bağlamı sağlayacaktır.

- Bir kesme noktasında bir program durduğunda var. İfade, bağlama ve belirli bir bağlamda değerlendirmek için hazır ayrıştırılmış bir ifadeyi temsil eden bir veri yapısıdır.

     Daha ayrıntılı olarak ifadeleri kullanarak oluşturulan [ParseText](../../extensibility/debugger/reference/idebugexpressioncontext2-parsetext.md) yöntemi. Bir ifade değerlendirildiğinde değişken veya bağımsız değişken ve değeri türünü ve adını içeren bir yazdırılabilir bir dize oluşturur. Bu dize, İzleme penceresinde veya IDE'nin Yereller penceresinde görüntülenir.

     Verilen bir `BSTR` ve [IDebugExpressionContext2](../../extensibility/debugger/reference/idebugexpressioncontext2.md) arabirimi hata ayıklama altyapısı (DE) oluşturabilir bir [IDebugExpression2](../../extensibility/debugger/reference/idebugexpression2.md) bir ifade ayrıştırma tarafından arabirimi. Verilen bir `IDebugExpression2` arabirimini DE bir değer üzerinden zaman uyumlu veya zaman uyumsuz bir ifade değerlendirme alabilirsiniz. Bu değer, birlikte değişken veya bağımsız değişken türü ve ad IDE görüntülenmek üzere gönderilir.

## <a name="see-also"></a>Ayrıca bkz.
- [İfade değerlendirme arabirimleri](../../extensibility/debugger/reference/expression-evaluation-interfaces.md)
- [Hata ayıklayıcı bağlamları](../../extensibility/debugger/debugger-contexts.md)
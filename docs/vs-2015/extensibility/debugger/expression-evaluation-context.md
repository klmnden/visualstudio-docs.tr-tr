---
title: İfade değerlendirme bağlamının | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-sdk
ms.topic: conceptual
helpviewer_keywords:
- expression evaluation, context
ms.assetid: a2fd3758-09bd-45ae-8ecc-2d276c0036ba
caps.latest.revision: 12
ms.author: gregvanl
manager: jillfra
ms.openlocfilehash: 348fc23fbe240f36e647d12589a9255cec2afad0
ms.sourcegitcommit: 8b538eea125241e9d6d8b7297b72a66faa9a4a47
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54760810"
---
# <a name="expression-evaluation-context"></a>İfade Değerlendirme Bağlamı
[!INCLUDE[vs2017banner](../../includes/vs2017banner.md)]

İçinde [!INCLUDE[vsprvs](../../includes/vsprvs-md.md)] hata ayıklama, bir **ifade değerlendirme bağlamının**:  
  
-   İfade değerlendirme bağlamının temsil eder. Genellikle, bir değerlendirme bağlam değişkenleri, parametreleri, İşlevler ve yöntemleri değerlendirileceği sözlü kapsamda karşılık gelir. Örneğin, bir yığın çerçevesiyle ilgili bir ifade değerlendirme bağlamı, yerel değişkenler, yöntem parametreleri ve sınıf üyeleri (varsa) değerlendirmesi için bağlamı sağlayacaktır.  
  
-   Bir kesme noktasında bir program durduğunda var. İfade, bağlama ve belirli bir bağlamda değerlendirmek için hazır ayrıştırılmış bir ifadeyi temsil eden bir veri yapısıdır.  
  
     Daha ayrıntılı olarak ifadeleri kullanarak oluşturulan [ParseText](../../extensibility/debugger/reference/idebugexpressioncontext2-parsetext.md) yöntemi. Bir ifade değerlendirildiğinde değişken veya bağımsız değişken ve değeri türünü ve adını içeren bir yazdırılabilir bir dize oluşturur. Bu dize, İzleme penceresinde veya IDE'nin Yereller penceresinde görüntülenir.  
  
     Verilen bir `BSTR` ve [IDebugExpressionContext2](../../extensibility/debugger/reference/idebugexpressioncontext2.md) arabirimi hata ayıklama altyapısı (DE) oluşturabilir bir [IDebugExpression2](../../extensibility/debugger/reference/idebugexpression2.md) bir ifade ayrıştırma tarafından arabirimi. Verilen bir `IDebugExpression2` arabirimini DE bir değer üzerinden zaman uyumlu veya zaman uyumsuz bir ifade değerlendirme alabilirsiniz. Bu değer, birlikte değişken veya bağımsız değişken türü ve ad IDE görüntülenmek üzere gönderilir.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [İfade değerlendirme arabirimleri](../../extensibility/debugger/reference/expression-evaluation-interfaces.md)   
 [Hata Ayıklayıcı Bağlamları](../../extensibility/debugger/debugger-contexts.md)

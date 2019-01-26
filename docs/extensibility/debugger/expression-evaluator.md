---
title: İfade değerlendirici | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
helpviewer_keywords:
- expressions [Debugging SDK]
- debugging [Debugging SDK], expression evaluation
- expression evaluation
ms.assetid: f9381b2f-99aa-426c-aea0-d9c15f3c859b
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: b7eda2399b3bd711664e141800c503f31b12e244
ms.sourcegitcommit: 2193323efc608118e0ce6f6b2ff532f158245d56
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/25/2019
ms.locfileid: "54916556"
---
# <a name="expression-evaluator"></a>İfade değerlendirici
İfade değerlendiricilerini (EE), bunları IDE kesme modundayken, kullanıcı tarafından görüntülenmesine izin verme ayrıştırılamadı ve çalışma zamanında değişkenleri ve ifadeleri değerlendirin dilinin sözdizimi inceleyin.  
  
## <a name="use-expression-evaluators"></a>İfade değerlendiricilerini kullan  
 İfadeleri kullanarak oluşturulan [ParseText](../../extensibility/debugger/reference/idebugexpressioncontext2-parsetext.md) yöntemini aşağıdaki gibi:  
  
1. Hata ayıklama altyapısı (DE) uygulayan [IDebugExpressionContext2](../../extensibility/debugger/reference/idebugexpressioncontext2.md) arabirimi.  
  
2. Hata ayıklama paketi alır bir `IDebugExpressionContext2` nesnesinden bir [IDebugStackFrame2](../../extensibility/debugger/reference/idebugstackframe2.md) arabirimi ve çağrıları `IDebugStackFrame2::ParseText` almak için yöntemi bir [IDebugExpression2](../../extensibility/debugger/reference/idebugexpression2.md) nesne.  
  
3. Hata ayıklama paketi çağrıları [EvaluateSync](../../extensibility/debugger/reference/idebugexpression2-evaluatesync.md) yöntemi veya [EvaluateAsync](../../extensibility/debugger/reference/idebugexpression2-evaluateasync.md) ifadenin değerini almak için yöntemi. `IDebugExpression2::EvaluateAsync` Komut/hemen penceresinden çağrılır. Diğer tüm kullanıcı Arabirimi bileşenleri çağırma `IDebugExpression2::EvaluateSync`.  
  
4. İfade değerlendirmesinin sonucu olan bir [IDebugProperty2](../../extensibility/debugger/reference/idebugproperty2.md) adı, tür ve ifade değerlendirme sonucu değerini içeren bir nesne.  
  
   İfade değerlendirme sırasında EE sembol sağlayıcısı bileşenini bilgileri gerektirir. Sembol sağlayıcısı ayrıştırılmış ifade anlama ve tanımlamak için kullanılan bir sembolik bilgi sağlar.  
  
   Zaman uyumsuz bir ifade değerlendirme tamamlandıktan sonra zaman uyumsuz bir olay tarafından oturum hata ayıklama Yöneticisi (SDM) üzerinden DE IDE ifade değerlendirme tamamlandıktan bildirim gönderilir. Ve değerlendirme sonucu ardından çağrısından döndürülen `IDebugExpression2::EvaluateSync` yöntemi.  
  
## <a name="implementation-notes"></a>Uygulama notları  
 [!INCLUDE[vsprvs](../../code-quality/includes/vsprvs_md.md)] Hata ayıklama motorlarını beklediğiniz ortak dil çalışma zamanı (CLR) arabirimlerini kullanarak ifade değerlendiricisi ile bahsedeceğiz. Sonuç olarak, bir ifade değerlendiricisi çalıştığını ile [!INCLUDE[vsprvs](../../code-quality/includes/vsprvs_md.md)] hata ayıklama motorlarını CLR desteklemesi gerekir (tüm CLR hata ayıklama arabirimleri tam listesi parçası olan debugref.doc içinde bulunabilir, [!INCLUDE[winsdklong](../../deployment/includes/winsdklong_md.md)]).  
  
## <a name="see-also"></a>Ayrıca bkz.  
 [Hata ayıklayıcı bileşenleri](../../extensibility/debugger/debugger-components.md)
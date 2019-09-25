---
title: 'CA2212: Servis verilen bileşenleri WebMethod ile işaretlemeyin'
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- CA2212
- DoNotMarkServicedComponentsWithWebMethod
helpviewer_keywords:
- CA2212
- DoNotMarkServicedComponentsWithWebMethod
ms.assetid: 774bc55d-e588-48ee-8f38-c228580feca2
author: gewarren
ms.author: gewarren
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 7b2ace5f6e51fc7a8d29faab14cc2332fd808f93
ms.sourcegitcommit: 0c2523d975d48926dd2b35bcd2d32a8ae14c06d8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/24/2019
ms.locfileid: "71231662"
---
# <a name="ca2212-do-not-mark-serviced-components-with-webmethod"></a>CA2212: Servis verilen bileşenleri WebMethod ile işaretlemeyin

|||
|-|-|
|TypeName|DoNotMarkServicedComponentsWithWebMethod|
|CheckId|CA2212|
|Kategori|Microsoft. Usage|
|Son değişiklik|Yeni|

## <a name="cause"></a>Sebep

Öğesinden <xref:System.EnterpriseServices.ServicedComponent?displayProperty=fullName> devralan bir tür yöntemi ile <xref:System.Web.Services.WebMethodAttribute?displayProperty=fullName>işaretlenir.

## <a name="rule-description"></a>Kural açıklaması

<xref:System.Web.Services.WebMethodAttribute>ASP.NET kullanılarak oluşturulmuş bir XML Web hizmeti içindeki yöntemler için geçerlidir; yöntemi, uzak Web istemcilerinden çağrılabilir hale getirir. Yöntem ve sınıf ortak olmalıdır ve bir ASP.NET Web uygulamasında yürütmelidir. <xref:System.EnterpriseServices.ServicedComponent>türler COM+ uygulamaları tarafından barındırılır ve COM+ Hizmetleri kullanılabilir. <xref:System.Web.Services.WebMethodAttribute>, aynı senaryolar için <xref:System.EnterpriseServices.ServicedComponent> düşünülmediği için türlere uygulanmaz. Özellikle, özniteliği <xref:System.EnterpriseServices.ServicedComponent> yöntemine eklemek yöntemi uzak Web istemcilerinden çağrılabilir hale getirir. Ve <xref:System.Web.Services.WebMethodAttribute> bir<xref:System.EnterpriseServices.ServicedComponent> yönteminde bağlam ve işlem akışı için çakışan davranışlar ve gereksinimler olduğundan, metodun davranışı bazı senaryolarda yanlış olacaktır.

## <a name="how-to-fix-violations"></a>İhlalleri çözme

Bu kuralın ihlalini onarmak için, <xref:System.EnterpriseServices.ServicedComponent> yönteminden özniteliğini kaldırın.

## <a name="when-to-suppress-warnings"></a>Uyarıların ne zaman bastırılamıyor

Bu kuraldan uyarıyı bastırmayın. Bu öğelerin birleştirilmesinin doğru olduğu bir senaryo yoktur.

## <a name="see-also"></a>Ayrıca bkz.

- <xref:System.EnterpriseServices.ServicedComponent?displayProperty=fullName>
- <xref:System.Web.Services.WebMethodAttribute?displayProperty=fullName>
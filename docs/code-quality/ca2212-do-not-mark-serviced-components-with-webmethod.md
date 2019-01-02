---
title: 'CA2212: Servis verilen bileşenleri WebMethod ile işaretlemeyin'
ms.date: 11/04/2016
ms.prod: visual-studio-dev15
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
manager: douge
ms.workload:
- multiple
ms.openlocfilehash: 402e27bcfb94adc73aa5376ca71271e8d55f5d8d
ms.sourcegitcommit: 37fb7075b0a65d2add3b137a5230767aa3266c74
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/02/2019
ms.locfileid: "53856676"
---
# <a name="ca2212-do-not-mark-serviced-components-with-webmethod"></a>CA2212: Servis verilen bileşenleri WebMethod ile işaretlemeyin

|||
|-|-|
|TypeName|DoNotMarkServicedComponentsWithWebMethod|
|CheckId|CA2212|
|Kategori|Microsoft.Usage|
|Yeni Değişiklik|Yeni|

## <a name="cause"></a>Sebep

Devralınan bir türde bir yöntemin <xref:System.EnterpriseServices.ServicedComponent?displayProperty=fullName> ile işaretlenmiş <xref:System.Web.Services.WebMethodAttribute?displayProperty=fullName>.

## <a name="rule-description"></a>Kural açıklaması

<xref:System.Web.Services.WebMethodAttribute> ASP.NET kullanarak oluşturulan bir XML web hizmeti yöntemlerini uygular; yöntem çağrılabilir Uzak web istemcilerinden kolaylaştırır. Sınıf ve yöntem, genel ve çalışan bir ASP.NET web uygulamasında olması gerekir. <xref:System.EnterpriseServices.ServicedComponent> türleri COM + uygulamaları tarafından barındırılan ve COM + Hizmetleri kullanabilir. <xref:System.Web.Services.WebMethodAttribute> uygulanmaz <xref:System.EnterpriseServices.ServicedComponent> çünkü aynı senaryolar için tasarlanmamıştır. Özellikle, öznitelik için ekleme <xref:System.EnterpriseServices.ServicedComponent> yöntemi yapmaz yöntemi çağrılabilir Uzak web istemcilerinden. Çünkü <xref:System.Web.Services.WebMethodAttribute> ve <xref:System.EnterpriseServices.ServicedComponent> yöntemine sahip çakışan davranışları ve bağlam ve işlem akışı, yöntemin davranışını gereksinimleri bazı senaryolarda yanlış olacaktır.

## <a name="how-to-fix-violations"></a>İhlaller nasıl düzeltilir?

Bu kural ihlalini düzeltmek için özniteliği kaldırın. <xref:System.EnterpriseServices.ServicedComponent> yöntemi.

## <a name="when-to-suppress-warnings"></a>Uyarılar bastırıldığında

Bu kuraldan uyarıyı bastırmayın. Bu öğeleri birleştirme doğru olduğu senaryo vardır.

## <a name="see-also"></a>Ayrıca bkz.

- <xref:System.EnterpriseServices.ServicedComponent?displayProperty=fullName>
- <xref:System.Web.Services.WebMethodAttribute?displayProperty=fullName>
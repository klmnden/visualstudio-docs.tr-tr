---
title: 'CA2212: Servis verilen bileşenleri WebMethod ile işaretlemeyin | Microsoft Docs'
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-code-analysis
ms.topic: reference
f1_keywords:
- CA2212
- DoNotMarkServicedComponentsWithWebMethod
helpviewer_keywords:
- CA2212
- DoNotMarkServicedComponentsWithWebMethod
ms.assetid: 774bc55d-e588-48ee-8f38-c228580feca2
caps.latest.revision: 15
author: gewarren
ms.author: gewarren
manager: wpickett
ms.openlocfilehash: 6f2e89705e36407e39103296e3eee70482e3d03f
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "68142478"
---
# <a name="ca2212-do-not-mark-serviced-components-with-webmethod"></a>CA2212: Servis verilen bileşenleri WebMethod ile işaretlemeyin
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

|||
|-|-|
|TypeName|DoNotMarkServicedComponentsWithWebMethod|
|CheckId|CA2212|
|Kategori|Microsoft.Usage|
|Yeni Değişiklik|Yeni|

## <a name="cause"></a>Sebep
 Devralınan bir türde bir yöntemin <xref:System.EnterpriseServices.ServicedComponent?displayProperty=fullName> ile işaretlenmiş <xref:System.Web.Services.WebMethodAttribute?displayProperty=fullName>.

## <a name="rule-description"></a>Kural Tanımı
 <xref:System.Web.Services.WebMethodAttribute> ASP.NET kullanarak oluşturulan bir XML Web hizmeti yöntemlerini uygular; yöntem çağrılabilir uzak Web istemcilerinden kolaylaştırır. Metot ve sınıf, genel ve bir ASP.NET Web uygulamasında yürütme olması gerekir. <xref:System.EnterpriseServices.ServicedComponent> türleri COM + uygulamaları tarafından barındırılan ve COM + Hizmetleri kullanabilir. <xref:System.Web.Services.WebMethodAttribute> uygulanmaz <xref:System.EnterpriseServices.ServicedComponent> çünkü aynı senaryolar için tasarlanmamıştır. Özellikle, öznitelik için ekleme <xref:System.EnterpriseServices.ServicedComponent> yöntemi yapmaz yöntemi çağrılabilir uzak Web istemcilerinden. Çünkü <xref:System.Web.Services.WebMethodAttribute> ve <xref:System.EnterpriseServices.ServicedComponent> yöntemine sahip çakışan davranışları ve bağlam ve işlem akışı, yöntemin davranışını gereksinimleri bazı senaryolarda yanlış olacaktır.

## <a name="how-to-fix-violations"></a>İhlaller Nasıl Düzeltilir?
 Bu kural ihlalini düzeltmek için özniteliği kaldırın. <xref:System.EnterpriseServices.ServicedComponent> yöntemi.

## <a name="when-to-suppress-warnings"></a>Uyarılar Bastırıldığında
 Bu kuraldan uyarıyı bastırmayın. Bu öğeleri birleştirme doğru olduğu senaryo vardır.

## <a name="see-also"></a>Ayrıca Bkz.
 <xref:System.EnterpriseServices.ServicedComponent?displayProperty=fullName><xref:System.Web.Services.WebMethodAttribute?displayProperty=fullName>

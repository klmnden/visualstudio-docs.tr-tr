---
title: 'CA1307: StringComparison belirtme | Microsoft Docs'
ms.custom: ''
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.reviewer: ''
ms.suite: ''
ms.technology: vs-devops-test
ms.tgt_pltfrm: ''
ms.topic: article
f1_keywords:
- CA1307
- SpecifyStringComparison
helpviewer_keywords:
- CA1307
- SpecifyStringComparison
ms.assetid: 9b0d5e71-1683-4a0d-bc4a-68b2fbd8af71
caps.latest.revision: 13
author: gewarren
ms.author: gewarren
manager: wpickett
ms.openlocfilehash: 577ca853d6b68696640d368cc9e52e4c7bb051c2
ms.sourcegitcommit: 37fb7075b0a65d2add3b137a5230767aa3266c74
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/02/2019
ms.locfileid: "53887003"
---
# <a name="ca1307-specify-stringcomparison"></a>CA1307: StringComparison belirtin
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

|||
|-|-|
|TypeName|SpecifyStringComparison|
|CheckId|CA1307|
|Kategori|Microsoft.Globalization|
|Yeni Değişiklik|Bölünemez|

## <a name="cause"></a>Sebep
 Ayarlanmamış bir yöntemi aşırı bir dize karşılaştırma işlemi kullanan bir <xref:System.StringComparison> parametresi.

## <a name="rule-description"></a>Kural Tanımı
 Çoğu dize işlemleri, en önemli <xref:System.String.Compare%2A> ve <xref:System.String.Equals%2A> yöntemlerini sağlar kabul eden bir aşırı bir <xref:System.StringComparison> numaralandırma değeri olarak bir parametre.

 Her bir aşırı var. Bu alır bir <xref:System.StringComparison> parametresi, bu parametre almayan bir aşırı yükleme yerine kullanılmalıdır. Bu parametre açıkça ayarlayarak, genellikle yapılan daha açık ve bakımını kodudur.

## <a name="how-to-fix-violations"></a>İhlaller Nasıl Düzeltilir?
 Bu kural ihlalini düzeltmek için dize karşılaştırma yöntemleri kabul eden aşırı yüklemeler için değişiklik <xref:System.StringComparison> parametre olarak numaralandırması. Örneğin: değiştirmek `String.Compare(str1, str2)` için `String.Compare(str1, str2, StringComparison.Ordinal)`.

## <a name="when-to-suppress-warnings"></a>Uyarılar Bastırıldığında
 Uygulama ve kitaplık yerel sınırlı bir kitle için tasarlanmıştır ve değil yerelleştirilecek olduğunda bu kuraldan bir uyarıyı bastırmak güvenlidir.

## <a name="see-also"></a>Ayrıca Bkz.
 [Genelleştirme uyarıları](../code-quality/globalization-warnings.md) [CA1309: Sıralı StringComparison kullanın](../code-quality/ca1309-use-ordinal-stringcomparison.md)

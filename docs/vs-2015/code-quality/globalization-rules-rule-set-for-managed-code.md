---
title: Yönetilen kod için genelleştirme kuralları kural kümesi | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-code-analysis
ms.topic: conceptual
ms.assetid: 3c4032ee-0805-4581-8c48-b1827cd6b213
caps.latest.revision: 11
author: gewarren
ms.author: gewarren
manager: wpickett
ms.openlocfilehash: 9d4e196ce3a6168db3ed74e667b5f4f48177859f
ms.sourcegitcommit: 8b538eea125241e9d6d8b7297b72a66faa9a4a47
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54786602"
---
# <a name="globalization-rules-rule-set-for-managed-code"></a>Yönetilen kod için Genelleştirme Kuralları kural kümesi
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Microsoft Genelleştirme kuralları kural veri uygulamanızın farklı dil, yerel ayarlar ve kültürler düzgün görüntülenmesini engelleyen sorunlara odaklanmak için kümesi kullanabilirsiniz. Bu kural, uygulama Eğer, yerelleştirilmiş ise, kümesi veya her ikisini de içermelidir.  
  
|Kural|Açıklama|  
|----------|-----------------|  
|[CA1300](../code-quality/ca1300-specify-messageboxoptions.md)|MessageBoxOptions belirt|  
|[CA1301](../code-quality/ca1301-avoid-duplicate-accelerators.md)|Yinelenen hızlandırıcılardan kaçının|  
|[CA1302](../code-quality/ca1302-do-not-hardcode-locale-specific-strings.md)|Yerel özel dizeleri doğrudan programın içine gömmeyin|  
|[CA1303](../code-quality/ca1303-do-not-pass-literals-as-localized-parameters.md)|Harfleri yerelleştirilmiş parametreler olarak göndermeyin|  
|[CA1304](../code-quality/ca1304-specify-cultureinfo.md)|CultureInfo belirt|  
|[CA1305](../code-quality/ca1305-specify-iformatprovider.md)|IFormatProvider belirt|  
|[CA1306](../code-quality/ca1306-set-locale-for-data-types.md)|Veri türleri için yereli ayarlayın|  
|[CA1307](../code-quality/ca1307-specify-stringcomparison.md)|StringComparison belirt|  
|[CA1308](../code-quality/ca1308-normalize-strings-to-uppercase.md)|Dizeleri büyük harfe normalleştirin|  
|[CA1309](../code-quality/ca1309-use-ordinal-stringcomparison.md)|Sıralı StringComparison kullanın|  
|[CA2101](../code-quality/ca2101-specify-marshaling-for-p-invoke-string-arguments.md)|P/Invoke dize bağımsız değişkenleri için sıralama belirtin|

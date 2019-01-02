---
title: Yönetilen kod için Genelleştirme Kuralları kural kümesi
ms.date: 11/04/2016
ms.prod: visual-studio-dev15
ms.topic: reference
ms.assetid: 3c4032ee-0805-4581-8c48-b1827cd6b213
author: gewarren
ms.author: gewarren
manager: douge
ms.workload:
- dotnet
ms.openlocfilehash: a0c0eb4edfb58d740692f2afff187659a665b234
ms.sourcegitcommit: 37fb7075b0a65d2add3b137a5230767aa3266c74
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/02/2019
ms.locfileid: "53936990"
---
# <a name="globalization-rules-rule-set-for-managed-code"></a>Yönetilen kod için Genelleştirme Kuralları kural kümesi
Microsoft Genelleştirme kuralları kural veri uygulamanızın farklı dil, yerel ayarlar ve kültürler düzgün görüntülenmesini engelleyen sorunlara odaklanmak için kümesi kullanabilirsiniz. Bu kural, uygulama Eğer, yerelleştirilmiş ise, kümesi veya her ikisini de içermelidir.

|Kural|Açıklama|
|----------|-----------------|
|[CA1300](../code-quality/ca1300-specify-messageboxoptions.md)|MessageBoxOptions belirtin|
|[CA1301](../code-quality/ca1301-avoid-duplicate-accelerators.md)|Yinelenen hızlandırıcılardan kaçının|
|[CA1302](../code-quality/ca1302-do-not-hardcode-locale-specific-strings.md)|Yerel özel dizeleri otomatik olarak gömmeyin|
|[CA1303](../code-quality/ca1303-do-not-pass-literals-as-localized-parameters.md)|Harfleri yerelleştirilmiş parametreler olarak göndermeyin|
|[CA1304](../code-quality/ca1304-specify-cultureinfo.md)|CultureInfo belirt|
|[CA1305](../code-quality/ca1305-specify-iformatprovider.md)|Iformatprovider belirtin|
|[CA1306](../code-quality/ca1306-set-locale-for-data-types.md)|Veri türleri için Yereli ayarlayın|
|[CA1307](../code-quality/ca1307-specify-stringcomparison.md)|StringComparison belirtin|
|[CA1308](../code-quality/ca1308-normalize-strings-to-uppercase.md)|Dizeleri büyük harfe normalleştirin|
|[CA1309](../code-quality/ca1309-use-ordinal-stringcomparison.md)|Sıralı StringComparison kullanın|
|[CA2101](../code-quality/ca2101-specify-marshaling-for-p-invoke-string-arguments.md)|P/Invoke dize bağımsız değişkenleri için hazırlama belirtin|
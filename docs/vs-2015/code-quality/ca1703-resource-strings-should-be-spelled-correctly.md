---
title: 'CA1703: Kaynak dizeleri yazıldığından | Microsoft Docs'
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-code-analysis
ms.topic: reference
f1_keywords:
- ResourceStringsShouldBeSpelledCorrectly
- CA1703
helpviewer_keywords:
- CA1703
- ResourceStringsShouldBeSpelledCorrectly
ms.assetid: 693f4970-f512-40cb-ae3b-a0f3a5c6d6f1
caps.latest.revision: 18
author: gewarren
ms.author: gewarren
manager: wpickett
ms.openlocfilehash: c1ff5a2600a4f40673f7d38dfe551ab9ac8cfe29
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "68189224"
---
# <a name="ca1703-resource-strings-should-be-spelled-correctly"></a>CA1703: Kaynak dizeleri doğru yazılmalıdır
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

|||
|-|-|
|TypeName|ResourceStringsShouldBeSpelledCorrectly|
|CheckId|CA1703|
|Kategori|Microsoft.Naming|
|Yeni Değişiklik|Bölünemez|

## <a name="cause"></a>Sebep
 Kaynak dizesi, Microsoft Yazım kitaplığı tarafından tanınmayan bir veya birkaç sözcük içerir.

## <a name="rule-description"></a>Kural Tanımı
 Bu kural kaynak dizesi (bileşik sözcüklerin) kelimelere ayrıştırır ve her kelimenin/belirtecin yazımını denetler. Ayrıştırma algoritma hakkında daha fazla bilgi için bkz. [CA1704: Tanımlayıcıları yazıldığından](../code-quality/ca1704-identifiers-should-be-spelled-correctly.md).

 Varsayılan olarak, yazım denetimcisi (TR) İngilizce sürümü kullanılır.

## <a name="how-to-fix-violations"></a>İhlaller Nasıl Düzeltilir?
 Bu kural ihlalini düzeltmek için sözcüklerin bir özel sözlüğüne ekleyin ya da doğru yazıldığından tam sözcük kullanın. Özel sözlükler kullanma hakkında daha fazla bilgi için bkz: [CA1704: Tanımlayıcıları yazıldığından](../code-quality/ca1704-identifiers-should-be-spelled-correctly.md).

## <a name="when-to-suppress-warnings"></a>Uyarılar Bastırıldığında
 Bu kuraldan uyarıyı bastırmayın. Doğru bir şekilde yazılmış kelimeler yeni yazılım kitaplıkları öğrenmek için gereken süreyi azaltın.

## <a name="related-rules"></a>İlgili kuralları
 [CA1701: Kaynak dize bileşik sözcüklerinin doğru yazılmalıdır](../code-quality/ca1701-resource-string-compound-words-should-be-cased-correctly.md)

 [CA1704: Tanımlayıcılar doğru yazılmalıdır](../code-quality/ca1704-identifiers-should-be-spelled-correctly.md)

 [CA2204: Değişmez değerler doğru yazılmalıdır](../code-quality/ca2204-literals-should-be-spelled-correctly.md)

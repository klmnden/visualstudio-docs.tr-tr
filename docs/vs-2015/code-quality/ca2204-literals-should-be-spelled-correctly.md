---
title: 'CA2204: Değişmez değerler yazıldığından | Microsoft Docs'
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-code-analysis
ms.topic: reference
f1_keywords:
- Literals should be spelled correctly
- CA2204
- LiteralsShouldBeSpelledCorrectly
helpviewer_keywords:
- CA2204
ms.assetid: b0bbcbb6-c92d-4c14-8ef7-9c8b38c791a6
caps.latest.revision: 21
author: gewarren
ms.author: gewarren
manager: wpickett
ms.openlocfilehash: a08cb7cee2af51ade4b94dbf675ff83d7da456e2
ms.sourcegitcommit: 8b538eea125241e9d6d8b7297b72a66faa9a4a47
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54786563"
---
# <a name="ca2204-literals-should-be-spelled-correctly"></a>CA2204: Harfler doğru yazılmalıdır
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

|||
|-|-|
|TypeName|LiteralsShouldBeSpelledCorrectly|
|CheckId|CA2204|
|Kategori|Microsoft.Usage|
|Yeni Değişiklik|Bozucu olmayan|

## <a name="cause"></a>Sebep
 Bir sabit dizesi, bir parametre veya bir yerelleştirilmiş dize arar ve sabit dizesini gerektiren özelliği kullanılır. bir yöntem geçişleri Microsoft Yazım kitaplığı tarafından tanınmayan bir veya birkaç sözcük içerir.

## <a name="rule-description"></a>Kural Tanımı
 Bu kural, bir parametre veya bir özellik için bir değer olarak geçirilen bir sabit dize denetler veya aşağıdaki durumlarda daha fazla doğrudur:

- <xref:System.ComponentModel.LocalizableAttribute> Özniteliği parametre ya da özelliğin true.

- Parametresi veya özellik adı "Metin", "İleti" veya "Başlık" içeriyor.

- "Value" veya "biçim" Console.Write veya Console.WriteLine yönteme geçirilen dize parametresi adıdır.

  Bu kural sabit dizesini bileşik sözcüklerin kelimelere, ayrıştırır ve her kelimenin/belirtecin yazımını denetler. Ayrıştırma algoritma hakkında daha fazla bilgi için bkz. [CA1704: Tanımlayıcıları yazıldığından](../code-quality/ca1704-identifiers-should-be-spelled-correctly.md).

  Varsayılan olarak, yazım denetimcisi (TR) İngilizce sürümü kullanılır.

## <a name="how-to-fix-violations"></a>İhlaller Nasıl Düzeltilir?
 Bu kural ihlalini düzeltmek için sözcük yazımını düzeltin ya da sözcüğü bir özel sözlüğüne ekleyin. Özel sözlükler kullanma hakkında daha fazla bilgi için bkz: [nasıl yapılır: Kod çözümleme dizinini özelleştirme](../code-quality/how-to-customize-the-code-analysis-dictionary.md).

## <a name="when-to-suppress-warnings"></a>Uyarılar Bastırıldığında
 Bu kuraldan uyarıyı bastırmayın. Doğru bir şekilde yazılmış kelimeler yeni yazılım kitaplıkları için gereken öğrenme eğrisini azaltır.

## <a name="related-rules"></a>İlgili kuralları
 [CA1704: Tanımlayıcılar doğru yazılmalıdır](../code-quality/ca1704-identifiers-should-be-spelled-correctly.md)

 [CA1703: Kaynak dizeler doğru yazılmalıdır](../code-quality/ca1703-resource-strings-should-be-spelled-correctly.md)

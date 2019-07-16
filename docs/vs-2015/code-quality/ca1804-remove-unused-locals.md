---
title: 'CA1804: Kullanılmayan yerel öğeleri Kaldır | Microsoft Docs'
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-code-analysis
ms.topic: reference
f1_keywords:
- CA1804
- RemoveUnusedLocals
helpviewer_keywords:
- RemoveUnusedLocals
- CA1804
ms.assetid: cc332e67-6543-4813-bd8a-6f6fc75bf22a
caps.latest.revision: 20
author: gewarren
ms.author: gewarren
manager: wpickett
ms.openlocfilehash: 38fe76bbdf2fdafa69ca12caf4f131a05f783954
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "68143125"
---
# <a name="ca1804-remove-unused-locals"></a>CA1804: Kullanılmayan yerelleri kaldırın
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

|||
|-|-|
|TypeName|RemoveUnusedLocals|
|CheckId|CA1804|
|Kategori|Microsoft.Performance|
|Yeni Değişiklik|Bölünemez|

## <a name="cause"></a>Sebep
 Bir yöntem bir yerel değişkeni bildirir ancak dışında değişkeni büyük olasılıkla Atama ifadesinin alıcı olarak kullanmaz. Bu kural tarafından analiz, test edilen derleme, hata ayıklama bilgileri ile oluşturulmalıdır ve ilişkili bir program veritabanı (.pdb) dosyası kullanılabilir olmalıdır.

## <a name="rule-description"></a>Kural Tanımı
 Kullanılmayan yerel değişkenler ve gereksiz atamaların derleme boyutunu artırır ve performansı düşürür.

## <a name="how-to-fix-violations"></a>İhlaller Nasıl Düzeltilir?
 Bu kural ihlalini düzeltmek için kaldırın veya yerel değişkenini kullanın. C# derleyicisi, birlikte unutmayın [!INCLUDE[dnprdnlong](../includes/dnprdnlong-md.md)] kullanılmayan yerel değişkenler kaldırır, `optimize` seçeneği etkinleştirilir.

## <a name="when-to-suppress-warnings"></a>Uyarılar Bastırıldığında
 Yayılan derleyici değişkeni ise bu kuraldan bir uyarıyı gizler. Performans ve kod bakımı birincil kaygıları değilse de bu kuraldan bir uyarıyı bastırmak için veya kuralı devre dışı bırakmak için güvenli değildir.

## <a name="example"></a>Örnek
 Aşağıdaki örnek, çeşitli kullanılmayan yerel değişkenler gösterir.

 [!code-csharp[FxCop.Performance.UnusedLocals#1](../snippets/csharp/VS_Snippets_CodeAnalysis/FxCop.Performance.UnusedLocals/cs/FxCop.Performance.UnusedLocals.cs#1)]
 [!code-vb[FxCop.Performance.UnusedLocals#1](../snippets/visualbasic/VS_Snippets_CodeAnalysis/FxCop.Performance.UnusedLocals/vb/FxCop.Performance.UnusedLocals.vb#1)]

## <a name="related-rules"></a>İlgili kuralları
 [CA1809: Aşırı yerel öğelerden Kaçın](../code-quality/ca1809-avoid-excessive-locals.md)

 [CA1811: Çağrılmayan özel kodlardan kaçının](../code-quality/ca1811-avoid-uncalled-private-code.md)

 [CA1812: Örneklenmemiş iç sınıflardan kaçının](../code-quality/ca1812-avoid-uninstantiated-internal-classes.md)

 [CA1801: Kullanılmayan parametreleri gözden geçir](../code-quality/ca1801-review-unused-parameters.md)

---
title: 'CA1804: Kullanılmayan yerelleri kaldırın'
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- CA1804
- RemoveUnusedLocals
helpviewer_keywords:
- RemoveUnusedLocals
- CA1804
ms.assetid: cc332e67-6543-4813-bd8a-6f6fc75bf22a
author: gewarren
ms.author: gewarren
manager: jillfra
dev_langs:
- CSharp
- VB
ms.workload:
- multiple
ms.openlocfilehash: 0a83d0afffc50c7697fad98c4dc49e31770d63d4
ms.sourcegitcommit: 0c2523d975d48926dd2b35bcd2d32a8ae14c06d8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/24/2019
ms.locfileid: "71233747"
---
# <a name="ca1804-remove-unused-locals"></a>CA1804: Kullanılmayan yerelleri kaldırın

|||
|-|-|
|TypeName|RemoveUnusedLocals|
|CheckId|CA1804|
|Kategori|Microsoft. Performance|
|Son değişiklik|Kırılmamış|

## <a name="cause"></a>Sebep
Bir yöntem yerel bir değişken bildirir, ancak muhtemelen bir atama ifadesinin alıcısı olarak bu değişkeni kullanmaz. Bu kurala göre analiz için, sınanan derleme hata ayıklama bilgileri ile oluşturulmalıdır ve ilişkili program veritabanı (. pdb) dosyası kullanılabilir olmalıdır.

## <a name="rule-description"></a>Kural açıklaması
Kullanılmayan yerel değişkenler ve gereksiz atamaların derleme boyutunu artırır ve performansı düşürür.

## <a name="how-to-fix-violations"></a>İhlalleri çözme

Bu kural ihlalini onarmak için yerel değişkeni kaldırın veya kullanın.

> [!NOTE]
> C# Derleyici, `optimize` seçeneği etkinken kullanılmayan yerel değişkenleri kaldırır.

## <a name="when-to-suppress-warnings"></a>Uyarıların ne zaman bastırılamıyor
Değişken derleyicinin yayıldıysa, bu kuraldan bir uyarı gizleyin. Bu kuraldan bir uyarıyı gizlemek veya performans ve kod Bakımı birincil endişeleriniz değilse kuralı devre dışı bırakmak de güvenlidir.

## <a name="example"></a>Örnek
Aşağıdaki örnek, kullanılmamış bazı yerel değişkenleri gösterir.

[!code-vb[FxCop.Performance.UnusedLocals#1](../code-quality/codesnippet/VisualBasic/ca1804-remove-unused-locals_1.vb)]
[!code-csharp[FxCop.Performance.UnusedLocals#1](../code-quality/codesnippet/CSharp/ca1804-remove-unused-locals_1.cs)]

## <a name="related-rules"></a>İlgili kurallar
[CA1809 Aşırı Yerellerden kaçının](../code-quality/ca1809-avoid-excessive-locals.md)

[CA1811 Çağrılmadı özel koddan kaçının](../code-quality/ca1811-avoid-uncalled-private-code.md)

[CA1812 Örneklenmemiş iç sınıflardan kaçının](../code-quality/ca1812-avoid-uninstantiated-internal-classes.md)

[CA1801 Kullanılmayan parametreleri gözden geçir](../code-quality/ca1801-review-unused-parameters.md)
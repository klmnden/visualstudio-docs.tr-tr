---
title: 'CA1806: Metot sonuçlarını yoksaymayın'
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- CA1806
- DoNotIgnoreMethodResults
helpviewer_keywords:
- CA1806
- DoNotIgnoreMethodResults
ms.assetid: fd805687-0817-481e-804e-b62cfb3b1076
author: gewarren
ms.author: gewarren
dev_langs:
- CPP
- CSharp
- VB
manager: jillfra
ms.openlocfilehash: d2a1dd9984601afa34e4aac7fa5ddc24061cf6ae
ms.sourcegitcommit: 21d667104199c2493accec20c2388cf674b195c3
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/08/2019
ms.locfileid: "55954511"
---
# <a name="ca1806-do-not-ignore-method-results"></a>CA1806: Metot sonuçlarını yoksaymayın

|||
|-|-|
|TypeName|DoNotIgnoreMethodResults|
|CheckId|CA1806|
|Kategori|Microsoft.Usage|
|Yeni Değişiklik|Bozucu olmayan|

## <a name="cause"></a>Sebep

Bu uyarı için birkaç olası nedeni vardır:

- Yeni bir nesne oluşturulur, ancak hiç kullanılmadı.

- Oluşturur ve yeni bir dize döndüren bir yöntem olarak adlandırılır ve yeni bir dize hiçbir zaman kullanılmaz.

- Bir HRESULT ya da hata kodunu döndüren bir COM veya P/Invoke yöntemi hiçbir zaman kullanılmaz. Kural Tanımı

Gereksiz nesne oluşturma ve kullanılmayan nesnenin ilişkili çöp toplama performansını düşürebilir.

Dizeleri sabittir ve yöntemleri String.ToUpper gibi bir dize yöntemi çağrılırken dizesinde örneğini değiştirmek yerine yeni bir örneğini döndürür.

HRESULT ya da hata kodu yoksayılıyor beklenmeyen davranışlara hata koşullarında ya da düşük kaynak koşulları yol açabilir.

## <a name="how-to-fix-violations"></a>İhlaller nasıl düzeltilir?
 Bir yöntemi hiçbir zaman kullanılmaz B nesnesinin yeni bir örneğini oluşturur, örneği bir bağımsız değişken olarak başka yönteme geçirin veya örneği bir değişkene atayın. Nesne oluşturma gereksizse kaldıramazsınız- veya -

 Yöntemi bir B yöntemini çağırır, ancak B yöntemi döndüren yeni dize örneğinde kullanmaz. Örneği bir bağımsız değişken olarak başka yönteme geçirin, örneği bir değişkene atayın. Ya da gereksizse çağrısını kaldırın.

 -veya-

 Yöntem, yöntem A B yöntemini çağırır, ancak HRESULT kullanmaz veya hata kodu döndürür. Sonucu bir koşullu deyimde kullanın, sonucu bir değişkene atayın ya da başka yönteme bağımsız değişken olarak geçirin.

## <a name="when-to-suppress-warnings"></a>Uyarılar bastırıldığında
 Nesne oluşturma işlemi bazı amaca hizmet eder sürece bu kuraldan bir uyarıyı bastırmayın.

## <a name="example"></a>Örnek
 Aşağıdaki örnek, çağıran String.Trim sonucunu yoksayar bir sınıfı gösterir.

 [!code-csharp[FxCop.Usage.DoNotIgnoreMethodResults3#1](../code-quality/codesnippet/CSharp/ca1806-do-not-ignore-method-results_1.cs)]
 [!code-vb[FxCop.Usage.DoNotIgnoreMethodResults3#1](../code-quality/codesnippet/VisualBasic/ca1806-do-not-ignore-method-results_1.vb)]
 [!code-cpp[FxCop.Usage.DoNotIgnoreMethodResults3#1](../code-quality/codesnippet/CPP/ca1806-do-not-ignore-method-results_1.cpp)]

## <a name="example"></a>Örnek
 Aşağıdaki örnek, önceki ihlali String.Trim sonucu geri çağrıldı değişken atanarak düzeltir.

 [!code-csharp[FxCop.Usage.DoNotIgnoreMethodResults4#1](../code-quality/codesnippet/CSharp/ca1806-do-not-ignore-method-results_2.cs)]
 [!code-vb[FxCop.Usage.DoNotIgnoreMethodResults4#1](../code-quality/codesnippet/VisualBasic/ca1806-do-not-ignore-method-results_2.vb)]
 [!code-cpp[FxCop.Usage.DoNotIgnoreMethodResults4#1](../code-quality/codesnippet/CPP/ca1806-do-not-ignore-method-results_2.cpp)]

## <a name="example"></a>Örnek
 Aşağıdaki örnek, oluşturduğu bir nesne kullanmayan bir yöntemi gösterir.

> [!NOTE]
> Visual Basic'te bu ihlal oluşturulamayacak.

 [!code-cpp[FxCop.Usage.DoNotIgnoreMethodResults5#1](../code-quality/codesnippet/CPP/ca1806-do-not-ignore-method-results_3.cpp)]
 [!code-csharp[FxCop.Usage.DoNotIgnoreMethodResults5#1](../code-quality/codesnippet/CSharp/ca1806-do-not-ignore-method-results_3.cs)]

## <a name="example"></a>Örnek
 Aşağıdaki örnek, bir nesne gereksiz oluşturulmasını kaldırarak önceki ihlali düzeltir.

 [!code-csharp[FxCop.Usage.DoNotIgnoreMethodResults6#1](../code-quality/codesnippet/CSharp/ca1806-do-not-ignore-method-results_4.cs)]
 [!code-cpp[FxCop.Usage.DoNotIgnoreMethodResults6#1](../code-quality/codesnippet/CPP/ca1806-do-not-ignore-method-results_4.cpp)]

<!-- Examples don't exist for the below... -->
<!--
## Example
 The following example shows a method that ignores the error code that the native method GetShortPathName returns.

## Example
 The following example fixes the previous violation by checking the error code and throwing an exception when the call fails.
-->
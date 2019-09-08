---
title: 'CA1821: Boş sonlandırıcıları kaldırın'
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- RemoveEmptyFinalizers
- CA1821
helpviewer_keywords:
- CA1821
ms.assetid: 3f4855a0-e4a0-46e6-923c-4c3b7074048d
author: gewarren
ms.author: gewarren
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: f616547738c7c58d61289b2be71c8e56a1a427c8
ms.sourcegitcommit: 0f44ec8ba0263056ad04d2d0dc904ad4206ce8fc
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/06/2019
ms.locfileid: "70766070"
---
# <a name="ca1821-remove-empty-finalizers"></a>CA1821: Boş sonlandırıcıları kaldırın

|||
|-|-|
|TypeName|Removeemptyfinalleyiciler|
|CheckId|CA1821|
|Kategori|Microsoft. Performance|
|Yeni Değişiklik|Kırılmamış|

## <a name="cause"></a>Sebep

Bir tür, boş bir Sonlandırıcı uygular, yalnızca temel tür sonlandırıcısını çağırır veya yalnızca koşullu olarak yayınlanan yöntemleri çağırır.

## <a name="rule-description"></a>Kural açıklaması

Her ne zaman, nesne ömrü izlenirken yer alan ek performans yükü nedeniyle sonlandırıcılardan kaçının. Çöp toplayıcı, nesneyi toplamadan önce sonlandırıcıyı çalıştırır. Bu, nesneyi toplamak için en az iki koleksiyonun gerekli olduğu anlamına gelir. Boş bir Sonlandırıcı bu ek yükü herhangi bir avantajsız olarak doğurur.

## <a name="how-to-fix-violations"></a>İhlalleri çözme

Boş sonlandırıcıyı kaldırın. Hata ayıklama için bir Sonlandırıcı gerekliyse, tüm sonlandırıcıyı `#if DEBUG / #endif` yönergelerden çevreden alın.

## <a name="when-to-suppress-warnings"></a>Uyarıların ne zaman bastırılamıyor

Bu kuraldan bir ileti bastırmayın.

## <a name="example"></a>Örnek

Aşağıdaki örnek, kaldırılması gereken boş bir Sonlandırıcı, `#if DEBUG / #endif` yönergeler içine alınması gereken sonlandırıcının ve `#if DEBUG / #endif` yönergeleri doğru bir şekilde kullanan sonlandırıcının gösterildiği gösterilmektedir.

[!code-csharp[FxCop.Performance.RemoveEmptyFinalizers#1](../code-quality/codesnippet/CSharp/ca1821-remove-empty-finalizers_1.cs)]

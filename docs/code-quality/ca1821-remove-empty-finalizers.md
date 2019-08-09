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
ms.openlocfilehash: 9c8c4d4ca04c7a9a21cd1e80e4dc06e8d5a92c2f
ms.sourcegitcommit: 5216c15e9f24d1d5db9ebe204ee0e7ad08705347
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/09/2019
ms.locfileid: "68921371"
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
Güncelleştirirken, nesne kullanım süresini izleme söz konusu olduğunda ek performans yükü nedeniyle sonlandırıcılardan kaçının. Çöp toplayıcı, nesneyi toplamadan önce sonlandırıcıyı çalıştırır. Bu, nesnenin toplanması için iki koleksiyonun gerekli olacağı anlamına gelir. Boş bir Sonlandırıcı bu ek yükü herhangi bir avantajsız olarak doğurur.

## <a name="how-to-fix-violations"></a>İhlalleri çözme
Boş sonlandırıcıyı kaldırın. Hata ayıklama için bir Sonlandırıcı gerekliyse, tüm sonlandırıcıyı `#if DEBUG / #endif` yönergelerden çevreden alın.

## <a name="when-to-suppress-warnings"></a>Uyarıların ne zaman bastırılamıyor
Bu kuraldan bir ileti bastırmayın. Sonlandırma performansı gizlenmemesi ve hiçbir avantaj sunamaması.

## <a name="example"></a>Örnek
Aşağıdaki örnek, kaldırılması gereken boş bir Sonlandırıcı, `#if DEBUG / #endif` yönergeler içine alınması gereken sonlandırıcının ve `#if DEBUG / #endif` yönergeleri doğru bir şekilde kullanan sonlandırıcının gösterildiği gösterilmektedir.

[!code-csharp[FxCop.Performance.RemoveEmptyFinalizers#1](../code-quality/codesnippet/CSharp/ca1821-remove-empty-finalizers_1.cs)]
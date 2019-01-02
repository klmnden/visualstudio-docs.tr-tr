---
title: 'CA1821: Boş Sonlandırıcıları kaldırın'
ms.date: 11/04/2016
ms.prod: visual-studio-dev15
ms.topic: reference
f1_keywords:
- RemoveEmptyFinalizers
- CA1821
helpviewer_keywords:
- CA1821
ms.assetid: 3f4855a0-e4a0-46e6-923c-4c3b7074048d
author: gewarren
ms.author: gewarren
manager: douge
ms.workload:
- multiple
ms.openlocfilehash: d155d8846828d8806fb4927d39120bfad2b01f33
ms.sourcegitcommit: 37fb7075b0a65d2add3b137a5230767aa3266c74
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/02/2019
ms.locfileid: "53937341"
---
# <a name="ca1821-remove-empty-finalizers"></a>CA1821: Boş Sonlandırıcıları kaldırın

|||
|-|-|
|TypeName|RemoveEmptyFinalizers|
|CheckId|CA1821|
|Kategori|Microsoft.Performance|
|Yeni Değişiklik|Bölünemez|

## <a name="cause"></a>Sebep
 Bir tür boş, yalnızca temel tür Sonlandırıcı çağırır veya yöntemleri koşullu olarak yayınlanan yalnızca çağıran sonlandırıcıyı uygular.

## <a name="rule-description"></a>Kural açıklaması
 Güncelleştirirken, nesne kullanım süresini izleme söz konusu olduğunda ek performans yükü nedeniyle sonlandırıcılardan kaçının. Nesne topladığı önce çöp toplayıcının sonlandırıcıyı çalışacak. Başka bir deyişle, iki koleksiyon nesnesi toplamak için gerekli olacaktır. Boş Sonlandırıcı eklenen yükü hiçbir avantajı bu artmasına neden olur.

## <a name="how-to-fix-violations"></a>İhlaller nasıl düzeltilir?
 Boş Sonlandırıcı kaldırın. Bir sonlandırıcı hata ayıklama için gereklidir, içindeki tüm Sonlandırıcı içine `#if DEBUG / #endif` yönergeleri.

## <a name="when-to-suppress-warnings"></a>Uyarılar bastırıldığında
 Bu kural bir iletiden bastırmayın. Sonlandırma bastırmak için hata performansınızın ve hiçbir avantaj sağlar.

## <a name="example"></a>Örnek
 Aşağıdaki örnek kaldırılacak boş Sonlandırıcı, içinde içine alınması bir sonlandırıcıyı gösterir `#if DEBUG / #endif` yönergeleriyle birlikte kullanan bir sonlandırıcı `#if DEBUG / #endif` yönergeleri doğru.

 [!code-csharp[FxCop.Performance.RemoveEmptyFinalizers#1](../code-quality/codesnippet/CSharp/ca1821-remove-empty-finalizers_1.cs)]
---
title: 'CA1821: Boş Sonlandırıcıları kaldırın | Microsoft Docs'
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-code-analysis
ms.topic: reference
f1_keywords:
- RemoveEmptyFinalizers
- CA1821
helpviewer_keywords:
- CA1821
ms.assetid: 3f4855a0-e4a0-46e6-923c-4c3b7074048d
caps.latest.revision: 15
author: gewarren
ms.author: gewarren
manager: wpickett
ms.openlocfilehash: 5a6175871e74bf3cb99610dce0926f0982f331d4
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "68201664"
---
# <a name="ca1821-remove-empty-finalizers"></a>CA1821: Boş sonlandırıcıları kaldırın
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

|||
|-|-|
|TypeName|RemoveEmptyFinalizers|
|CheckId|CA1821|
|Kategori|Microsoft.Performance|
|Yeni Değişiklik|Bölünemez|

## <a name="cause"></a>Sebep
 Bir tür boş, yalnızca temel tür Sonlandırıcı çağırır veya yöntemleri koşullu olarak yayınlanan yalnızca çağıran sonlandırıcıyı uygular.

## <a name="rule-description"></a>Kural Tanımı
 Güncelleştirirken, nesne kullanım süresini izleme söz konusu olduğunda ek performans yükü nedeniyle sonlandırıcılardan kaçının. Nesne topladığı önce çöp toplayıcının sonlandırıcıyı çalışacak. Başka bir deyişle, iki koleksiyon nesnesi toplamak için gerekli olacaktır. Boş Sonlandırıcı eklenen yükü hiçbir avantajı bu artmasına neden olur.

## <a name="how-to-fix-violations"></a>İhlaller Nasıl Düzeltilir?
 Boş Sonlandırıcı kaldırın. Bir sonlandırıcı hata ayıklama için gereklidir, içindeki tüm Sonlandırıcı içine `#if DEBUG / #endif` yönergeleri.

## <a name="when-to-suppress-warnings"></a>Uyarılar Bastırıldığında
 Bu kural bir iletiden bastırmayın. Sonlandırma bastırmak için hata performansınızın ve hiçbir avantaj sağlar.

## <a name="example"></a>Örnek
 Aşağıdaki örnek kaldırılacak boş Sonlandırıcı, içinde içine alınması bir sonlandırıcıyı gösterir `#if DEBUG / #endif` yönergeleriyle birlikte kullanan bir sonlandırıcı `#if DEBUG / #endif` yönergeleri doğru.

 [!code-csharp[FxCop.Performance.RemoveEmptyFinalizers#1](../snippets/csharp/VS_Snippets_CodeAnalysis/FxCop.Performance.RemoveEmptyFinalizers/cs/FxCop.Performance.RemoveEmptyFinalizers.cs#1)]

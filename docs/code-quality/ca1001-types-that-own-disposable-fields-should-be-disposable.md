---
title: 'CA1001: Atılabilir alanlara sahip türler atılabilir olmalıdır'
ms.date: 11/04/2016
ms.prod: visual-studio-dev15
ms.topic: reference
f1_keywords:
- CA1001
- TypesThatOwnDisposableFieldsShouldBeDisposable
helpviewer_keywords:
- CA1001
- TypesThatOwnDisposableFieldsShouldBeDisposable
ms.assetid: c85c126c-2b16-4505-940a-b5ddf873fb22
author: gewarren
ms.author: gewarren
manager: douge
dev_langs:
- CSharp
- VB
ms.workload:
- multiple
ms.openlocfilehash: d935d6310e9160cec222ef71933f23f1abf379cc
ms.sourcegitcommit: 37fb7075b0a65d2add3b137a5230767aa3266c74
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/02/2019
ms.locfileid: "53908833"
---
# <a name="ca1001-types-that-own-disposable-fields-should-be-disposable"></a>CA1001: Atılabilir alanlara sahip türler atılabilir olmalıdır

|||
|-|-|
|TypeName|TypesThatOwnDisposableFieldsShouldBeDisposable|
|CheckId|CA1001|
|Kategori|Microsoft.Design|
|Yeni Değişiklik|Bölünemez - türü derlemenin dışında görünür değilse.<br /><br /> Derlemenin dışında görünür bir tür ise - kesiliyor.|

## <a name="cause"></a>Sebep
 Bir sınıfı bildirir ve bir örnek alan uygulayan bir <xref:System.IDisposable?displayProperty=fullName> türü ve sınıf uygulamıyor <xref:System.IDisposable>.

## <a name="rule-description"></a>Kural açıklaması
 Arabirimini uygulayan bir sınıf <xref:System.IDisposable> sahip olduğu yönetilmeyen kaynaklarını silmek için arabirim. Bir örnek alan bir <xref:System.IDisposable> türü, alan bir yönetilmeyen kaynağa sahip olduğunu gösterir. Bildiren bir sınıf bir <xref:System.IDisposable> alan dolaylı olarak bir yönetilmeyen kaynağa sahip ve uygulamalıdır <xref:System.IDisposable> arabirimi. Sınıf doğrudan herhangi bir yönetilmeyen kaynağa sahip değilse, bir sonlandırıcı uygulamamalıdır.

## <a name="how-to-fix-violations"></a>İhlaller nasıl düzeltilir?
 Bu kural ihlalini düzeltmek için uygulama <xref:System.IDisposable> ve <xref:System.IDisposable.Dispose%2A?displayProperty=fullName> yöntem çağrısının <xref:System.IDisposable.Dispose%2A> alan yöntemi.

## <a name="when-to-suppress-warnings"></a>Uyarılar bastırıldığında
 Bu kuraldan uyarıyı bastırmayın.

## <a name="example"></a>Örnek
 Aşağıdaki örnek, kuralını ihlal eden bir sınıf ve kural uygulayarak karşılayan bir sınıfı gösterir <xref:System.IDisposable>. Sınıf doğrudan herhangi bir yönetilmeyen kaynağa sahibi değildir çünkü sınıfı bir sonlandırıcı uygulamıyor.

 [!code-vb[FxCop.Design.DisposableFields#1](../code-quality/codesnippet/VisualBasic/ca1001-types-that-own-disposable-fields-should-be-disposable_1.vb)]
 [!code-csharp[FxCop.Design.DisposableFields#1](../code-quality/codesnippet/CSharp/ca1001-types-that-own-disposable-fields-should-be-disposable_1.cs)]

## <a name="related-rules"></a>İlgili kuralları
 [CA2213: Atılabilen alanlar atılmalıdır](../code-quality/ca2213-disposable-fields-should-be-disposed.md)

 [CA2216: Atılabilir türler sonlandırıcıyı bildirmelidir](../code-quality/ca2216-disposable-types-should-declare-finalizer.md)

 [CA2215: Atma yöntemleri taban sınıf atmayı çağırmalıdır](../code-quality/ca2215-dispose-methods-should-call-base-class-dispose.md)

 [CA1049: Yerel kaynaklara sahip türler atılabilir olmalıdır](../code-quality/ca1049-types-that-own-native-resources-should-be-disposable.md)
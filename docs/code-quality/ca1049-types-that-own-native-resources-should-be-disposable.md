---
title: 'CA1049: Yerel kaynaklara sahip türler atılabilir olmalıdır'
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- CA1049
- TypesThatOwnNativeResourcesShouldBeDisposable
helpviewer_keywords:
- TypesThatOwnNativeResourcesShouldBeDisposable
- CA1049
ms.assetid: 084e587d-0e45-4092-b767-49eed30d6a35
author: gewarren
ms.author: gewarren
manager: jillfra
dev_langs:
- CSharp
- VB
ms.workload:
- cplusplus
ms.openlocfilehash: ef7b72eade7ea8e4486d5c317c06026bb4d0b95f
ms.sourcegitcommit: 0c2523d975d48926dd2b35bcd2d32a8ae14c06d8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/24/2019
ms.locfileid: "71235738"
---
# <a name="ca1049-types-that-own-native-resources-should-be-disposable"></a>CA1049: Yerel kaynaklara sahip türler atılabilir olmalıdır

|||
|-|-|
|TypeName|TypesThatOwnNativeResourcesShouldBeDisposable|
|CheckId|CA1049|
|Kategori|Microsoft.Design|
|Son değişiklik|Kırılmamış|

## <a name="cause"></a>Sebep

Bir tür bir <xref:System.IntPtr?displayProperty=fullName> alana <xref:System.UIntPtr?displayProperty=fullName> , alana veya <xref:System.Runtime.InteropServices.HandleRef?displayProperty=fullName> alana başvurur, ancak uygulamaz <xref:System.IDisposable?displayProperty=fullName>.

## <a name="rule-description"></a>Kural açıklaması

Bu kural <xref:System.IntPtr>, <xref:System.UIntPtr>ve <xref:System.Runtime.InteropServices.HandleRef> alanlarının yönetilmeyen kaynaklara işaretçiler depodığını varsayar. Yönetilmeyen kaynakları ayıran türler, arayanların <xref:System.IDisposable> bu kaynakları talep üzerine serbest bırakmasına ve kaynakları tutan nesnelerin yaşam sürelerini kısaltmasına imkan sağlamak için uygulamalıdır.

Yönetilmeyen kaynakları temizlemek için önerilen tasarım deseninin, sırasıyla <xref:System.Object.Finalize%2A?displayProperty=fullName> yöntemi <xref:System.IDisposable.Dispose%2A?displayProperty=fullName> ve yöntemi kullanılarak bu kaynakları serbest bırakmak için hem örtük hem de açık bir yol sağlamaktır. Çöp toplayıcı, nesnenin artık <xref:System.Object.Finalize%2A> erişilebilir olmadığı belirlendikten sonra bir nesnenin yöntemini belirsiz bir zamanda çağırır. Çağrıldıktan <xref:System.Object.Finalize%2A> sonra, nesneyi serbest bırakmak için ek bir atık toplama gerekir. <xref:System.IDisposable.Dispose%2A> Yöntemi, çağıranın kaynak atık toplayıcıya ayrıldıysa, kaynakların önceden açık şekilde kaynak serbest bırakıldığını sağlar. Yönetilmeyen kaynakları <xref:System.IDisposable.Dispose%2A> temizledikten sonra çöp toplayıcısının <xref:System.Object.Finalize%2A> artık çağrılmamasına izin vermek için <xref:System.GC.SuppressFinalize%2A?displayProperty=fullName> yöntemini çağırmalıdır; bu, ek çöp toplama gereksinimini ortadan kaldırır ve nesnenin yaşam süresi.

## <a name="how-to-fix-violations"></a>İhlalleri çözme
Bu kural ihlalini onarmak için uygulamasını uygulayın <xref:System.IDisposable>.

## <a name="when-to-suppress-warnings"></a>Uyarıların ne zaman bastırılamıyor
Tür yönetilmeyen bir kaynağa başvurmadığından, bu kuraldan bir uyarının bastırmasının güvenli hale gelir. Aksi takdirde, uygulama <xref:System.IDisposable> hatası yönetilmeyen kaynakların kullanılamaz hale gelmesine veya az kullanılmamasına neden olabileceğinden, bu kuraldan bir uyarıyı bastırmayın.

## <a name="example"></a>Örnek
Aşağıdaki örnek, yönetilmeyen bir kaynağı temizlemek için <xref:System.IDisposable> uygulayan bir türü gösterir.

[!code-csharp[FxCop.Design.UnmanagedResources#1](../code-quality/codesnippet/CSharp/ca1049-types-that-own-native-resources-should-be-disposable_1.cs)]
[!code-vb[FxCop.Design.UnmanagedResources#1](../code-quality/codesnippet/VisualBasic/ca1049-types-that-own-native-resources-should-be-disposable_1.vb)]

## <a name="related-rules"></a>İlgili kurallar
[CA2115 GC 'yi çağırın. Yerel kaynaklar kullanılırken KeepAlive](../code-quality/ca2115-call-gc-keepalive-when-using-native-resources.md)

[CA1816 GC 'yi çağırın. SuppressFinalize doğru](../code-quality/ca1816-call-gc-suppressfinalize-correctly.md)

[CA2216 Atılabilir türler sonlandırıcıyı bildirmelidir](../code-quality/ca2216-disposable-types-should-declare-finalizer.md)

[CA1001 Atılabilir alanlarının sahibi olan türler atılabilir olmalıdır](../code-quality/ca1001-types-that-own-disposable-fields-should-be-disposable.md)

## <a name="see-also"></a>Ayrıca bkz.

- [Yönetilmeyen Kaynakları Temizleme](/dotnet/standard/garbage-collection/unmanaged)
- [Dispose Deseni](/dotnet/standard/design-guidelines/dispose-pattern)
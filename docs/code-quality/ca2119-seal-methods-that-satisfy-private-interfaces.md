---
title: 'CA2119: Özel arabirimleri karşılayan metotları mühürleyin'
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- SealMethodsThatSatisfyPrivateInterfaces
- CA2119
helpviewer_keywords:
- CA2119
- SealMethodsThatSatisfyPrivateInterfaces
ms.assetid: 483d02e1-cfaf-4754-a98f-4116df0f3509
author: gewarren
ms.author: gewarren
manager: jillfra
dev_langs:
- CPP
- CSharp
- VB
ms.workload:
- multiple
ms.openlocfilehash: 4c019e98e7f1311b6521dff563cb8e7bb0a2356e
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62544035"
---
# <a name="ca2119-seal-methods-that-satisfy-private-interfaces"></a>CA2119: Özel arabirimleri karşılayan metotları mühürleyin

|||
|-|-|
|TypeName|SealMethodsThatSatisfyPrivateInterfaces|
|CheckId|CA2119|
|Kategori|Microsoft.Security|
|Yeni Değişiklik|Yeni|

## <a name="cause"></a>Sebep
 Devralınabilir bir ortak tür, geçersiz yöntem uygulamasını sağlar. bir `internal` (`Friend` Visual Basic'te) arabirimi.

## <a name="rule-description"></a>Kural açıklaması
 Uygulama türü değiştirilemez ortak erişilebilirlik arabirim yöntemleri vardır. Bir iç arabiriminde arabirimi tanımlayan derlemenin dışından uygulanmak üzere tasarlanmamıştır bir anlaşma oluşturur. Bir yöntem kullanarak bir iç arabirimi uygulayan bir genel türü `virtual` (`Overridable` Visual Basic) değiştirici yöntemin, derlemenin dışından türetilmiş bir tür tarafından geçersiz kılınmasını sağlar. İkinci bir derlemenin türü yöntemini çağırır ve yalnızca dahili bir sözleşme bekliyor, bunun yerine bir dış derlemede geçersiz kılınan yöntemi yürütüldüğünde davranışını tehlikeye. Bu bir güvenlik açığı oluşturur.

## <a name="how-to-fix-violations"></a>İhlaller nasıl düzeltilir?
 Bu kural ihlalini düzeltmek için yöntemin derlemenin dışından aşağıdakilerden birini kullanarak geçersiz kılınmasını önleyin:

- Bildirim türü olun `sealed` (`NotInheritable` Visual Basic'te).

- Bildirim türü için erişilebilirliğini `internal` (`Friend` Visual Basic'te).

- Tüm public oluşturucuları bildirim türünden kaldırın.

- Kullanmadan yöntemi uygulamak `virtual` değiştiricisi.

- Yöntemi açıkça uygulayın.

## <a name="when-to-suppress-warnings"></a>Uyarılar bastırıldığında
 Bu bir uyarıyı bastırmak güvenlidir inceledikten sonra hiçbir güvenlik sorunu varsa, kural, derlemenin dışından yöntemi geçersiz kılınırsa açıklardan olabilir.

## <a name="example-1"></a>Örnek 1
 Aşağıdaki örnek, bir tür gösterir `BaseImplementation`, bu kuralı ihlal ediyor.

 [!code-cpp[FxCop.Security.SealMethods1#1](../code-quality/codesnippet/CPP/ca2119-seal-methods-that-satisfy-private-interfaces_1.cpp)]
 [!code-csharp[FxCop.Security.SealMethods1#1](../code-quality/codesnippet/CSharp/ca2119-seal-methods-that-satisfy-private-interfaces_1.cs)]
 [!code-vb[FxCop.Security.SealMethods1#1](../code-quality/codesnippet/VisualBasic/ca2119-seal-methods-that-satisfy-private-interfaces_1.vb)]

## <a name="example-2"></a>Örnek 2
 Aşağıdaki örnek, önceki örnekte sanal yöntem uygulaması yararlanan.

 [!code-cpp[FxCop.Security.SealMethods2#1](../code-quality/codesnippet/CPP/ca2119-seal-methods-that-satisfy-private-interfaces_2.cpp)]
 [!code-csharp[FxCop.Security.SealMethods2#1](../code-quality/codesnippet/CSharp/ca2119-seal-methods-that-satisfy-private-interfaces_2.cs)]
 [!code-vb[FxCop.Security.SealMethods2#1](../code-quality/codesnippet/VisualBasic/ca2119-seal-methods-that-satisfy-private-interfaces_2.vb)]

## <a name="see-also"></a>Ayrıca bkz.

- [Arabirimler](/dotnet/csharp/programming-guide/interfaces/index)
- [Arabirimler](/dotnet/visual-basic/programming-guide/language-features/interfaces/index)
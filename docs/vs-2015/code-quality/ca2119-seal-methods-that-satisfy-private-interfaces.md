---
title: 'CA2119: Özel arabirimleri karşılayan yöntemleri mühürleyin | Microsoft Docs'
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-code-analysis
ms.topic: reference
f1_keywords:
- SealMethodsThatSatisfyPrivateInterfaces
- CA2119
helpviewer_keywords:
- CA2119
- SealMethodsThatSatisfyPrivateInterfaces
ms.assetid: 483d02e1-cfaf-4754-a98f-4116df0f3509
caps.latest.revision: 20
author: gewarren
ms.author: gewarren
manager: wpickett
ms.openlocfilehash: 56b08d1b842e65e1c1c29a7409813c314cbf014d
ms.sourcegitcommit: 08fc78516f1107b83f46e2401888df4868bb1e40
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/15/2019
ms.locfileid: "65687272"
---
# <a name="ca2119-seal-methods-that-satisfy-private-interfaces"></a>CA2119: Özel arabirimleri karşılayan metotları mühürleyin
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

|||
|-|-|
|TypeName|SealMethodsThatSatisfyPrivateInterfaces|
|CheckId|CA2119|
|Kategori|Microsoft.Security|
|Yeni Değişiklik|Yeni|

## <a name="cause"></a>Sebep
 Devralınabilir bir ortak tür, geçersiz yöntem uygulamasını sağlar. bir `internal` (`Friend` Visual Basic'te) arabirimi.

## <a name="rule-description"></a>Kural Tanımı
 Uygulama türü değiştirilemez ortak erişilebilirlik arabirim yöntemleri vardır. Bir iç arabiriminde arabirimi tanımlayan derlemenin dışından uygulanmak üzere tasarlanmamıştır bir anlaşma oluşturur. Bir yöntem kullanarak bir iç arabirimi uygulayan bir genel türü `virtual` (`Overridable` Visual Basic) değiştirici yöntemin, derlemenin dışından türetilmiş bir tür tarafından geçersiz kılınmasını sağlar. İkinci bir derlemenin türü yöntemini çağırır ve yalnızca dahili bir sözleşme bekliyor, bunun yerine bir dış derlemede geçersiz kılınan yöntemi yürütüldüğünde davranışını tehlikeye. Bu bir güvenlik açığı oluşturur.

## <a name="how-to-fix-violations"></a>İhlaller Nasıl Düzeltilir?
 Bu kural ihlalini düzeltmek için yöntemin derlemenin dışından aşağıdakilerden birini kullanarak geçersiz kılınmasını önleyin:

- Bildirim türü olun `sealed` (`NotInheritable` Visual Basic'te).

- Bildirim türü için erişilebilirliğini `internal` (`Friend` Visual Basic'te).

- Tüm public oluşturucuları bildirim türünden kaldırın.

- Kullanmadan yöntemi uygulamak `virtual` değiştiricisi.

- Yöntemi açıkça uygulayın.

## <a name="when-to-suppress-warnings"></a>Uyarılar Bastırıldığında
 Bu bir uyarıyı bastırmak güvenlidir inceledikten sonra hiçbir güvenlik sorunu varsa, kural, derlemenin dışından yöntemi geçersiz kılınırsa açıklardan olabilir.

## <a name="example"></a>Örnek
 Aşağıdaki örnek, bir tür gösterir `BaseImplementation`, bu kuralı ihlal ediyor.

 [!code-cpp[FxCop.Security.SealMethods1#1](../snippets/cpp/VS_Snippets_CodeAnalysis/FxCop.Security.SealMethods1/cpp/FxCop.Security.SealMethods1.cpp#1)]
 [!code-csharp[FxCop.Security.SealMethods1#1](../snippets/csharp/VS_Snippets_CodeAnalysis/FxCop.Security.SealMethods1/cs/FxCop.Security.SealMethods1.cs#1)]
 [!code-vb[FxCop.Security.SealMethods1#1](../snippets/visualbasic/VS_Snippets_CodeAnalysis/FxCop.Security.SealMethods1/vb/FxCop.Security.SealMethods1.vb#1)]

## <a name="example"></a>Örnek
 Aşağıdaki örnek, önceki örnekte sanal yöntem uygulaması yararlanan.

 [!code-cpp[FxCop.Security.SealMethods2#1](../snippets/cpp/VS_Snippets_CodeAnalysis/FxCop.Security.SealMethods2/cpp/FxCop.Security.SealMethods2.cpp#1)]
 [!code-csharp[FxCop.Security.SealMethods2#1](../snippets/csharp/VS_Snippets_CodeAnalysis/FxCop.Security.SealMethods2/cs/FxCop.Security.SealMethods2.cs#1)]
 [!code-vb[FxCop.Security.SealMethods2#1](../snippets/visualbasic/VS_Snippets_CodeAnalysis/FxCop.Security.SealMethods2/vb/FxCop.Security.SealMethods2.vb#1)]

## <a name="see-also"></a>Ayrıca Bkz.
 [Arabirimleri](https://msdn.microsoft.com/library/2feda177-ce11-432d-81b4-d50f5f35fd37) [arabirimleri](https://msdn.microsoft.com/library/61b06674-12c9-430b-be68-cc67ecee1f5b)

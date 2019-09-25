---
title: 'CA2102: CLSCompliant olmayan özel durumları genel işleyiciler içinde yakalayın'
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- CA2102
- CatchNonClsCompliantExceptionsInGeneralHandlers
helpviewer_keywords:
- CA2102
ms.assetid: bf2df68f-d386-4379-ad9e-930a2c2e930d
author: gewarren
ms.author: gewarren
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: f62ad97bbb96f49a7263edd29f0f8a7c263bec4c
ms.sourcegitcommit: 0c2523d975d48926dd2b35bcd2d32a8ae14c06d8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/24/2019
ms.locfileid: "71233004"
---
# <a name="ca2102-catch-non-clscompliant-exceptions-in-general-handlers"></a>CA2102: CLSCompliant olmayan özel durumları genel işleyiciler içinde yakalayın

|||
|-|-|
|TypeName|CatchNonClsCompliantExceptionsInGeneralHandlers|
|CheckId|CA2102|
|Kategori|Microsoft.Security|
|Son değişiklik|Kırılmamış|

## <a name="cause"></a>Sebep

Ya <xref:System.Runtime.CompilerServices.RuntimeCompatibilityAttribute> daile<xref:System.Exception?displayProperty=fullName> işaretlenmemiş bir derlemedeki üye, hemen aşağıdaki genel catch bloğunu işleyen ve içermeyen bir catch bloğu içerir.`RuntimeCompatibility(WrapNonExceptionThrows = false)` Bu kural derlemeleri [!INCLUDE[vbprvb](../code-quality/includes/vbprvb_md.md)] yoksayar.

## <a name="rule-description"></a>Kural açıklaması

Tüm ortak dil belirtimi ( <xref:System.Exception> CLS) uyumlu özel durumlarını yakalayan bir catch bloğu. Ancak, CLS uyumlu olmayan özel durumları yakalamaz. CLS uyumlu olmayan özel durumlar yerel koddan veya Microsoft ara dili (MSIL) derleyicisi tarafından oluşturulan yönetilen koddan oluşturulabilir. C# Ve[!INCLUDE[vbprvb](../code-quality/includes/vbprvb_md.md)] derleyicilerin CLS uyumlu olmayan özel durumların atılamayacağını ve [!INCLUDE[vbprvb](../code-quality/includes/vbprvb_md.md)] CLS uyumlu olmayan özel durumları yakalamayacağını unutmayın. Catch bloğunun amacı tüm özel durumları işlemek ise, aşağıdaki genel catch bloğu sözdizimini kullanın.

- C#:`catch {}`

- C++: `catch(...) {}` veya`catch(Object^) {}`

İşlenmemiş CLS uyumlu olmayan bir özel durum, önceden izin verilen izinler catch bloğunda kaldırıldığında bir güvenlik sorunu haline gelir. CLS uyumlu olmayan özel durumlar yakalanmadığı için, CLS uyumlu olmayan bir özel durum oluşturan kötü niyetli bir yöntem yükseltilmiş izinlerle çalıştırılabilir.

## <a name="how-to-fix-violations"></a>İhlalleri çözme

Amaç tüm özel durumları yakalamada, genel bir catch bloğu yerine koymak veya eklemek ya da derlemeyi `RuntimeCompatibility(WrapNonExceptionThrows = true)`işaretlemek için bu kural ihlalini onarmak için. İzinler catch bloğunda kaldırılırsa, genel catch bloğundaki işlevselliği çoğaltın. Tüm özel durumları işleme amacı değilse, özel özel durum türlerini işleyen catch bloklarıyla işleyen <xref:System.Exception> catch bloğunu değiştirin.

## <a name="when-to-suppress-warnings"></a>Uyarıların ne zaman bastırılamıyor

Try bloğu CLS uyumlu olmayan bir özel durum oluşturabilen deyimler içermiyorsa, bu kuraldan bir uyarıyı gizlemek güvenlidir. Herhangi bir yerel veya yönetilen kod CLS uyumlu olmayan bir özel durum oluşturabileceğinden, bu, try bloğu içindeki tüm kod yollarında yürütülebilecek tüm kodlar için bilgi gerektirir. CLS uyumlu olmayan özel durumların ortak dil çalışma zamanı tarafından oluşturulduğuna dikkat edin.

## <a name="example-1"></a>Örnek 1

Aşağıdaki örnekte, CLS uyumlu olmayan bir özel durum oluşturan bir MSIL sınıfı gösterilmektedir.

```cpp
.assembly ThrowNonClsCompliantException {}
.class public auto ansi beforefieldinit ThrowsExceptions
{
   .method public hidebysig static void
         ThrowNonClsException() cil managed
   {
      .maxstack  1
      IL_0000:  newobj     instance void [mscorlib]System.Object::.ctor()
      IL_0005:  throw
   }
}
```

## <a name="example-2"></a>Örnek 2

Aşağıdaki örnek, kuralını karşılayan genel bir catch bloğunu içeren bir yöntemi gösterir.

[!code-csharp[FxCop.Security.CatchNonClsCompliantException#1](../code-quality/codesnippet/CSharp/ca2102-catch-non-clscompliant-exceptions-in-general-handlers_1.cs)]

Önceki örnekleri aşağıdaki şekilde derleyin.

```cpp
ilasm /dll ThrowNonClsCompliantException.il
csc /r:ThrowNonClsCompliantException.dll CatchNonClsCompliantException.cs
```

## <a name="related-rules"></a>İlgili kurallar

[CA1031 Genel özel durum türlerini yakalamayın](../code-quality/ca1031-do-not-catch-general-exception-types.md)

## <a name="see-also"></a>Ayrıca bkz.

- [Özel Durumlar ve Özel Durum İşleme](/dotnet/csharp/programming-guide/exceptions/exceptions-and-exception-handling)
- [Ilasm.exe (IL Derleyici)](/dotnet/framework/tools/ilasm-exe-il-assembler)
- [Dil Bağımsızlığı ve Dilden Bağımsız Bileşenler](/dotnet/standard/language-independence-and-language-independent-components)
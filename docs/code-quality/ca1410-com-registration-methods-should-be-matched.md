---
title: 'CA1410: COM kayıt metotları eşleşmelidir'
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- CA1410
- ComRegistrationMethodsShouldBeMatched
helpviewer_keywords:
- CA1410
- ComRegistrationMethodsShouldBeMatched
ms.assetid: f3b2e62d-fd66-4093-9f0c-dba01ad995fd
author: gewarren
ms.author: gewarren
manager: jillfra
dev_langs:
- CSharp
- VB
ms.workload:
- multiple
ms.openlocfilehash: c606a55be00ac8e44d54bad289076498e2655af1
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62546420"
---
# <a name="ca1410-com-registration-methods-should-be-matched"></a>CA1410: COM kayıt metotları eşleşmelidir

|||
|-|-|
|TypeName|ComRegistrationMethodsShouldBeMatched|
|CheckId|CA1410|
|Kategori|Microsoft.Interoperability|
|Yeni Değişiklik|Bölünemez|

## <a name="cause"></a>Sebep
 İle işaretlenmiş bir yöntem bir tür bildirir <xref:System.Runtime.InteropServices.ComRegisterFunctionAttribute?displayProperty=fullName> özniteliği ancak ile işaretlenmiş bir yöntemi bildirmez <xref:System.Runtime.InteropServices.ComUnregisterFunctionAttribute?displayProperty=fullName> özniteliği, ya da tam tersi.

## <a name="rule-description"></a>Kural açıklaması
 Bileşen Nesne Modeli (COM) istemcilerin bir .NET Framework türü oluşturmak için türü önce kayıtlı olması gerekir. Varsa, ile işaretlenmiş bir yöntemi <xref:System.Runtime.InteropServices.ComRegisterFunctionAttribute> özniteliği, kullanıcı tarafından belirtilen kodu çalıştırmak için kayıt işlemi sırasında çağrılır. Karşılık gelen ile işaretlenmiş bir yöntemi <xref:System.Runtime.InteropServices.ComUnregisterFunctionAttribute> özniteliği, kayıt yöntemini işlemleri tersine çevirmek için kayıt silme işlemi sırasında çağrılır.

## <a name="how-to-fix-violations"></a>İhlaller nasıl düzeltilir?
 Bu kural ihlalini düzeltmek için karşılık gelen bir kayıt veya silme yöntemi ekleyin.

## <a name="when-to-suppress-warnings"></a>Uyarılar bastırıldığında
 Bu kuraldan uyarıyı bastırmayın.

## <a name="example"></a>Örnek
 Aşağıdaki örnek kuralını ihlal eden bir tür gösterir. Açıklamalı kod düzeltme ihlali gösterir.

 [!code-csharp[FxCop.Interoperability.ComRegistration#1](../code-quality/codesnippet/CSharp/ca1410-com-registration-methods-should-be-matched_1.cs)]
 [!code-vb[FxCop.Interoperability.ComRegistration#1](../code-quality/codesnippet/VisualBasic/ca1410-com-registration-methods-should-be-matched_1.vb)]

## <a name="related-rules"></a>İlgili kuralları
 [CA1411: COM kayıt yöntemleri görünebilir olmamalıdır](../code-quality/ca1411-com-registration-methods-should-not-be-visible.md)

## <a name="see-also"></a>Ayrıca bkz.

- <xref:System.Runtime.InteropServices.RegistrationServices?displayProperty=fullName>
- [Bütünleştirilmiş Kodları COM ile Kaydetme](/dotnet/framework/interop/registering-assemblies-with-com)
- [Regasm.exe (Derleme Kayıt Aracı)](/dotnet/framework/tools/regasm-exe-assembly-registration-tool)
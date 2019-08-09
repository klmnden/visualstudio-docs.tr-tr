---
title: 'CA1400: P-Invoke giriş noktaları bulunmalıdır'
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- CA1400
- PInvokeEntryPointsShouldExist
helpviewer_keywords:
- PInvokeEntryPointsShouldExist
- CA1400
ms.assetid: 1d64e470-7b2f-4cca-8fb0-ac92829e6332
author: gewarren
ms.author: gewarren
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: b292c58e666c11130fb25f67c234bfd2282fe463
ms.sourcegitcommit: 5216c15e9f24d1d5db9ebe204ee0e7ad08705347
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/09/2019
ms.locfileid: "68922251"
---
# <a name="ca1400-pinvoke-entry-points-should-exist"></a>CA1400: P/Invoke giriş noktaları bulunmalıdır

|||
|-|-|
|TypeName|PInvokeEntryPointsShouldExist|
|CheckId|CA1400|
|Kategori|Microsoft. çalışabilirliği|
|Yeni Değişiklik|Kırılmamış|

## <a name="cause"></a>Sebep
Ortak veya korumalı bir yöntem ile <xref:System.Runtime.InteropServices.DllImportAttribute?displayProperty=fullName>işaretlenir. Yönetilmeyen kitaplık bulunamadı ya da yöntem için bir işlev kitaplığında eşleştirilemedi. Kural, yöntem adını tam olarak belirtilen şekilde bulamazsa, yöntem adını ' A ' veya ' W ' ile birlikte düzelterek metodun ANSI veya geniş karakterli sürümlerini arar. Eşleşme bulunmazsa, kural __stdcall ad biçimini kullanarak bir işlevi bulmaya çalışır (_MyMethod@12burada, 12 bağımsız değişkenlerin uzunluğunu temsil eder). Eşleşme bulunmazsa ve Yöntem adı ' # ' ile başlıyorsa, kural, işlevi bir ad başvurusu yerine bir sıralı başvuru olarak arar.

## <a name="rule-description"></a>Kural açıklaması
İle <xref:System.Runtime.InteropServices.DllImportAttribute> işaretlenen yöntemlerin başvurulan yönetilmeyen DLL 'de bulunduğundan emin olmak için derleme zamanı denetimi kullanılamaz. Kitaplıkta belirtilen ada sahip hiçbir işlev yoksa veya metodun bağımsız değişkenleri işlev bağımsız değişkenleriyle eşleşmezse, ortak dil çalışma zamanı bir özel durum oluşturur.

## <a name="how-to-fix-violations"></a>İhlalleri çözme
Bu kural ihlalini düzeltmek için <xref:System.Runtime.InteropServices.DllImportAttribute> özniteliğine sahip olan yöntemi düzeltin. Yönetilmeyen kitaplığın var olduğundan ve yöntemi içeren derlemeyle aynı dizinde olduğundan emin olun. Kitaplık varsa ve doğru şekilde başvuruluyorsa, yöntem adı, dönüş türü ve bağımsız değişken imzasının kitaplık işleviyle eşleştiğinden emin olun.

## <a name="when-to-suppress-warnings"></a>Uyarıların ne zaman bastırılamıyor
Yönetilmeyen kitaplık, kendisine başvuran yönetilen derlemeyle aynı dizinde olduğunda, bu kuraldan bir uyarıyı bastırmayın. Yönetilmeyen kitaplığın yer aldığı durumlarda bu kuraldan bir uyarıyı gizlemek güvenli olabilir.

## <a name="example"></a>Örnek
Aşağıdaki örnek, kuralı ihlal eden bir türü gösterir. Kernel32. dll içinde adlı `DoSomethingUnmanaged` hiçbir işlev oluşmaz.

[!code-csharp[FxCop.Interoperability.DLLExists#1](../code-quality/codesnippet/CSharp/ca1400-p-invoke-entry-points-should-exist_1.cs)]

## <a name="see-also"></a>Ayrıca bkz.
 <xref:System.Runtime.InteropServices.DllImportAttribute?displayProperty=fullName>
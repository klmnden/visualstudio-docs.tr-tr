---
title: 'CA1411: COM kayıt yöntemleri görünebilir olmamalıdır | Microsoft Docs'
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-code-analysis
ms.topic: reference
f1_keywords:
- CA1411
- ComRegistrationMethodsShouldNotBeVisible
helpviewer_keywords:
- ComRegistrationMethodsShouldNotBeVisible
- CA1411
ms.assetid: a59f96f1-1f38-4596-b656-947df5c55311
caps.latest.revision: 15
author: gewarren
ms.author: gewarren
manager: wpickett
ms.openlocfilehash: 2d7bcaf5637be70174a3a337343d92b7b3705b46
ms.sourcegitcommit: 08fc78516f1107b83f46e2401888df4868bb1e40
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/15/2019
ms.locfileid: "65692038"
---
# <a name="ca1411-com-registration-methods-should-not-be-visible"></a>CA1411: COM kayıt metotları görünebilir olmamalıdır
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

|||
|-|-|
|TypeName|ComRegistrationMethodsShouldNotBeVisible|
|CheckId|CA1411|
|Kategori|Microsoft.Interoperability|
|Yeni Değişiklik|Yeni|

## <a name="cause"></a>Sebep
 İle işaretlenmiş bir yöntemi <xref:System.Runtime.InteropServices.ComRegisterFunctionAttribute?displayProperty=fullName> veya <xref:System.Runtime.InteropServices.ComUnregisterFunctionAttribute?displayProperty=fullName> özniteliktir dışarıdan görünür.

## <a name="rule-description"></a>Kural Tanımı
 Bir derlemeyi Bileşen Nesne Modeli (COM) ile kaydettiğinizde, kayıt defterine her derlemenin COM görünür türü için girişler eklenir. İle işaretlenmiş yöntemler <xref:System.Runtime.InteropServices.ComRegisterFunctionAttribute> ve <xref:System.Runtime.InteropServices.ComUnregisterFunctionAttribute> öznitelikleri kayıt ve kayıt silme işlemleri sırasında sırasıyla kaydolmayı/kaydı kaldırmayı için bu tür özel kullanıcı kodu çalıştırmak için çağrılır. Bu kod, bu işlemlerin dışında çağrılmamalıdır.

## <a name="how-to-fix-violations"></a>İhlaller Nasıl Düzeltilir?
 Bu kural ihlalini düzeltmek için yöntemin erişilebilirliği değiştirme `private` veya `internal` (`Friend` içinde [!INCLUDE[vbprvb](../includes/vbprvb-md.md)]).

## <a name="when-to-suppress-warnings"></a>Uyarılar Bastırıldığında
 Bu kuraldan uyarıyı bastırmayın.

## <a name="example"></a>Örnek
 Aşağıdaki örnek, kural ihlal iki yöntem gösterir.

 [!code-csharp[FxCop.Interoperability.ComRegistration2#1](../snippets/csharp/VS_Snippets_CodeAnalysis/FxCop.Interoperability.ComRegistration2/cs/FxCop.Interoperability.ComRegistration2.cs#1)]
 [!code-vb[FxCop.Interoperability.ComRegistration2#1](../snippets/visualbasic/VS_Snippets_CodeAnalysis/FxCop.Interoperability.ComRegistration2/vb/FxCop.Interoperability.ComRegistration2.vb#1)]

## <a name="related-rules"></a>İlgili kuralları
 [CA1410: COM kayıt yöntemleri eşleşmelidir](../code-quality/ca1410-com-registration-methods-should-be-matched.md)

## <a name="see-also"></a>Ayrıca Bkz.
 <xref:System.Runtime.InteropServices.RegistrationServices?displayProperty=fullName> [Derlemeleri COM ile kaydetme](https://msdn.microsoft.com/library/87925795-a3ae-4833-b138-125413478551) [Regasm.exe (derleme kayıt aracı)](https://msdn.microsoft.com/library/e190e342-36ef-4651-a0b4-0e8c2c0281cb)

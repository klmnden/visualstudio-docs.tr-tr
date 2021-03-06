---
title: 'CA1057: String URI aşırı yüklemeleri System.Uri aşırı çağrı | Microsoft Docs'
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-code-analysis
ms.topic: reference
f1_keywords:
- CA1057
- StringUriOverloadsCallSystemUriOverloads
helpviewer_keywords:
- StringUriOverloadsCallSystemUriOverloads
- CA1057
ms.assetid: ef1e983e-9ca7-404b-82d7-65740ba0ce20
caps.latest.revision: 16
author: gewarren
ms.author: gewarren
manager: wpickett
ms.openlocfilehash: 4cf50ca225544b06409415320c73e7824a10843a
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62552735"
---
# <a name="ca1057-string-uri-overloads-call-systemuri-overloads"></a>CA1057: String URI aşırı yüklemeleri System.Uri aşırı yüklemelerini çağırır
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

|||
|-|-|
|TypeName|StringUriOverloadsCallSystemUriOverloads|
|CheckId|CA1057|
|Kategori|Microsoft.Design|
|Yeni Değişiklik|Bölünemez|

## <a name="cause"></a>Sebep
 Bir tür yalnızca bir dize parametresi adlandırılan farklı yöntem aşırı yüklemeleri bildirir bir <xref:System.Uri?displayProperty=fullName> parametresi ve dize parametresi alan aşırı yüklemesini alan aşırı yüklemesini çağırmaz <xref:System.Uri> parametresi.

## <a name="rule-description"></a>Kural Tanımı
 Yalnızca dize tarafından aşırı yüklemeler farklı olduğundan /<xref:System.Uri> parametresi dize bir Tekdüzen Kaynak Tanımlayıcısı (URI) temsil etmek için varsayılır. Bir URI'nın dize sunumu ayrıştırma ve hataları kodlama eğilimindedir ve güvenlik açıklarına yol açabilir. <xref:System.Uri> Sınıfı bu hizmetleri güvenli bir biçimde sunar. Avantajlarını kazanmak için <xref:System.Uri> sınıfı, dize aşırı yüklemesi çağırmanız <xref:System.Uri> dize bağımsız değişkeni kullanılarak aşırı yükleme.

## <a name="how-to-fix-violations"></a>İhlaller Nasıl Düzeltilir?
 URI'ın dize gösterimini kullanır ve böylece bir örneğini oluşturur yöntemi yeniden uygulamak <xref:System.Uri> dize bağımsız değişkeni kullanarak ve ardından geçirir <xref:System.Uri> olan aşırı yüklenmiş bir nesneye <xref:System.Uri> parametresi.

## <a name="when-to-suppress-warnings"></a>Uyarılar Bastırıldığında
 Dize parametresi bir URI temsil etmiyorsa, bu kuraldan bir uyarıyı bastırmak güvenlidir.

## <a name="example"></a>Örnek
 Aşağıdaki örnek, doğru uygulanmış bir aşırı gösterir.

 [!code-cpp[FxCop.Design.CallUriOverload#1](../snippets/cpp/VS_Snippets_CodeAnalysis/FxCop.Design.CallUriOverload/cpp/FxCop.Design.CallUriOverload.cpp#1)]
 [!code-csharp[FxCop.Design.CallUriOverload#1](../snippets/csharp/VS_Snippets_CodeAnalysis/FxCop.Design.CallUriOverload/cs/FxCop.Design.CallUriOverload.cs#1)]
 [!code-vb[FxCop.Design.CallUriOverload#1](../snippets/visualbasic/VS_Snippets_CodeAnalysis/FxCop.Design.CallUriOverload/vb/FxCop.Design.CallUriOverload.vb#1)]

## <a name="related-rules"></a>İlgili kuralları
 [CA2234: Dizeler yerine System.Uri nesneleri geçirin](../code-quality/ca2234-pass-system-uri-objects-instead-of-strings.md)

 [CA1056: URI özellikleri dizeler olmamalıdır](../code-quality/ca1056-uri-properties-should-not-be-strings.md)

 [CA1054: URI parametreleri dizeler olmamalıdır](../code-quality/ca1054-uri-parameters-should-not-be-strings.md)

 [CA1055: URI dönüş değerleri dizeler olmamalıdır](../code-quality/ca1055-uri-return-values-should-not-be-strings.md)

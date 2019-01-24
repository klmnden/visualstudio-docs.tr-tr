---
title: 'CA1054: URI parametreleri dizeler olmamalıdır | Microsoft Docs'
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-code-analysis
ms.topic: reference
f1_keywords:
- CA1054
- UriParametersShouldNotBeStrings
helpviewer_keywords:
- CA1054
- UriParametersShouldNotBeStrings
ms.assetid: 8e99d72b-a658-47a7-8dd5-9784ce2c30b8
caps.latest.revision: 16
author: gewarren
ms.author: gewarren
manager: wpickett
ms.openlocfilehash: f7af579cf92a785f9850805ae06743a15364eade
ms.sourcegitcommit: 8b538eea125241e9d6d8b7297b72a66faa9a4a47
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54754802"
---
# <a name="ca1054-uri-parameters-should-not-be-strings"></a>CA1054: URI parametreleri dize olmamalıdır
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

|||
|-|-|
|TypeName|UriParametersShouldNotBeStrings|
|CheckId|CA1054|
|Kategori|Microsoft.Design|
|Yeni Değişiklik|Yeni|

## <a name="cause"></a>Sebep
 Adında "URI", "Uri", "urn", "Urn", "url" veya "Url" içeren bir dize parametresi olan bir yöntem bir tür bildirir ve türü alan karşılık gelen aşırı bildirmiyor bir <xref:System.Uri?displayProperty=fullName> parametresi.

## <a name="rule-description"></a>Kural Tanımı
 Bu kural, parametre adı belirteçleri camel casing standardına göre ayıran ve her belirteç "URI", "Uri", "urn", "Urn", "url" veya "Url" eşit olup olmadığını denetler. Bir eşleşme varsa, kural parametresi bir Tekdüzen Kaynak Tanımlayıcısı (URI) temsil ettiğini varsayar. Bir URI'nın dize sunumu ayrıştırma ve hataları kodlama eğilimindedir ve güvenlik açıklarına yol açabilir. Örneğini alan sağlanan URI dize gösterimi bir yöntemi alır, karşılık gelen aşırı olmalıdır <xref:System.Uri> bu hizmetleri güvenli bir şekilde sağlar sınıfını.

## <a name="how-to-fix-violations"></a>İhlaller Nasıl Düzeltilir?
 Bu kural ihlalini düzeltmek için parametreyi değiştirmek bir <xref:System.Uri> yazın; bir değişiklik budur. Alternatif olarak, alan yönteminin bir aşırı yüklemesini sağlayan bir <xref:System.Uri> parametre; bu bölünemez bir değişikliktir.

## <a name="when-to-suppress-warnings"></a>Uyarılar Bastırıldığında
 Parametre bir URI temsil etmiyorsa bu kuraldan bir uyarıyı bastırmak güvenlidir.

## <a name="example"></a>Örnek
 Aşağıdaki örnek, bir tür gösterir `ErrorProne`, bu kuralı ve bir tür ihlal `SaferWay`, bu kural karşılar.

 [!code-cpp[FxCop.Design.UriNotString#1](../snippets/cpp/VS_Snippets_CodeAnalysis/FxCop.Design.UriNotString/cpp/FxCop.Design.UriNotString.cpp#1)]
 [!code-csharp[FxCop.Design.UriNotString#1](../snippets/csharp/VS_Snippets_CodeAnalysis/FxCop.Design.UriNotString/cs/FxCop.Design.UriNotString.cs#1)]
 [!code-vb[FxCop.Design.UriNotString#1](../snippets/visualbasic/VS_Snippets_CodeAnalysis/FxCop.Design.UriNotString/vb/FxCop.Design.UriNotString.vb#1)]

## <a name="related-rules"></a>İlgili kuralları
 [CA1056: URI özellikleri dizeler olmamalıdır](../code-quality/ca1056-uri-properties-should-not-be-strings.md)

 [CA1055: URI dönüş değerleri dizeler olmamalıdır](../code-quality/ca1055-uri-return-values-should-not-be-strings.md)

 [CA2234: Dizeler yerine System.Uri nesneleri geçirin](../code-quality/ca2234-pass-system-uri-objects-instead-of-strings.md)

 [CA1057: String URI aşırı yüklemeleri System.Uri aşırı yüklemelerini çağırır](../code-quality/ca1057-string-uri-overloads-call-system-uri-overloads.md)

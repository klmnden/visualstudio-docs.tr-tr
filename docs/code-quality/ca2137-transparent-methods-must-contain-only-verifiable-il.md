---
title: 'CA2137: Saydam metotlar yalnızca doğrulanabilir IL içermelidir'
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- CA2137
ms.assetid: cbaeb0e1-56b6-43b4-812a-596b2859c329
author: gewarren
ms.author: gewarren
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 8ae8f507f17a1c64cb9fdfc5872ffa22e3c0f170
ms.sourcegitcommit: 0c2523d975d48926dd2b35bcd2d32a8ae14c06d8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/24/2019
ms.locfileid: "71232227"
---
# <a name="ca2137-transparent-methods-must-contain-only-verifiable-il"></a>CA2137: Saydam metotlar yalnızca doğrulanabilir IL içermelidir

|||
|-|-|
|TypeName|TransparentMethodsMustBeVerifiable|
|CheckId|CA2137|
|Kategori|Microsoft.Security|
|Son değişiklik|Yeni|

## <a name="cause"></a>Sebep
Bir yöntem, doğrulanamayan kodu içerir veya başvuruya göre bir tür döndürür.

## <a name="rule-description"></a>Kural açıklaması
Bu kural, doğrulanamayan MSIL'yi (Microsoft Ara Dili) yürütmek için güvenlik saydam kodu tarafından girişimleri tetikler. Ancak kural tam IL doğrulayıcısı içermez ve MSIL doğrulamasının çoğu ihlalini yakalamak için buluşsal yöntemler kullanır.

Kodunuzun yalnızca doğrulanabilir MSIL içerdiğinden emin olmak için, derlemenizin içinde [Peverify. exe (PEVerify Aracı)](/dotnet/framework/tools/peverify-exe-peverify-tool) çalıştırın. Çıktıyı yalnızca doğrulanamayan saydam yöntemlerle sınırlayan ve hataya neden olabilecek **/Transparent** seçeneğiyle PEVerify komutunu çalıştırın. /Transparent seçeneği kullanılmazsa, PEVerify, doğrulanamayan kod içermesine izin verilen kritik yöntemleri de doğrular.

## <a name="how-to-fix-violations"></a>İhlalleri çözme
Bu kural ihlalini onarmak için yöntemini <xref:System.Security.SecurityCriticalAttribute> veya <xref:System.Security.SecuritySafeCriticalAttribute> özniteliğiyle işaretleyin ya da doğrulanamaz kodu kaldırın.

## <a name="when-to-suppress-warnings"></a>Uyarıların ne zaman bastırılamıyor
Bu kuraldan uyarıyı bastırmayın.

## <a name="example"></a>Örnek
Bu örnekteki yöntem doğrulanamayan kodu kullanır ve <xref:System.Security.SecurityCriticalAttribute> ya <xref:System.Security.SecuritySafeCriticalAttribute> da özniteliğiyle işaretlenmelidir.

[!code-csharp[FxCop.Security.CA2137.TransparentMethodsMustBeVerifiable#1](../code-quality/codesnippet/CSharp/ca2137-transparent-methods-must-contain-only-verifiable-il_1.cs)]
---
title: 'CA2137: Saydam yöntemler yalnızca doğrulanabilir IL içermelidir | Microsoft Docs'
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-code-analysis
ms.topic: reference
f1_keywords:
- CA2137
ms.assetid: cbaeb0e1-56b6-43b4-812a-596b2859c329
caps.latest.revision: 15
author: gewarren
ms.author: gewarren
manager: wpickett
ms.openlocfilehash: 2803e220cd38bc03efa464bbe857ab41fff1ea52
ms.sourcegitcommit: 08fc78516f1107b83f46e2401888df4868bb1e40
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/15/2019
ms.locfileid: "65696236"
---
# <a name="ca2137-transparent-methods-must-contain-only-verifiable-il"></a>CA2137: Saydam metotlar yalnızca doğrulanabilir IL içermelidir
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

|||
|-|-|
|TypeName|TransparentMethodsMustBeVerifiable|
|CheckId|CA2137|
|Kategori|Microsoft.Security|
|Yeni Değişiklik|Yeni|

## <a name="cause"></a>Sebep
 Bir yöntem, doğrulanamayan kodu içerir veya başvuruya göre bir tür döndürür.

## <a name="rule-description"></a>Kural Tanımı
 Bu kural, doğrulanamayan MSIL'yi (Microsoft Ara Dili) yürütmek için güvenlik saydam kodu tarafından girişimleri tetikler. Ancak kural tam IL doğrulayıcısı içermez ve MSIL doğrulamasının çoğu ihlalini yakalamak için buluşsal yöntemler kullanır.

 Kodunuzu yalnızca doğrulanabilir MSIL içeren emin olmak için çalıştırın [Peverify.exe (PEVerify aracı)](https://msdn.microsoft.com/library/f4f46f9e-8d08-4e66-a94b-0c69c9b0bbfa) bütünleştirilmiş kodunuzda. PEVerify ile çalıştırma **/ saydam** hataya neden olur yalnızca doğrulanamayan saydam yöntemleri çıkışı sınırlar seçeneği. Varsa / saydam seçeneği kullanılmazsa, PEVerify doğrulanamayan kodu içermesi için izin verilen kritik yöntemleri de doğrular.

## <a name="how-to-fix-violations"></a>İhlaller Nasıl Düzeltilir?
 Bu kural ihlalini düzeltmek için yöntemi işaretlemek <xref:System.Security.SecurityCriticalAttribute> veya <xref:System.Security.SecuritySafeCriticalAttribute> özniteliği veya doğrulanamaz kod kaldırın.

## <a name="when-to-suppress-warnings"></a>Uyarılar Bastırıldığında
 Bu kuraldan uyarıyı bastırmayın.

## <a name="example"></a>Örnek
 Bu örnekte yöntem doğrulanamaz kod kullanır ve ile işaretlenmelidir <xref:System.Security.SecurityCriticalAttribute> veya <xref:System.Security.SecuritySafeCriticalAttribute> özniteliği.

 [!code-csharp[FxCop.Security.CA2137.TransparentMethodsMustBeVerifiable#1](../snippets/csharp/VS_Snippets_CodeAnalysis/fxcop.security.ca2137.transparentmethodsmustbeverifiable/cs/ca2137 - transparentmethodsmustbeverifiable.cs#1)]

---
title: 'CA1302: Yerel özel dizeleri otomatik olarak gömmeyin | Microsoft Docs'
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-code-analysis
ms.topic: reference
f1_keywords:
- DoNotHardcodeLocaleSpecificStrings
- CA1302
helpviewer_keywords:
- DoNotHardcodeLocaleSpecificStrings
- CA1302
ms.assetid: 05ed134a-837d-43d7-bf97-906edeac44ce
caps.latest.revision: 19
author: gewarren
ms.author: gewarren
manager: wpickett
ms.openlocfilehash: d52489ba25fe2c541d2d0329fcad61aef75350e9
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "68200417"
---
# <a name="ca1302-do-not-hardcode-locale-specific-strings"></a>CA1302: Yerel özel dizeleri doğrudan programın içine gömmeyin
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

|||
|-|-|
|TypeName|DoNotHardcodeLocaleSpecificStrings|
|CheckId|CA1302|
|Kategori|Microsoft.Globalization|
|Yeni Değişiklik|Bölünemez|

## <a name="cause"></a>Sebep
 Belirli sistem klasörlerinin yolu parçası temsil eden bir dize sabit değeri bir yöntem kullanır.

## <a name="rule-description"></a>Kural Tanımı
 <xref:System.Environment.SpecialFolder?displayProperty=fullName> Numaralandırma özel sistem klasörlerine başvuran üyeleri içerir. Bu klasörlerin konumları farklı işletim sistemleri üzerinde farklı değerlere sahip olabilir, kullanıcı konumları değiştirebilir ve konumlar yerelleştirilmiştir. Özel bir klasör "C:\WINDOWS\system32" olan sistem klasörü üzerinde örneğidir [!INCLUDE[winxp](../includes/winxp-md.md)] ancak üzerinde "C:\WINNT\system32" [!INCLUDE[win2kfamily](../includes/win2kfamily-md.md)]. <xref:System.Environment.GetFolderPath%2A?displayProperty=fullName> Yöntemi ile ilişkili konumları döndürür <xref:System.Environment.SpecialFolder> sabit listesi. Tarafından döndürülen konumları <xref:System.Environment.GetFolderPath%2A> yerelleştirilir ve için o anda çalışan bilgisayara uygun.

 Bu kural kullanarak alınabilecek klasör yollarını tokenizes <xref:System.Environment.GetFolderPath%2A> ayrı dizin düzeylere yöntemi. Her dize sabit değeri belirteçleri karşılaştırılır. Bir eşleşme bulunursa, yöntem belirteçle ilişkilendirilen sistem konuma başvuran bir dize oluşturuyor varsayılır. Taşınabilirlik ve yerelleştirme için <xref:System.Environment.GetFolderPath%2A> dize değişmez değerleri kullanmak yerine özel sistem klasörlerine konumlarını almak için yöntemi.

## <a name="how-to-fix-violations"></a>İhlaller Nasıl Düzeltilir?
 Bu kural ihlalini düzeltmek için konumu kullanarak almak <xref:System.Environment.GetFolderPath%2A> yöntemi.

## <a name="when-to-suppress-warnings"></a>Uyarılar Bastırıldığında
 Dize sabit değeri ile ilişkili sistem konumlardan birine başvurmak için kullanılmıyorsa bu kuraldan bir uyarıyı bastırmak güvenlidir <xref:System.Environment.SpecialFolder> sabit listesi.

## <a name="example"></a>Örnek
 Aşağıdaki örnek bu kuraldan üç uyarıları oluşturur ortak uygulama veri klasörünün yolunu oluşturur. Ardından, kullanarak örnek yolunu alır <xref:System.Environment.GetFolderPath%2A> yöntemi.

 [!code-csharp[FxCop.Globalization.HardcodedLocaleStrings#1](../snippets/csharp/VS_Snippets_CodeAnalysis/FxCop.Globalization.HardcodedLocaleStrings/cs/FxCop.Globalization.HardcodedLocaleStrings.cs#1)]
 [!code-vb[FxCop.Globalization.HardcodedLocaleStrings#1](../snippets/visualbasic/VS_Snippets_CodeAnalysis/FxCop.Globalization.HardcodedLocaleStrings/vb/FxCop.Globalization.HardcodedLocaleStrings.vb#1)]

## <a name="related-rules"></a>İlgili kuralları
 [CA1303: Harfleri yerelleştirilmiş parametreler olarak göndermeyin](../code-quality/ca1303-do-not-pass-literals-as-localized-parameters.md)

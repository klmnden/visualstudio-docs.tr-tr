---
title: 'CA1304: CultureInfo belirt | Microsoft Docs'
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-code-analysis
ms.topic: reference
f1_keywords:
- SpecifyCultureInfo
- CA1304
helpviewer_keywords:
- SpecifyCultureInfo
- CA1304
ms.assetid: b912d76a-54fd-4c93-b25d-16491e0ae319
caps.latest.revision: 22
author: gewarren
ms.author: gewarren
manager: wpickett
ms.openlocfilehash: 173ab11e85853324089f1dee66cd047e0afb7f13
ms.sourcegitcommit: 8b538eea125241e9d6d8b7297b72a66faa9a4a47
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54767375"
---
# <a name="ca1304-specify-cultureinfo"></a>CA1304: CultureInfo belirt
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

|||
|-|-|
|TypeName|SpecifyCultureInfo|
|CheckId|CA1304|
|Kategori|Microsoft.Globalization|
|Yeni Değişiklik|Bölünemez|

## <a name="cause"></a>Sebep
 Yöntem veya Oluşturucu kabul eden aşırı yüklenmiş bir üyeyi çağıran bir <xref:System.Globalization.CultureInfo?displayProperty=fullName> parametresi ve yöntem veya Oluşturucu alan aşırı yüklemesini çağırmaz <xref:System.Globalization.CultureInfo> parametresi. Bu kural aşağıdaki yöntemlere yapılan çağrılar yok sayar:

-   <xref:System.Activator.CreateInstance%2A?displayProperty=fullName>

-   <xref:System.Resources.ResourceManager.GetObject%2A?displayProperty=fullName>

-   <xref:System.Resources.ResourceManager.GetString%2A?displayProperty=fullName>

## <a name="rule-description"></a>Kural Tanımı
 Olduğunda bir <xref:System.Globalization.CultureInfo> veya <xref:System.IFormatProvider?displayProperty=fullName> nesnesi sağlanmadı, aşırı yüklü üye tarafından sağlanan varsayılan değer, tüm yerel ayarlarda istediğiniz etkiyi vermeyebilir. Ayrıca, [!INCLUDE[dnprdnshort](../includes/dnprdnshort-md.md)] üyeleri varsayılan kültür seçin ve alan biçimlendirme hakkında varsayımlar kodunuz için doğru olmayabilir. Kod senaryolarınız için beklendiği gibi çalıştığından emin olmak için aşağıdaki kılavuzlara göre kültüre özgü bilgileri vermeniz gerekir:

- Değeri kullanıcıya görüntülenir, geçerli kültür kullanın. Bkz. <xref:System.Globalization.CultureInfo.CurrentCulture%2A?displayProperty=fullName>.

- Diğer bir deyişle, bir dosya ya da veritabanı, kalıcı bir değeri depolanan ve yazılım tarafından erişilen, sabit kültür kullanın. Bkz. <xref:System.Globalization.CultureInfo.InvariantCulture%2A?displayProperty=fullName>.

- Hedef değerin bilmiyorsanız, veri tüketici sahip veya sağlayıcıyı kültür.

  Unutmayın <xref:System.Globalization.CultureInfo.CurrentUICulture%2A?displayProperty=fullName> yalnızca bir örneğini kullanarak yerelleştirilmiş kaynakları almak için kullanılan <xref:System.Resources.ResourceManager?displayProperty=fullName> sınıfı.

  Varsayılan davranışı, aşırı yüklü üye gereksinimleriniz için uygun olsa bile, böylece kendi belge ve daha kolay tutulan kodunuzu kültüre özgü aşırı açıkça çağırmak daha iyidir.

## <a name="how-to-fix-violations"></a>İhlaller Nasıl Düzeltilir?
 Bu kural ihlalini düzeltmek için alan aşırı yüklemesini kullanın. bir <xref:System.Globalization.CultureInfo> veya <xref:System.IFormatProvider> ve daha önce listelenen yönergelerine göre bağımsız değişken belirtin.

## <a name="when-to-suppress-warnings"></a>Uyarılar Bastırıldığında
 Varsayılan kültür/biçim sağlayıcısı doğru seçimdir belirli olduğunda ve kod bakımı önemli geliştirme önceliği olmadığı bu kuraldan bir uyarıyı bastırmak güvenlidir.

## <a name="example"></a>Örnek
 Aşağıdaki örnekte, `BadMethod` iki bu kural ihlalleri neden olur. `GoodMethod` Sabit kültür için System.String.Compare geçirerek ilk ihlali düzeltir ve ikinci ihlali için geçerli kültürün geçirerek düzeltir <xref:System.String.ToLower%2A> çünkü `string3` kullanıcıya görüntülenir.

 [!code-csharp[FxCop.Globalization.CultureInfo#1](../snippets/csharp/VS_Snippets_CodeAnalysis/FxCop.Globalization.CultureInfo/cs/FxCop.Globalization.CultureInfo.cs#1)]

## <a name="example"></a>Örnek
 Aşağıdaki örnek, varsayılan olarak geçerli kültürü etkisini gösterir <xref:System.IFormatProvider> tarafından seçilen <xref:System.DateTime> türü.

 [!code-csharp[FxCop.Globalization.IFormatProvider#1](../snippets/csharp/VS_Snippets_CodeAnalysis/FxCop.Globalization.IFormatProvider/cs/FxCop.Globalization.IFormatProvider.cs#1)]

 Bu örnek aşağıdaki çıktıyı üretir.

 **6/4/1900 12:15:12 PM**
**06/04/1900 12:15:12**
## <a name="related-rules"></a>İlgili kuralları
 [CA1305: Iformatprovider belirtin](../code-quality/ca1305-specify-iformatprovider.md)

## <a name="see-also"></a>Ayrıca Bkz.
 [NIB: CultureInfo sınıfını kullanma](http://msdn.microsoft.com/d4329e34-64c3-4d1e-8c73-5b0ee626ba7a)

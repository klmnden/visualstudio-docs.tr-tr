---
title: 'CA1305: Iformatprovider belirtme | Microsoft Docs'
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-code-analysis
ms.topic: reference
f1_keywords:
- SpecifyIFormatProvider
- CA1305
helpviewer_keywords:
- CA1305
- SpecifyIFormatProvider
ms.assetid: fb34ed9a-4eab-47cc-8eef-3068a4a1397e
caps.latest.revision: 24
author: gewarren
ms.author: gewarren
manager: wpickett
ms.openlocfilehash: 11e1d9614c4f2a512c56f84117d28363e80c6b90
ms.sourcegitcommit: 1fc6ee928733e61a1f42782f832ead9f7946d00c
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/22/2019
ms.locfileid: "60048107"
---
# <a name="ca1305-specify-iformatprovider"></a>CA1305: IFormatProvider belirt
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

|||
|-|-|
|TypeName|SpecifyIFormatProvider|
|CheckId|CA1305|
|Kategori|Microsoft.Globalization|
|Yeni Değişiklik|Bölünemez|

## <a name="cause"></a>Sebep
 Yöntem veya Oluşturucu kabul eden aşırı yüklemelere sahip bir veya daha fazla üye çağıran bir <xref:System.IFormatProvider?displayProperty=fullName> parametresi ve yöntem veya Oluşturucu alan aşırı yüklemesini çağırmaz <xref:System.IFormatProvider> parametresi. Bu kural çağrıları yok sayar [!INCLUDE[dnprdnshort](../includes/dnprdnshort-md.md)] yoksayılıyor olarak belgelenmiştir yöntemleri <xref:System.IFormatProvider> parametresi ve ayrıca aşağıdaki yöntemlerden:

- <xref:System.Activator.CreateInstance%2A?displayProperty=fullName>

- <xref:System.Resources.ResourceManager.GetObject%2A?displayProperty=fullName>

- <xref:System.Resources.ResourceManager.GetString%2A?displayProperty=fullName>

## <a name="rule-description"></a>Kural Tanımı
 Olduğunda bir <xref:System.Globalization.CultureInfo?displayProperty=fullName> veya <xref:System.IFormatProvider> nesnesi sağlanmadı, aşırı yüklü üye tarafından sağlanan varsayılan değer, tüm yerel ayarlarda istediğiniz etkiyi vermeyebilir. Ayrıca, [!INCLUDE[dnprdnshort](../includes/dnprdnshort-md.md)] üyeleri varsayılan kültür seçin ve alan biçimlendirme hakkında varsayımlar kodunuz için doğru olmayabilir. Kod senaryolarınız için beklendiği gibi çalıştığından emin olmak için aşağıdaki kılavuzlara göre kültüre özgü bilgileri vermeniz gerekir:

- Değeri kullanıcıya görüntülenir, geçerli kültür kullanın. Bkz. <xref:System.Globalization.CultureInfo.CurrentCulture%2A?displayProperty=fullName>.

- Bir değeri depolanan ve (bir dosyadan veya veritabanından kalıcı) yazılım tarafından erişilen, sabit kültür kullanın. Bkz. <xref:System.Globalization.CultureInfo.InvariantCulture%2A?displayProperty=fullName>.

- Hedef değerin bilmiyorsanız, veri tüketici sahip veya sağlayıcıyı kültür.

  Unutmayın <xref:System.Globalization.CultureInfo.CurrentUICulture%2A?displayProperty=fullName> yalnızca bir örneğini kullanarak yerelleştirilmiş kaynakları almak için kullanılan <xref:System.Resources.ResourceManager?displayProperty=fullName> sınıfı.

  Varsayılan davranışı, aşırı yüklü üye gereksinimleriniz için uygun olsa bile, böylece kendi belge ve daha kolay tutulan kodunuzu kültüre özgü aşırı açıkça çağırmak daha iyidir.

## <a name="how-to-fix-violations"></a>İhlaller Nasıl Düzeltilir?
 Bu kural ihlalini düzeltmek için alan aşırı yüklemesini kullanın. bir <xref:System.Globalization.CultureInfo> veya <xref:System.IFormatProvider> ve daha önce listelenen yönergelerine göre bağımsız değişken belirtin.

## <a name="when-to-suppress-warnings"></a>Uyarılar Bastırıldığında
 Varsayılan kültür/biçim sağlayıcısı doğru seçim ve sürdürülebilirlik önemli geliştirme öncelikli olduğu geldiğinden emin olduğunda bu kuraldan bir uyarıyı bastırmak güvenlidir.

## <a name="example"></a>Örnek
 Aşağıdaki örnekte, `BadMethod` iki bu kural ihlalleri neden olur. `GoodMethod` Sabit kültür için geçirerek ilk ihlali düzeltir <xref:System.String.Compare%2A>ve geçerli kültürü için geçirerek ikinci ihlali düzeltir <xref:System.String.ToLower%2A> çünkü `string3` kullanıcıya görüntülenir.

 [!code-csharp[FxCop.Globalization.CultureInfo#1](../snippets/csharp/VS_Snippets_CodeAnalysis/FxCop.Globalization.CultureInfo/cs/FxCop.Globalization.CultureInfo.cs#1)]

## <a name="example"></a>Örnek
 Aşağıdaki örnek, varsayılan olarak geçerli kültürü etkisini gösterir <xref:System.IFormatProvider> tarafından seçilen <xref:System.DateTime> türü.

 [!code-csharp[FxCop.Globalization.IFormatProvider#1](../snippets/csharp/VS_Snippets_CodeAnalysis/FxCop.Globalization.IFormatProvider/cs/FxCop.Globalization.IFormatProvider.cs#1)]

 Bu örnek aşağıdaki çıktıyı üretir.

 **6/4/1900 12:15:12 PM**
**06/04/1900 12:15:12**
## <a name="related-rules"></a>İlgili kuralları
 [CA1304: CultureInfo belirt](../code-quality/ca1304-specify-cultureinfo.md)

## <a name="see-also"></a>Ayrıca Bkz.
 [NIB: CultureInfo sınıfını kullanma](http://msdn.microsoft.com/d4329e34-64c3-4d1e-8c73-5b0ee626ba7a)

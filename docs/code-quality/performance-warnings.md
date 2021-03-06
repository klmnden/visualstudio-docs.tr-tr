---
title: Performans Uyarıları
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- vs.codeanalysis.performancerules
helpviewer_keywords:
- warnings, performance
- performance warnings
- performance, warnings
- managed code analysis warnings, performance warnings
ms.assetid: e014ac3a-02e6-46d9-942c-3491dd63782f
author: gewarren
ms.author: gewarren
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: f8d8f06fe0d3d1e114662a8ea99d1458d65e3e4c
ms.sourcegitcommit: 541a0556958201ad6626bc8638406ad02640f764
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/18/2019
ms.locfileid: "71079238"
---
# <a name="performance-warnings"></a>Performans Uyarıları
Performans uyarıları yüksek performanslı kitaplıkları ve uygulamaları destekler.

## <a name="in-this-section"></a>Bu Bölümde

| Kural | Açıklama |
| - | - |
| [CA1800 Gereksiz yere atama](../code-quality/ca1800-do-not-cast-unnecessarily.md) | Özellikle yayınlar sıkıştırılmış yineleme deyiminde gerçekleştirildiğinde yinelenen yayınların performansını azaltır. |
| [CA1801 Kullanılmayan parametreleri gözden geçir](../code-quality/ca1801-review-unused-parameters.md) | Yöntem imzası, yöntemin gövdesinde kullanılmayan bir parametre içerir. |
| [CA1802 Uygun yerlerde sabit değerler kullanın](../code-quality/ca1802-use-literals-where-appropriate.md) | Bir alan statik ve salt okunur (paylaşılan ve salt [!INCLUDE[vbprvb](../code-quality/includes/vbprvb_md.md)]okunur) olarak tanımlanır ve derleme zamanında oluşturulabilir bir değer ile başlatılır. Hedeflenen alana atanan değer derleme zamanında hesaplanabilir olduğundan, bildirimi hesaplanmasını değiştirme (içinde sabit [!INCLUDE[vbprvb](../code-quality/includes/vbprvb_md.md)]) ve böylece, çalışma zamanında derleme zamanından yerine değeri hesaplanan alan. |
| [CA1804 Kullanılmayan yerelleri kaldır](../code-quality/ca1804-remove-unused-locals.md) | Kullanılmayan yerel değişkenler ve gereksiz atamaların derleme boyutunu artırır ve performansı düşürür. |
| [CA1806 Yöntem sonuçlarını yoksaymayın](../code-quality/ca1806-do-not-ignore-method-results.md) | Yeni bir nesne oluşturulur, ancak hiçbir zaman kullanılmaz veya yeni bir dize oluşturan ve döndüren bir yöntem çağrılır ve yeni dize hiçbir zaman kullanılmaz veya bir bileşen nesne modeli (COM) ya da P/Invoke yöntemi hiçbir zaman kullanılmayan bir HRESULT veya hata kodu döndürür. |
| [CA1809 Aşırı Yerellerden kaçının](../code-quality/ca1809-avoid-excessive-locals.md) | Bir değeri bellek yerine işlemci yazmacında tutmak yaygın bir performans iyileştirmesidir ve buna "değeri kaydetmek denir".  Tüm yerel değişkenlerin kaydedilme imkanına sahip olabilmesi şansını artırmak için 64 yerel değişken sayısını sınırlayın. |
| [CA1810 Başvuru türü statik alanları satır içi Başlat](../code-quality/ca1810-initialize-reference-type-static-fields-inline.md) | Bir tür açık statik yapıcı bildirdiğinde, JIT derleyici her bir statik yöntemi kontrol ekler ve türün yapıcı örneği statik yapıcının daha önceden çağrıldığından emin olur. Statik oluşturucu denetimleri performansı düşürebilir. |
| [CA1811 Çağrılmadı özel koddan kaçının](../code-quality/ca1811-avoid-uncalled-private-code.md) | Özel veya dahili (derleme düzeyi) bir üyenin derlemede çağıranları yoktur, ortak dil çalışma zamanı tarafından çağrılmaz ve bir temsilci tarafından çağrılmaz. |
| [CA1812 Örneklenmemiş iç sınıflardan kaçının](../code-quality/ca1812-avoid-uninstantiated-internal-classes.md) | Bir derleme düzeyi türünün örneği, derleme içindeki kod tarafından oluşturulmaz. |
| [CA1813 Korumasız özniteliklerden kaçının](../code-quality/ca1813-avoid-unsealed-attributes.md) | .NET özel özniteliklerin alınması için yöntemler sağlar. Varsayılan olarak, bu yöntemleri öznitelik devralma hiyerarşisinde arar. Öznitelik mühürleme kalıtım hiyerarşisi aracılığıyla aramayı ortadan kaldırır ve performansı artırabilir. |
| [CA1814 Çok boyutlu üzerinde pürüzlü Diziler tercih etme](../code-quality/ca1814-prefer-jagged-arrays-over-multidimensional.md) | Basit bir dizi, öğeleri dizi olan bir dizidir. Öğeleri oluşturan diziler farklı boyutlarda olabilir ve bu da bazı veri kümeleri için daha az alana yol açabilir. |
| [CA1815 Değer türlerinde Equals ve işleç eşittir geçersiz kılma](../code-quality/ca1815-override-equals-and-operator-equals-on-value-types.md) | Değer türleri için, Equals'ın devralınmış uygulaması Reflection kitaplığını kullanır ve türdeki tüm alanların içeriğini karşılaştırır. Yansıma hesaplama açısından pahalıdır ve her alan için eşitlik karşılaştırma gereksiz olabilir. Kullanıcıları karşılaştırmak veya örneklerini sıralamak ya da tablo anahtarlarını karma olarak kullanmayı bekliyorsanız, değer türünüz Equals'ı uygulamalıdır. |
| [CA1816 GC 'yi çağırın. SuppressFinalize doğru](../code-quality/ca1816-call-gc-suppressfinalize-correctly.md) | Dispose uygulamasının bir yöntemi GC çağrısını yapmaz. SuppressFinalize veya Dispose çağrılarının uygulanması olmayan bir yöntem GC. SuppressFinalize veya bir yöntemi GC çağırır. SuppressFinalize ve bu (benim [!INCLUDE[vbprvb](../code-quality/includes/vbprvb_md.md)]) dışında bir şey geçirir. |
| [CA1819 Özellikler diziler döndürmemelidir](../code-quality/ca1819-properties-should-not-return-arrays.md) | Özellik salt okunurdur olsa bile, Özellikler tarafından döndürülen diziler yazma korumalı değildir. Dizi değiştirilmeye kanıt tutulacak özellik dizisinin bir kopyasını döndürmelidir. Tipik olarak, kullanıcılar bu tür bir özellik aramanın performans üzerindeki olumsuz etkilerini anlamayacaktır. |
| [CA1820 Dize uzunluğunu kullanarak boş dizeler için test](../code-quality/ca1820-test-for-empty-strings-using-string-length.md) | String.Length özelliği veya String.IsNullOrEmpty yöntemi, Equals kullanılmasından önemli ölçüde daha hızlıdır. |
| [CA1821 Boş sonlandırıcıları kaldır](../code-quality/ca1821-remove-empty-finalizers.md) | Güncelleştirirken, nesne kullanım süresini izleme söz konusu olduğunda ek performans yükü nedeniyle sonlandırıcılardan kaçının. Boş bir Sonlandırıcı, hiçbir avantaj olmadan ek yüke neden olur. |
| [CA1822: Üyeleri statik olarak işaretle](../code-quality/ca1822-mark-members-as-static.md) | Örnek veri veya çağrı örnek yöntemlerinin erişmez üyeleri işaretlenebilir olarak statik (paylaşılan [!INCLUDE[vbprvb](../code-quality/includes/vbprvb_md.md)]). Yöntemleri statik olarak işaretledikten sonra, derleyici sanal olmayan arama sitelerini bu üyelere yayar. Bu, ölçülebilir kazanç performansını performans duyarlı kodunuz için verebilir. |
| [CA1823 Kullanılmayan özel alanlardan kaçının](../code-quality/ca1823-avoid-unused-private-fields.md) | Derlemede erişimi görülmeyen özel alanlar algılandı. |
| [CA1824 Derlemeleri NeutralResourcesLanguageAttribute ile işaretleyin](../code-quality/ca1824-mark-assemblies-with-neutralresourceslanguageattribute.md) | NeutralResourcesLanguage özniteliği bir derlemenin bağımsız kültürünün kaynağını görüntüleyen dilin Kaynak Yöneticisi'ni bilgilendirir. Bu ilk yüklediğiniz kaynak için arama performansını artırır ve çalışma kümenizi azaltabilir. |
| [CA1825: Sıfır uzunluklu dizi ayırmaktan kaçının](../code-quality/ca1825.md) | Sıfır uzunluklu bir diziyi başlatmak gereksiz bellek ayırmaya yol açar. Bunun yerine, çağırarak <xref:System.Array.Empty%2A?displayProperty=nameWithType>statik olarak ayrılan boş dizi örneğini kullanın. Bellek ayırma, bu yöntemin tüm etkinleştirmeleri genelinde paylaşılır. |

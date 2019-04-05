---
title: Yönetilen kod için Güvenlik Kuralları kural kümesi
ms.date: 11/04/2016
ms.topic: reference
ms.assetid: 564aeac6-03fa-41b0-b655-88179f0ab01b
author: gewarren
ms.author: gewarren
manager: jillfra
ms.workload:
- dotnet
ms.openlocfilehash: c43e1edc2e2aae13fef6df4b4fe414b933067798
ms.sourcegitcommit: b6177ce198c7c5a00030604c9d4faa735405d5df
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/04/2019
ms.locfileid: "59018395"
---
# <a name="security-rules-rule-set-for-managed-code"></a>Yönetilen kod için Güvenlik Kuralları kural kümesi
Microsoft Güvenlik kuralları kural raporlanan olası güvenlik sorunlarını sayısı en üst düzeye çıkarmak için kümesi içermelidir.

|Kural|Açıklama|
|----------|-----------------|
|[CA2100](../code-quality/ca2100-review-sql-queries-for-security-vulnerabilities.md)|SQL sorgularını güvenlik açıkları için inceleyin|
|[CA2102](../code-quality/ca2102-catch-non-clscompliant-exceptions-in-general-handlers.md)|CLSCompliant olmayan özel durumları genel işleyiciler içinde yakalayın|
|[CA2103](../code-quality/ca2103-review-imperative-security.md)|Kesin temelli güvenliği gözden geçirin|
|[CA2104](../code-quality/ca2104-do-not-declare-read-only-mutable-reference-types.md)|Salt okunur kesilebilir başvuru türleri bildirmeyin|
|[CA2105](../code-quality/ca2105-array-fields-should-not-be-read-only.md)|Dizi alanları salt okunur olmamalıdır|
|[CA2106](../code-quality/ca2106-secure-asserts.md)|Onay deyimlerinin güvenliğini sağlayın|
|[CA2107](../code-quality/ca2107-review-deny-and-permit-only-usage.md)|Gözden geçirmeyi reddedin ve yalnızca kullanımına izin verin|
|[CA2108](../code-quality/ca2108-review-declarative-security-on-value-types.md)|Değer türleri üzerinde bildirimsel güvenliği gözden geçirin|
|[CA2109](../code-quality/ca2109-review-visible-event-handlers.md)|Görünen olay işleyicilerini gözden geçirin|
|[CA2111](../code-quality/ca2111-pointers-should-not-be-visible.md)|İşaretçiler görünür olmamalıdır|
|[CA2112](../code-quality/ca2112-secured-types-should-not-expose-fields.md)|Güvenli türler alanları açığa çıkarmamalıdır|
|[CA2114](../code-quality/ca2114-method-security-should-be-a-superset-of-type.md)|Metot güvenliği türün bir üst kümesi olmalıdır|
|[CA2115](../code-quality/ca2115-call-gc-keepalive-when-using-native-resources.md)|Yerel kaynaklar kullanırken GC.KeepAlive'ı çağırın|
|[CA2116](../code-quality/ca2116-aptca-methods-should-only-call-aptca-methods.md)|APTCA metotları yalnızca APTCA metotlarını çağırmalıdır|
|[CA2117](../code-quality/ca2117-aptca-types-should-only-extend-aptca-base-types.md)|APTCA türleri yalnızca APTCA taban türlerini genişletmelidir|
|[CA2118](../code-quality/ca2118-review-suppressunmanagedcodesecurityattribute-usage.md)|SuppressUnmanagedCodeSecurityAttribute kullanımını gözden geçirin|
|[CA2119](../code-quality/ca2119-seal-methods-that-satisfy-private-interfaces.md)|Özel arabirimleri karşılayan metotları mühürleyin|
|[CA2120](../code-quality/ca2120-secure-serialization-constructors.md)|Serileştirme oluşturucularının güvenliğini sağlayın|
|[CA2121](../code-quality/ca2121-static-constructors-should-be-private.md)|Statik oluşturucular özel olmalıdır|
|[CA2122](../code-quality/ca2122-do-not-indirectly-expose-methods-with-link-demands.md)|Bağlantı talepleri olan metotları dolaylı olarak açığa çıkarmayın|
|[CA2123](../code-quality/ca2123-override-link-demands-should-be-identical-to-base.md)|Geçersiz kılan bağlantı talepleri taban ile özdeş olmalıdır|
|[CA2124](../code-quality/ca2124-wrap-vulnerable-finally-clauses-in-outer-try.md)|Savunmasız sonunda yan tümcelerini dış deneme içine sarmalayın|
|[CA2126](../code-quality/ca2126-type-link-demands-require-inheritance-demands.md)|Tür bağlantı talepleri kalıtım taleplerini gerektirir|
|[CA2130](../code-quality/ca2130-security-critical-constants-should-be-transparent.md)|Güvenlik kritik sabitleri saydam olmalıdır|
|[CA2131](../code-quality/ca2131-security-critical-types-may-not-participate-in-type-equivalence.md)|Güvenlik kritik türleri tür eşdeğerliğine katılamaz|
|[CA2132](../code-quality/ca2132-default-constructors-must-be-at-least-as-critical-as-base-type-default-constructors.md)|Varsayılan oluşturucular en az taban tür varsayılan oluşturucular kadar kritik olmalıdır|
|[CA2133](../code-quality/ca2133-delegates-must-bind-to-methods-with-consistent-transparency.md)|Temsilciler tutarlı saydamlığı olan metotlara bağlanmalıdır|
|[CA2134](../code-quality/ca2134-methods-must-keep-consistent-transparency-when-overriding-base-methods.md)|Metotlar taban metotları geçersiz kılarken tutarlı saydamlığı tutmalıdır|
|[CA2135](../code-quality/ca2135-level-2-assemblies-should-not-contain-linkdemands.md)|Düzey 2 derlemeler LinkDemands içermemelidir|
|[CA2136](../code-quality/ca2136-members-should-not-have-conflicting-transparency-annotations.md)|Üyeler çakışan saydamlık ek açıklamalarına sahip olmamalıdır|
|[CA2137](../code-quality/ca2137-transparent-methods-must-contain-only-verifiable-il.md)|Saydam metotlar yalnızca doğrulanabilir IL içermelidir|
|[CA2138](../code-quality/ca2138-transparent-methods-must-not-call-methods-with-the-suppressunmanagedcodesecurity-attribute.md)|Saydam metotlar SuppressUnmanagedCodeSecurity özniteliğine sahip metotları çağırmamalıdır|
|[CA2139](../code-quality/ca2139-transparent-methods-may-not-use-the-handleprocesscorruptingexceptions-attribute.md)|Saydam metotlar HandleProcessCorruptingExceptions özniteliğini kullanamaz|
|[CA2140](../code-quality/ca2140-transparent-code-must-not-reference-security-critical-items.md)|Saydam kod güvenlik kritik nesnelerine başvurmamalıdır|
|[CA2141](../code-quality/ca2141-transparent-methods-must-not-satisfy-linkdemands.md)|Saydam yöntemleri LinkDemands karşılamalıdır değil|
|[CA2142](../code-quality/ca2142-transparent-code-should-not-be-protected-with-linkdemands.md)|Saydam kod LinkDemands ile korunmamalıdır|
|[CA2143](../code-quality/ca2143-transparent-methods-should-not-use-security-demands.md)|Saydam metotlar güvenlik taleplerini kullanmamalıdır|
|[CA2144](../code-quality/ca2144-transparent-code-should-not-load-assemblies-from-byte-arrays.md)|Saydam kod derlemeleri bayt dizilerinden yüklememelidir|
|[CA2145](../code-quality/ca2145-transparent-methods-should-not-be-decorated-with-the-suppressunmanagedcodesecurityattribute.md)|Saydam metotlar SuppressUnmanagedCodeSecurityAttribute ile donatılmamalıdır|
|[CA2146](../code-quality/ca2146-types-must-be-at-least-as-critical-as-their-base-types-and-interfaces.md)|Türler en az kendi taban türleri ve arabirimleri kadar kritik olmalıdır|
|[CA2147](../code-quality/ca2147-transparent-methods-may-not-use-security-asserts.md)|Saydam metotlar güvenlik onay deyimlerini kullanmamalıdır|
|[CA2149](../code-quality/ca2149-transparent-methods-must-not-call-into-native-code.md)|Saydam metotlar yerel kod içine çağırmamalıdır|
|[CA2210](../code-quality/ca2210-assemblies-should-have-valid-strong-names.md)|Derlemelerin geçerli tanımlayıcı adları olmalıdır|
|[CA3001](../code-quality/ca3001-review-code-for-sql-injection-vulnerabilities.md)|SQL ekleme güvenlik açıklarına yönelik kod gözden geçirme|
|[CA3002](../code-quality/ca3002-review-code-for-xss-vulnerabilities.md)|Kod XSS güvenlik açıkları için gözden geçirin|
|[CA3003](../code-quality/ca3003-review-code-for-file-path-injection-vulnerabilities.md)|Dosya yolu ekleme güvenlik açıklarına yönelik kod gözden geçirme|
|[CA3004](../code-quality/ca3004-review-code-for-information-disclosure-vulnerabilities.md)|Kod bilgileri açığa çıkması güvenlik açıkları için gözden geçirin|
|[CA3005](../code-quality/ca3005-review-code-for-ldap-injection-vulnerabilities.md)|LDAP ekleme güvenlik açıklarına yönelik kod gözden geçirme|
|[CA3006](../code-quality/ca3006-review-code-for-process-command-injection-vulnerabilities.md)|İşlem komut ekleme güvenlik açıklarına yönelik kod gözden geçirme|
|[CA3007](../code-quality/ca3007-review-code-for-open-redirect-vulnerabilities.md)|Kodu açık yeniden yönlendirme güvenlik açıkları için gözden geçirin|
|[CA3008](../code-quality/ca3008-review-code-for-xpath-injection-vulnerabilities.md)|XPath ekleme güvenlik açıklarına yönelik kod gözden geçirme|
|[CA3009](../code-quality/ca3009-review-code-for-xml-injection-vulnerabilities.md)|XML ekleme güvenlik açıklarına yönelik kod gözden geçirme|
|[CA3010](../code-quality/ca3010-review-code-for-xaml-injection-vulnerabilities.md)|XAML ekleme güvenlik açıklarına yönelik kod gözden geçirme|
|[CA3011](../code-quality/ca3011-review-code-for-dll-injection-vulnerabilities.md)|DLL ekleme güvenlik açıklarına yönelik kod gözden geçirme|
|[CA3012](../code-quality/ca3012-review-code-for-regex-injection-vulnerabilities.md)|Regex ekleme güvenlik açıklarına yönelik kod gözden geçirme|

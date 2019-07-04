---
title: FxCop kuralı bağlantı noktası durumu
ms.date: 05/21/2019
ms.topic: reference
helpviewer_keywords:
- fxcop rules
- fxcop analyzers, ported rules
author: gewarren
ms.author: gewarren
manager: jillfra
ms.workload:
- dotnet
ms.openlocfilehash: 4a458a50be6161e320b3ffbbe702e21f9f502c77
ms.sourcegitcommit: 74c5360186731de07828764eb32ea1033a8c2275
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/03/2019
ms.locfileid: "67559675"
---
# <a name="fxcop-rule-port-status"></a>FXCop kuralı bağlantı noktası durumu

Visual Studio'nun önceki bir sürümde daha önce statik kod analizi kullandıysanız, bu kuralların geçerli uygulama kullanılabilir olan merak ediyor olabilirsiniz [FxCop Çözümleyicileri](install-fxcop-analyzers.md). Bu sayfada unity'nin henüz bu yanı sıra verilir kuralları listelenir ve bunları bağlantı noktası planlamaktadır olup olmadığı.

## <a name="ported-rules"></a>Taşınan kurallar

[Otomatik olarak oluşturulan belgeleri sayfasını](https://github.com/dotnet/roslyn-analyzers/blob/master/src/Microsoft.CodeAnalysis.FxCopAnalyzers/Microsoft.CodeAnalysis.FxCopAnalyzers.md) roslyn Çözümleyicileri depo FxCop Çözümleyicileri için unity'nin kurallar hakkında en güncel listesi vardır. Bu sayfa ayrıca kural varsayılan olarak etkin olup olmadığı ve ilişkili olup olmadığını gibi ek bilgileri olan *kod düzeltme*. ([Kod düzeltme](../ide/quick-actions.md) ampul simgesini menüsünde Visual Studio'da tek tıklamayla düzeltmeleri kullanılabilir.)

Bu sayfadaki tarih itibariyle FxCop listesini kuralları için taşınmıştır [FxCop Çözümleyicileri](install-fxcop-analyzers.md) içerir:

Kural Kimliği | Başlık
--------|---------
[CA1000](ca1000-do-not-declare-static-members-on-generic-types.md) | Genel türlerde statik üyeler belirtme
[CA1001](ca1001-types-that-own-disposable-fields-should-be-disposable.md) | Atılabilen alanlara sahip türler atılabilir olmalıdır
[CA1003](ca1003-use-generic-event-handler-instances.md) | Genel olay işleyicisi örnekleri kullan
[CA1008](ca1008-enums-should-have-zero-value.md) | Sabit listelerinin sıfır değeri olmalıdır
[CA1010](ca1010-collections-should-implement-generic-interface.md) | Koleksiyonlar genel arabirimi uygulamalıdır
[CA1012](ca1012-abstract-types-should-not-have-constructors.md) | Soyut türlerin oluşturucuları olmamalıdır
[CA1014](ca1014-mark-assemblies-with-clscompliantattribute.md) | Derlemeleri CLSCompliant ile işaretleyin
[CA1016](ca1016-mark-assemblies-with-assemblyversionattribute.md) | Derlemeleri derleme sürümü ile işaretleyin
[CA1017](ca1017-mark-assemblies-with-comvisibleattribute.md) | Derlemeleri ComVisible ile işaretleyin
[CA1018](ca1018-mark-attributes-with-attributeusageattribute.md) | Öznitelikleri AttributeUsageAttribute ile işaretle
[CA1019](ca1019-define-accessors-for-attribute-arguments.md) | Öznitelik bağımsız değişkenleri için erişimciler tanımlayın
[CA1024](ca1024-use-properties-where-appropriate.md) | Uygun yerlerde özellikleri kullanın
[CA1027](ca1027-mark-enums-with-flagsattribute.md) | Sabit listelerini FlagsAttribute ile işaretleyin
[CA1028](ca1028-enum-storage-should-be-int32.md) | Numaralandırma depolaması Int32 olmalıdır
[CA1030](ca1030-use-events-where-appropriate.md) | Uygun yerlerde olayları kullanın
[CA1031](ca1031-do-not-catch-general-exception-types.md) | Genel özel durum türlerini yakalamayın
[CA1032](ca1032-implement-standard-exception-constructors.md) | Standart özel durum oluşturucularını uygulayın
[CA1033](ca1033-interface-methods-should-be-callable-by-child-types.md) | Arabirim metotları alt türler tarafından çağrılabilmelidir
[CA1034](ca1034-nested-types-should-not-be-visible.md) | İç içe türler görünür olmamalıdır
[CA1036](ca1036-override-methods-on-comparable-types.md) | Karşılaştırılabilir türlerde metotları geçersiz kıl
[CA1040](ca1040-avoid-empty-interfaces.md) | Boş arabirimlerden kaçının
[CA1041](ca1041-provide-obsoleteattribute-message.md) | ObsoleteAttribute iletisi sağla
[CA1043](ca1043-use-integral-or-string-argument-for-indexers.md) | Integral veya dize bağımsız değişkeni için dizin oluşturucular kullanma
[CA1044](ca1044-properties-should-not-be-write-only.md) | Özellikler salt yazılır olmamalıdır
[CA1050](ca1050-declare-types-in-namespaces.md) | Ad alanlarında türler bildirin
[CA1051](ca1051-do-not-declare-visible-instance-fields.md) | Görünür örnek alanlarını bildirmeyin
[CA1052](ca1052-static-holder-types-should-be-sealed.md) | Static tutucu türler statik veya NotInheritable (bu tablodan sonraki nota bakın)
[CA1053](ca1053-static-holder-types-should-not-have-constructors.md) | Static tutucu türler (bu tablodan sonraki nota bakın) oluşturucular bulunmamalıdır
[CA1054](ca1054-uri-parameters-should-not-be-strings.md) | URI parametreleri dizeler olmamalıdır
[CA1055](ca1055-uri-return-values-should-not-be-strings.md) | URI dönüş değerleri dizeler olmamalıdır
[CA1056](ca1056-uri-properties-should-not-be-strings.md) | URI özellikleri dizeler olmamalıdır
[CA1058](ca1058-types-should-not-extend-certain-base-types.md) | Türler belirli temel türleri aşmamalıdır
[CA1060](ca1060-move-p-invokes-to-nativemethods-class.md) | Pinvokes yerel yöntemlerin sınıfına taşıyın
[CA1061](ca1061-do-not-hide-base-class-methods.md) | Temel sınıf metotlarını gizlemeyin
[CA1062](ca1062-validate-arguments-of-public-methods.md) | Genel metotların bağımsız değişkenlerini doğrulayın
[CA1063](ca1063-implement-idisposable-correctly.md) | IDisposable'ı doğru uygulayın
[CA1064](ca1064-exceptions-should-be-public.md) | Özel durumlar genel olmalıdır
[CA1065](ca1065-do-not-raise-exceptions-in-unexpected-locations.md) | Beklenmeyen konumlarda özel durum harekete geçirmeyin
CA1066 | Tür {0} IEquatable uygulamalıdır\<T > eşittir kıldığından
CA1067 | Object.Equals(object) IEquatable uygularken geçersiz kılma\<T >
CA1068 | CancellationToken parametreleri son gelmelidir
CA1200 | Cref etiket öneki ile kullanmaktan kaçının
[CA1303](ca1303-do-not-pass-literals-as-localized-parameters.md) | Harfleri yerelleştirilmiş parametreler olarak göndermeyin
[CA1304](ca1304-specify-cultureinfo.md) | CultureInfo belirt
[CA1305](ca1305-specify-iformatprovider.md) | IFormatProvider belirt
[CA1307](ca1307-specify-stringcomparison.md) | StringComparison belirt
[CA1308](ca1308-normalize-strings-to-uppercase.md) | Dizeleri büyük harfe normalleştirin
[CA1309](ca1309-use-ordinal-stringcomparison.md) | Sıra dize karşılaştırma kullan
[CA1401](ca1401-p-invokes-should-not-be-visible.md) | P/Invoke'lar görünür olmamalıdır
[CA1501](ca1501-avoid-excessive-inheritance.md) | Aşırı devralmadan kaçının
[CA1502](ca1502-avoid-excessive-complexity.md) | Aşırı karmaşıklıktan kaçının
[CA1505](ca1505-avoid-unmaintainable-code.md) | Bakımı yapılamayan kodlardan kaçının
[CA1506](ca1506-avoid-excessive-class-coupling.md) | Aşırı sınıf bağlantısından kaçının
[CA1507](ca1507.md) | Sembol adlarını ifade nameof kullanın
CA1508 | Kullanılmayan koşullu kodlardan kaçının
CA1509 | Kod ölçümleri kural belirtimi dosyasında geçersiz giriş
[CA1707](ca1707-identifiers-should-not-contain-underscores.md) | Tanımlayıcılar alt çizgi içermemelidir
[CA1708](ca1708-identifiers-should-differ-by-more-than-case.md) | Tanımlayıcılar yalnızca büyük küçük harfle birbirinden farklı olmamalıdır
[CA1710](ca1710-identifiers-should-have-correct-suffix.md) | Tanımlayıcılar doğru soneke sahip olmalıdır
[CA1711](ca1711-identifiers-should-not-have-incorrect-suffix.md) | Tanımlayıcılar yanlış sonek içermemelidir
[CA1712](ca1712-do-not-prefix-enum-values-with-type-name.md) | Sabit listesi değerlerine tür adını önek olarak eklemeyin
[CA1714](ca1714-flags-enums-should-have-plural-names.md) | Bayrak sabit listeleri çoğul adlara sahip olmalıdır
[CA1715](ca1715-identifiers-should-have-correct-prefix.md) | Tanımlayıcılar doğru ön eke sahip olmalıdır
[CA1716](ca1716-identifiers-should-not-match-keywords.md) | Tanımlayıcılar anahtar sözcükler ile eşleşmemelidir
[CA1717](ca1717-only-flagsattribute-enums-should-have-plural-names.md) | Yalnızca FlagsAttribute sabit listeleri çoğul adlara sahip olmalıdır
[CA1720](ca1720-identifiers-should-not-contain-type-names.md) | Tanımlayıcı türü adını içerir.
[CA1721 TÜR](ca1721-property-names-should-not-match-get-methods.md) | Özellik adları get metotları ile eşleşmemelidir
[CA1724](ca1724-type-names-should-not-match-namespaces.md) | Tür adları ad alanlarıyla eşleşmemelidir
[CA1725](ca1725-parameter-names-should-match-base-declaration.md) | Parametre adları temel bildirimle eşleşmemelidir
[CA1801](ca1801-review-unused-parameters.md) | Kullanılmayan parametreleri gözden geçirin
[CA1802](ca1802-use-literals-where-appropriate.md) | Uygun yerlerde sabitleri kullan
[CA1806](ca1806-do-not-ignore-method-results.md) | Metot sonuçlarını yoksaymayın
[CA1810](ca1810-initialize-reference-type-static-fields-inline.md) | Başvuru türü statik alanları satır içinden başlatın
[CA1812](ca1812-avoid-uninstantiated-internal-classes.md) | Örneklenmemiş iç sınıflardan kaçının
[CA1813](ca1813-avoid-unsealed-attributes.md) | Mühürsüz özniteliklerden kaçının
[CA1814](ca1814-prefer-jagged-arrays-over-multidimensional.md) | Çok boyutlu diziler yerine basit dizileri tercih edin
[CA1815](ca1815-override-equals-and-operator-equals-on-value-types.md) | Değer türlerinde eşittir ve işleç eşittiri geçersiz kılın
[CA1816](ca1816-call-gc-suppressfinalize-correctly.md) | Atma yöntemleri SuppressFinalize çağırmalıdır
[CA1819](ca1819-properties-should-not-return-arrays.md) | Özellikler diziler döndürmemelidir
[CA1820](ca1820-test-for-empty-strings-using-string-length.md) | Dize uzunluğunu kullanarak boş dizeleri test edin
[CA1821](ca1821-remove-empty-finalizers.md) | Boş Sonlandırıcıları kaldırın
[CA1822](ca1822-mark-members-as-static.md) | Üyeleri static olarak işaretleyin
[CA1823](ca1823-avoid-unused-private-fields.md) | Kullanılmayan özel alanlardan kaçının
[CA1824](ca1824-mark-assemblies-with-neutralresourceslanguageattribute.md) | Derlemeleri NeutralResourcesLanguageAttribute ile işaretleyin
CA1825 | Sıfır uzunluklu dizi ayırmaları kaçının.
CA1826 | Numaralandırılabilir yöntemleri dizinlenebilir koleksiyonlarda kullanmayın. Bunun yerine koleksiyonun doğrudan kullanın
[CA2000](ca2000-dispose-objects-before-losing-scope.md) | Kapsamı kaybetmeden önce nesneleri bırakın
[CA2002](ca2002-do-not-lock-on-objects-with-weak-identity.md) | Zayıf kimliği olan nesneleri kilitlemeyin
[CA2007](ca2007-do-not-directly-await-task.md) | Beklenen görev üzerinde ConfigureAwait çağırmayı düşünün
CA2008 | Görevleri bir TaskScheduler geçmeden oluşturmayın
CA2009 | Bir ImmutableCollection değerine ToImmutableCollection çağırmayın
CA2010 | PreserveSigAttribute ile işaretlenmiş yöntemler tarafından döndürülen değer her zaman kullanma
[CA2100](ca2100-review-sql-queries-for-security-vulnerabilities.md) | SQL sorgularını güvenlik açıkları için inceleyin
[CA2101](ca2101-specify-marshaling-for-p-invoke-string-arguments.md) | P/Invoke dize bağımsız değişkenleri için sıralama belirtin
[CA2119](ca2119-seal-methods-that-satisfy-private-interfaces.md) | Özel arabirimleri karşılayan metotları mühürleyin
[CA2153](ca2153-avoid-handling-corrupted-state-exceptions.md) | Bozuk durum özel yakalamayın
[CA2200](ca2200-rethrow-to-preserve-stack-details.md) | Yığın ayrıntılarını korumak için yeniden fırlatma.
[CA2201](ca2201-do-not-raise-reserved-exception-types.md) | Ayrılmış özel durum türlerini harekete geçirmeyin
[CA2207](ca2207-initialize-value-type-static-fields-inline.md) | Değer türü statik alanları satır içi başlatın
[CA2208](ca2208-instantiate-argument-exceptions-correctly.md) | Bağımsız değişken özel durumlarını doğru örnekleyin
[CA2211](ca2211-non-constant-fields-should-not-be-visible.md) | Sabit olmayan alanlar görünür olmamalıdır
[CA2213](ca2213-disposable-fields-should-be-disposed.md) | Atılabilen alanlar atılmalıdır
[CA2214](ca2214-do-not-call-overridable-methods-in-constructors.md) | Geçersiz kılınabilir metotları oluşturucular içinde çağırmayın
[CA2216](ca2216-disposable-types-should-declare-finalizer.md) | Atılabilir türler sonlandırıcıyı bildirmelidir
[CA2217](ca2217-do-not-mark-enums-with-flagsattribute.md) | Sabit listelerini FlagsAttribute ile işaretlemeyin
[CA2218](ca2218-override-gethashcode-on-overriding-equals.md) | GetHashCode'u Eşittir'i geçersiz kılarak geçersiz kılın
[CA2219](ca2219-do-not-raise-exceptions-in-exception-clauses.md) | Finally yan tümceleri içinde özel durum harekete geçirmeyin
[CA2224](ca2224-override-equals-on-overloading-operator-equals.md) | Geçersiz kılma eşittir işlecini aşırı yüklerken equals
[CA2225](ca2225-operator-overloads-have-named-alternates.md) | İşleç aşırı yüklemeleri adlandırılmış alternatiflere sahiptir
[CA2226](ca2226-operators-should-have-symmetrical-overloads.md) | İşleçler simetrik aşırı yüklemelere sahip olmalıdır
[CA2227](ca2227-collection-properties-should-be-read-only.md) | Koleksiyon özellikleri salt okunur olmalıdır
[CA2229](ca2229-implement-serialization-constructors.md) | Serileştirme oluşturucularını uygulayın
[CA2231](ca2231-overload-operator-equals-on-overriding-valuetype-equals.md) | Equals değeri geçersiz kılarak aşırı eşittir işlecini yazın
[CA2234](ca2234-pass-system-uri-objects-instead-of-strings.md) | Sistem dizeler yerine URI nesneleri geçirin.
[CA2235](ca2235-mark-all-non-serializable-fields.md) | Tüm serileştirilebilir olmayan alanları işaretleyin
[CA2237](ca2237-mark-iserializable-types-with-serializableattribute.md) | Seri hale getirilebilir ile işareti ISerializable türler
[CA2241](ca2241-provide-correct-arguments-to-formatting-methods.md) | Biçimlendirme metotlarına doğru bağımsız değişkenleri sağlayın
[CA2242](ca2242-test-for-nan-correctly.md) | NaN için doğru test edin
[CA2243](ca2243-attribute-string-literals-should-parse-correctly.md) | Öznitelik dize harfleri doğru çözümlenmelidir
CA2244 | Dizinlenmiş öğeye başlatmalar yinelenen değil
[CA2300](ca2300-do-not-use-insecure-deserializer-binaryformatter.md) | Güvenli olmayan seri durumdan çıkarıcı BinaryFormatter kullanmayın
[CA2301](ca2301-do-not-call-binaryformatter-deserialize-without-first-setting-binaryformatter-binder.md) | İlk olarak BinaryFormatter.Binder öğesini ayarlamadan önce BinaryFormatter.Deserialize çağırmayın
[CA2302](ca2302-ensure-binaryformatter-binder-is-set-before-calling-binaryformatter-deserialize.md) | BinaryFormatter.Deserialize çağırmadan önce BinaryFormatter.Binder öğesinin ayarlandığından emin olun
[CA2305](ca2305-do-not-use-insecure-deserializer-losformatter.md) | Güvenli olmayan seri kaldırıcı LosFormatter kullanmayın
[CA2310](ca2310-do-not-use-insecure-deserializer-netdatacontractserializer.md) | Güvenli olmayan seri kaldırıcı NetDataContractSerializer kullanmayın
[CA2311](ca2311-do-not-deserialize-without-first-setting-netdatacontractserializer-binder.md) | İlk olarak NetDataContractSerializer.Binder öğesini ayarlamadan seri durumdan çıkarmayın
[CA2312](ca2312-ensure-netdatacontractserializer-binder-is-set-before-deserializing.md) | Seri durumdan çıkarmadan önce NetDataContractSerializer.Binder öğesinin ayarlandığından emin olun
[CA2315](ca2315-do-not-use-insecure-deserializer-objectstateformatter.md) | Güvenli olmayan seri kaldırıcı ObjectStateFormatter kullanmayın
[CA2321](ca2321.md) | SimpleTypeResolver kullanarak JavaScriptSerializer ile seri durumdan çıkarmayın
[CA2322](ca2322.md) | Seri durumdan çıkarmadan önce SimpleTypeResolver ile JavaScriptSerializer’ın başlatılmadığından emin olun
[CA3001](ca3001-review-code-for-sql-injection-vulnerabilities.md) | SQL ekleme güvenlik açıkları için inceleme kodu
[CA3002](ca3002-review-code-for-xss-vulnerabilities.md) | XSS güvenlik açıkları için inceleme kodu
[CA3003](ca3003-review-code-for-file-path-injection-vulnerabilities.md) | Dosya yolu ekleme güvenlik açıkları için inceleme kodu
[CA3004](ca3004-review-code-for-information-disclosure-vulnerabilities.md) | Bilgilerin açığa çıkmasıyla ilgili güvenlik açıkları için inceleme kodu
[CA3005](ca3005-review-code-for-ldap-injection-vulnerabilities.md) | LDAP ekleme güvenlik açıkları için inceleme kodu
[CA3006](ca3006-review-code-for-process-command-injection-vulnerabilities.md) | İşlem komutu ekleme güvenlik açıkları için inceleme kodu
[CA3007](ca3007-review-code-for-open-redirect-vulnerabilities.md) | Açık yeniden yönlendirme güvenlik açıkları için inceleme kodu
[CA3008](ca3008-review-code-for-xpath-injection-vulnerabilities.md) | XPath ekleme güvenlik açıkları için inceleme kodu
[CA3009](ca3009-review-code-for-xml-injection-vulnerabilities.md) | XML ekleme güvenlik açıkları için inceleme kodu
[CA3010](ca3010-review-code-for-xaml-injection-vulnerabilities.md) | XAML ekleme güvenlik açıkları için inceleme kodu
[CA3011](ca3011-review-code-for-dll-injection-vulnerabilities.md) | DLL ekleme güvenlik açıkları için inceleme kodu
[CA3012](ca3012-review-code-for-regex-injection-vulnerabilities.md) | Normal ifade ekleme güvenlik açıkları için inceleme kodu
CA3061 | URL'ye göre şema eklemeyin
[CA3075](ca3075-insecure-dtd-processing.md) | XML işleme güvensiz DTD
[CA3076](ca3076-insecure-xslt-script-execution.md) | Güvensiz XSLT betiği işleme.
[CA3077](ca3077-insecure-processing-in-api-design-xml-document-and-xml-text-reader.md) | API tasarımı ve XmlDocument XmlTextReader güvensiz işleme
[CA3147](ca3147-mark-verb-handlers-with-validateantiforgerytoken.md) | İşareti fiili işleyicilerle Antiforgery belirtecini doğrula
[CA5350](ca5350-do-not-use-weak-cryptographic-algorithms.md) | Zayıf Şifreleme Algoritmaları Kullanmayın
[CA5351](ca5351-do-not-use-broken-cryptographic-algorithms.md) | Bozuk şifreleme algoritmaları kullanmayın
CA5358 | Güvenli olmayan şifreleme modları kullanmayın
CA5359 | Sertifika doğrulaması devre dışı bırakmayın
CA5360 | Tehlikeli yöntemleri seri durumundan çıkarma içinde çağırmayın
CA5361 | SChannel güçlü şifreleme kullanımını devre dışı bırakmayın
CA5362 | Kendi kendine seri hale getirilebilir bir sınıf içinde Başvurmayın
CA5363 | İstek doğrulamanın devre dışı bırakmayın
CA5364 | Kullanım dışı güvenlik protokollerini kullanmayın
CA5365 | HTTP üstbilgisi denetimi devre dışı bırakmayın
CA5366 | XmlReader için veri kümesini okuma Xml kullanma
CA5367 | İşaretçi alanlara sahip türler seri hale getirmek değil
CA5368 | ViewStateUserKey sayfasından türetilmiş sınıflar için ayarlayın
CA5369 | XmlReader Deserialize için kullanın.
CA5370 | XmlReader okuyucu doğrulamak için kullanın.
CA5371 | XmlReader şema okuma için kullanın.
CA5372 | XmlReader XPathDocument için kullanın.
CA5373 | Geçersiz anahtar türetme işlevi kullanmayın
CA5374 | XslTransform kullanmayın
CA5375 | Hesap paylaşılan erişim imzası kullanmayın
CA5376 | SharedAccessProtocol HttpsOnly kullanın
CA5377 | Kapsayıcı düzeyinde erişim ilkesi kullanın
CA5378 | ServicePointManagerSecurityProtocols devre dışı bırakmayın
CA5379 | Zayıf anahtar türetme işlevi algoritması kullanmayın
CA9999 | Çözümleyici sürüm uyuşmazlığı

> [!NOTE]
> Kuralları CA1052 ve özgün FxCop uygulamasından CA1053 tek bir kural, CA1052, FxCop Çözümleyicileri içinde birleştirilir.

## <a name="unported-rules"></a>Unported kuralları

İçin unity'nin edilmemiş bir kural kümesinin [FxCop Çözümleyicileri](install-fxcop-analyzers.md) henüz yapmadıysanız, ancak hala kuralları içeren [unity'nin](#rules-that-may-be-ported)hem de kullanım dışıdır ve [taşınmasınıolmayacaktır](#deprecated-rules).

### <a name="rules-that-may-be-ported"></a>Unity'nin kuralları

Aşağıdaki FxCop statik kod analizi kuralları Çözümleyicileri henüz uygulamadığınız, ancak yine de olabilir. Bu bir engelleyen teknik neden nedeniyle ya da yalnızca kural daha düşük bir öncelik olduğundan emin olabilir. Her kural taşıma durumu hakkında daha fazla bilgi için bağlantıya tıklayın **sorun izleme** sütun.

Kural Kimliği | Sorun izleme
--- | ---
[CA1002](ca1002-do-not-expose-generic-lists.md) | [https://github.com/dotnet/roslyn-analyzers/issues/369](https://github.com/dotnet/roslyn-analyzers/issues/369)
[CA1004](ca1004-generic-methods-should-provide-type-parameter.md) | [https://github.com/dotnet/roslyn-analyzers/issues/370](https://github.com/dotnet/roslyn-analyzers/issues/370)
[CA1005](ca1005-avoid-excessive-parameters-on-generic-types.md) | [https://github.com/dotnet/roslyn-analyzers/issues/371](https://github.com/dotnet/roslyn-analyzers/issues/371)
[CA1006](ca1006-do-not-nest-generic-types-in-member-signatures.md) | [https://github.com/dotnet/roslyn-analyzers/issues/372](https://github.com/dotnet/roslyn-analyzers/issues/372)
[CA1007](ca1007-use-generics-where-appropriate.md) | [https://github.com/dotnet/roslyn-analyzers/issues/373](https://github.com/dotnet/roslyn-analyzers/issues/373)
[CA1011](ca1011-consider-passing-base-types-as-parameters.md) | [https://github.com/dotnet/roslyn-analyzers/issues/375](https://github.com/dotnet/roslyn-analyzers/issues/375)
[CA1021](ca1021-avoid-out-parameters.md) | [https://github.com/dotnet/roslyn-analyzers/issues/377](https://github.com/dotnet/roslyn-analyzers/issues/377)
[CA1023](ca1023-indexers-should-not-be-multidimensional.md) | [https://github.com/dotnet/roslyn-analyzers/issues/378](https://github.com/dotnet/roslyn-analyzers/issues/378)
[CA1045](ca1045-do-not-pass-types-by-reference.md) | [https://github.com/dotnet/roslyn-analyzers/issues/391](https://github.com/dotnet/roslyn-analyzers/issues/391)
[CA1046](ca1046-do-not-overload-operator-equals-on-reference-types.md) | [https://github.com/dotnet/roslyn-analyzers/issues/392](https://github.com/dotnet/roslyn-analyzers/issues/392)
[CA1047](ca1047-do-not-declare-protected-members-in-sealed-types.md) | [https://github.com/dotnet/roslyn-analyzers/issues/393](https://github.com/dotnet/roslyn-analyzers/issues/393)
[CA1048](ca1048-do-not-declare-virtual-members-in-sealed-types.md) | [https://github.com/dotnet/roslyn-analyzers/issues/394](https://github.com/dotnet/roslyn-analyzers/issues/394)
[CA1049](ca1049-types-that-own-native-resources-should-be-disposable.md) | [https://github.com/dotnet/roslyn-analyzers/issues/395](https://github.com/dotnet/roslyn-analyzers/issues/395)
[CA1057](ca1057-string-uri-overloads-call-system-uri-overloads.md) | [https://github.com/dotnet/roslyn-analyzers/issues/401](https://github.com/dotnet/roslyn-analyzers/issues/401)
[CA1300](ca1300-specify-messageboxoptions.md) | [https://github.com/dotnet/roslyn-analyzers/issues/408](https://github.com/dotnet/roslyn-analyzers/issues/408)
[CA1301](ca1301-avoid-duplicate-accelerators.md) | [https://github.com/dotnet/roslyn-analyzers/issues/409](https://github.com/dotnet/roslyn-analyzers/issues/409)
[CA1306](ca1306-set-locale-for-data-types.md) | [https://github.com/dotnet/roslyn-analyzers/issues/414](https://github.com/dotnet/roslyn-analyzers/issues/414)
[CA1402](ca1402-avoid-overloads-in-com-visible-interfaces.md) | [https://github.com/dotnet/roslyn-analyzers/issues/418](https://github.com/dotnet/roslyn-analyzers/issues/418)
[CA1403](ca1403-auto-layout-types-should-not-be-com-visible.md) | [https://github.com/dotnet/roslyn-analyzers/issues/419](https://github.com/dotnet/roslyn-analyzers/issues/419)
[CA1404](ca1404-call-getlasterror-immediately-after-p-invoke.md) | [https://github.com/dotnet/roslyn-analyzers/issues/420](https://github.com/dotnet/roslyn-analyzers/issues/420)
[CA1405](ca1405-com-visible-type-base-types-should-be-com-visible.md) | [https://github.com/dotnet/roslyn-analyzers/issues/421](https://github.com/dotnet/roslyn-analyzers/issues/421)
[CA1407](ca1407-avoid-static-members-in-com-visible-types.md) | [https://github.com/dotnet/roslyn-analyzers/issues/423](https://github.com/dotnet/roslyn-analyzers/issues/423)
[CA1408](ca1408-do-not-use-autodual-classinterfacetype.md) | [https://github.com/dotnet/roslyn-analyzers/issues/424](https://github.com/dotnet/roslyn-analyzers/issues/424)
[CA1409](ca1409-com-visible-types-should-be-creatable.md) | [https://github.com/dotnet/roslyn-analyzers/issues/425](https://github.com/dotnet/roslyn-analyzers/issues/425)
[CA1410](ca1410-com-registration-methods-should-be-matched.md) | [https://github.com/dotnet/roslyn-analyzers/issues/426](https://github.com/dotnet/roslyn-analyzers/issues/426)
[CA1411](ca1411-com-registration-methods-should-not-be-visible.md) | [https://github.com/dotnet/roslyn-analyzers/issues/427](https://github.com/dotnet/roslyn-analyzers/issues/427)
[CA1412](ca1412-mark-comsource-interfaces-as-idispatch.md) | [https://github.com/dotnet/roslyn-analyzers/issues/428](https://github.com/dotnet/roslyn-analyzers/issues/428)
[CA1413](ca1413-avoid-non-public-fields-in-com-visible-value-types.md) | [https://github.com/dotnet/roslyn-analyzers/issues/429](https://github.com/dotnet/roslyn-analyzers/issues/429)
[CA1414](ca1414-mark-boolean-p-invoke-arguments-with-marshalas.md) | [https://github.com/dotnet/roslyn-analyzers/issues/430](https://github.com/dotnet/roslyn-analyzers/issues/430)
[CA1415](ca1415-declare-p-invokes-correctly.md) | [https://github.com/dotnet/roslyn-analyzers/issues/431](https://github.com/dotnet/roslyn-analyzers/issues/431)
[CA1500](ca1500-variable-names-should-not-match-field-names.md) | [https://github.com/dotnet/roslyn-analyzers/issues/432](https://github.com/dotnet/roslyn-analyzers/issues/432)
[CA1600](ca1600-do-not-use-idle-process-priority.md) | [https://github.com/dotnet/roslyn-analyzers/issues/438](https://github.com/dotnet/roslyn-analyzers/issues/438)
[CA1601](ca1601-do-not-use-timers-that-prevent-power-state-changes.md) | [https://github.com/dotnet/roslyn-analyzers/issues/439](https://github.com/dotnet/roslyn-analyzers/issues/439)
[CA1700](ca1700-do-not-name-enum-values-reserved.md) | [https://github.com/dotnet/roslyn-analyzers/issues/440](https://github.com/dotnet/roslyn-analyzers/issues/440)
[CA1704](ca1704-identifiers-should-be-spelled-correctly.md) | [https://github.com/dotnet/roslyn-analyzers/issues/443](https://github.com/dotnet/roslyn-analyzers/issues/443)
[CA1709](ca1709-identifiers-should-be-cased-correctly.md) | [https://github.com/dotnet/roslyn-analyzers/issues/445](https://github.com/dotnet/roslyn-analyzers/issues/445)
[CA1713](ca1713-events-should-not-have-before-or-after-prefix.md) | [https://github.com/dotnet/roslyn-analyzers/issues/449](https://github.com/dotnet/roslyn-analyzers/issues/449)
[CA1719](ca1719-parameter-names-should-not-match-member-names.md) | [https://github.com/dotnet/roslyn-analyzers/issues/453](https://github.com/dotnet/roslyn-analyzers/issues/453)
[CA1722](ca1722-identifiers-should-not-have-incorrect-prefix.md) | [https://github.com/dotnet/roslyn-analyzers/issues/455](https://github.com/dotnet/roslyn-analyzers/issues/455)
[CA1726](ca1726-use-preferred-terms.md) | [https://github.com/dotnet/roslyn-analyzers/issues/458](https://github.com/dotnet/roslyn-analyzers/issues/458)
[CA1804](ca1804-remove-unused-locals.md) | [https://github.com/dotnet/roslyn-analyzers/issues/461](https://github.com/dotnet/roslyn-analyzers/issues/461)
[CA1811](ca1811-avoid-uncalled-private-code.md) | [https://github.com/dotnet/roslyn-analyzers/issues/464](https://github.com/dotnet/roslyn-analyzers/issues/464)
[CA1900](ca1900-value-type-fields-should-be-portable.md) | [https://github.com/dotnet/roslyn-analyzers/issues/474](https://github.com/dotnet/roslyn-analyzers/issues/474)
[CA2001](ca2001-avoid-calling-problematic-methods.md) | [https://github.com/dotnet/roslyn-analyzers/issues/477](https://github.com/dotnet/roslyn-analyzers/issues/477)
[CA2004](ca2004-remove-calls-to-gc-keepalive.md) | [https://github.com/dotnet/roslyn-analyzers/issues/479](https://github.com/dotnet/roslyn-analyzers/issues/479)
[CA2006](ca2006-use-safehandle-to-encapsulate-native-resources.md) | [https://github.com/dotnet/roslyn-analyzers/issues/480](https://github.com/dotnet/roslyn-analyzers/issues/480)
[CA2109](ca2109-review-visible-event-handlers.md) | [https://github.com/dotnet/roslyn-analyzers/issues/488](https://github.com/dotnet/roslyn-analyzers/issues/488)
[CA2204](ca2204-literals-should-be-spelled-correctly.md) | [https://github.com/dotnet/roslyn-analyzers/issues/529](https://github.com/dotnet/roslyn-analyzers/issues/529)
[CA2205](ca2205-use-managed-equivalents-of-win32-api.md) | [https://github.com/dotnet/roslyn-analyzers/issues/530](https://github.com/dotnet/roslyn-analyzers/issues/530)
[CA2212](ca2212-do-not-mark-serviced-components-with-webmethod.md) | [https://github.com/dotnet/roslyn-analyzers/issues/534](https://github.com/dotnet/roslyn-analyzers/issues/534)
[CA2215](ca2215-dispose-methods-should-call-base-class-dispose.md) | [https://github.com/dotnet/roslyn-analyzers/issues/535](https://github.com/dotnet/roslyn-analyzers/issues/535)
[CA2232](ca2232-mark-windows-forms-entry-points-with-stathread.md) | [https://github.com/dotnet/roslyn-analyzers/issues/545](https://github.com/dotnet/roslyn-analyzers/issues/545)
[CA2236](ca2236-call-base-class-methods-on-iserializable-types.md) | [https://github.com/dotnet/roslyn-analyzers/issues/548](https://github.com/dotnet/roslyn-analyzers/issues/548)
[CA2238](ca2238-implement-serialization-methods-correctly.md) | [https://github.com/dotnet/roslyn-analyzers/issues/549](https://github.com/dotnet/roslyn-analyzers/issues/549)
[CA2239](ca2239-provide-deserialization-methods-for-optional-fields.md) | [https://github.com/dotnet/roslyn-analyzers/issues/550](https://github.com/dotnet/roslyn-analyzers/issues/550)
[CA2240](ca2240-implement-iserializable-correctly.md) | [https://github.com/dotnet/roslyn-analyzers/issues/551](https://github.com/dotnet/roslyn-analyzers/issues/551)

### <a name="deprecated-rules"></a>Kullanım dışı bırakılan kuralları

Aşağıdaki FxCop statik kod analizi kuralları kullanım dışıdır ve çözümleyiciler uygulanan olmaz. Daha fazla bilgi için kural Kimliğine göre arama yapabilirsiniz (örneğin, **CA1009**) üzerinde [roslyn Çözümleyicileri GitHub sorunlar sayfasında](https://github.com/dotnet/roslyn-analyzers/issues?utf8=%E2%9C%93&q=is:issue+label:FxCop-Port).

- [CA1009](ca1009-declare-event-handlers-correctly.md)
- [CA1020](ca1020-avoid-namespaces-with-few-types.md)
- [CA1025](ca1025-replace-repetitive-arguments-with-params-array.md)
- [CA1026](ca1026-default-parameters-should-not-be-used.md)
- [CA1035](ca1035-icollection-implementations-have-strongly-typed-members.md)
- [CA1038](ca1038-enumerators-should-be-strongly-typed.md)
- [CA1039](ca1039-lists-are-strongly-typed.md)
- [CA1059](ca1059-members-should-not-expose-certain-concrete-types.md)
- [CA1302](ca1302-do-not-hardcode-locale-specific-strings.md)
- [CA1400](ca1400-p-invoke-entry-points-should-exist.md)
- [CA1406](ca1406-avoid-int64-arguments-for-visual-basic-6-clients.md)
- [CA1504](ca1504-review-misleading-field-names.md)
- [CA1701](ca1701-resource-string-compound-words-should-be-cased-correctly.md)
- [CA1702](ca1702-compound-words-should-be-cased-correctly.md)
- [CA1703](ca1703-resource-strings-should-be-spelled-correctly.md)
- [CA1800](ca1800-do-not-cast-unnecessarily.md)
- [CA1809](ca1809-avoid-excessive-locals.md)
- [CA1901](ca1901-p-invoke-declarations-should-be-portable.md)
- [CA1903](ca1903-use-only-api-from-targeted-framework.md)
- [CA2003](ca2003-do-not-treat-fibers-as-threads.md)
- [CA2102](ca2102-catch-non-clscompliant-exceptions-in-general-handlers.md)
- [CA2103](ca2103-review-imperative-security.md)
- [CA2104](ca2104-do-not-declare-read-only-mutable-reference-types.md)
- [CA2105](ca2105-array-fields-should-not-be-read-only.md)
- [CA2106](ca2106-secure-asserts.md)
- [CA2107](ca2107-review-deny-and-permit-only-usage.md)
- [CA2108](ca2108-review-declarative-security-on-value-types.md)
- [CA2111](ca2111-pointers-should-not-be-visible.md)
- [CA2112](ca2112-secured-types-should-not-expose-fields.md)
- [CA2114](ca2114-method-security-should-be-a-superset-of-type.md)
- [CA2115](ca2115-call-gc-keepalive-when-using-native-resources.md)
- [CA2116](ca2116-aptca-methods-should-only-call-aptca-methods.md)
- [CA2117](ca2117-aptca-types-should-only-extend-aptca-base-types.md)
- [CA2118](ca2118-review-suppressunmanagedcodesecurityattribute-usage.md)
- [CA2120](ca2120-secure-serialization-constructors.md)
- [CA2121](ca2121-static-constructors-should-be-private.md)
- [CA2122](ca2122-do-not-indirectly-expose-methods-with-link-demands.md)
- [CA2123](ca2123-override-link-demands-should-be-identical-to-base.md)
- [CA2124](ca2124-wrap-vulnerable-finally-clauses-in-outer-try.md)
- [CA2126](ca2126-type-link-demands-require-inheritance-demands.md)
- [CA2130](ca2130-security-critical-constants-should-be-transparent.md)
- [CA2131](ca2131-security-critical-types-may-not-participate-in-type-equivalence.md)
- [CA2132](ca2132-default-constructors-must-be-at-least-as-critical-as-base-type-default-constructors.md)
- [CA2133](ca2133-delegates-must-bind-to-methods-with-consistent-transparency.md)
- [CA2134](ca2134-methods-must-keep-consistent-transparency-when-overriding-base-methods.md)
- [CA2135](ca2135-level-2-assemblies-should-not-contain-linkdemands.md)
- [CA2136](ca2136-members-should-not-have-conflicting-transparency-annotations.md)
- [CA2137](ca2137-transparent-methods-must-contain-only-verifiable-il.md)
- [CA2138](ca2138-transparent-methods-must-not-call-methods-with-the-suppressunmanagedcodesecurity-attribute.md)
- [CA2139](ca2139-transparent-methods-may-not-use-the-handleprocesscorruptingexceptions-attribute.md)
- [CA2140](ca2140-transparent-code-must-not-reference-security-critical-items.md)
- [CA2141](ca2141-transparent-methods-must-not-satisfy-linkdemands.md)
- [CA2142](ca2142-transparent-code-should-not-be-protected-with-linkdemands.md)
- [CA2143](ca2143-transparent-methods-should-not-use-security-demands.md)
- [CA2144](ca2144-transparent-code-should-not-load-assemblies-from-byte-arrays.md)
- [CA2145](ca2145-transparent-methods-should-not-be-decorated-with-the-suppressunmanagedcodesecurityattribute.md)
- [CA2146](ca2146-types-must-be-at-least-as-critical-as-their-base-types-and-interfaces.md)
- [CA2147](ca2147-transparent-methods-may-not-use-security-asserts.md)
- [CA2149](ca2149-transparent-methods-must-not-call-into-native-code.md)
- [CA2151](ca2151-fields-with-critical-types-should-be-security-critical.md)
- [CA2202](ca2202-do-not-dispose-objects-multiple-times.md)
- [CA2210](ca2210-assemblies-should-have-valid-strong-names.md)
- [CA2220](ca2220-finalizers-should-call-base-class-finalizer.md)
- [CA2221](ca2221-finalizers-should-be-protected.md)
- [CA2222](ca2222-do-not-decrease-inherited-member-visibility.md) ([gerekçe](https://github.com/dotnet/roslyn-analyzers/issues/1378))
- [CA2223](ca2223-members-should-differ-by-more-than-return-type.md)
- [CA2228](ca2228-do-not-ship-unreleased-resource-formats.md)
- [CA2230](ca2230-use-params-for-variable-arguments.md)
- [CA2233](ca2233-operations-should-not-overflow.md)
- [CA5122](ca5122-p-invoke-declarations-should-not-be-safe-critical.md)

## <a name="see-also"></a>Ayrıca bkz.

- [Microsoft.CodeAnalysis.FxCopAnalyzers kuralları](https://github.com/dotnet/roslyn-analyzers/blob/master/src/Microsoft.CodeAnalysis.FxCopAnalyzers/Microsoft.CodeAnalysis.FxCopAnalyzers.md)
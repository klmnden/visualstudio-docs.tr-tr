---
title: Kullanım Uyarıları
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- vs.codeanalysis.usagerules
helpviewer_keywords:
- warnings, usage
- managed code analysis warnings, usage warnings
- usage warnings
ms.assetid: fe7dc2a3-289d-4bf7-a1e4-0947a81287c4
author: gewarren
ms.author: gewarren
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 53e7c0232406462a4c5938fd3f971189c9b2daca
ms.sourcegitcommit: 12f2851c8c9bd36a6ab00bf90a020c620b364076
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/06/2019
ms.locfileid: "66745074"
---
# <a name="usage-warnings"></a>Kullanım Uyarıları

Kullanım uyarıları .NET doğru kullanımını destekler.

## <a name="in-this-section"></a>Bu Bölümde

|Kural|Açıklama|
|----------|-----------------|
|[CA1801: Kullanılmayan parametreleri gözden geçir](../code-quality/ca1801-review-unused-parameters.md)|Yöntem imzası, yöntemin gövdesinde kullanılmayan bir parametre içerir.|
|[CA1806: Yöntem sonuçlarını yoksaymayın](../code-quality/ca1806-do-not-ignore-method-results.md)|Yeni bir nesne oluşturulur, ancak hiç kullanılmaz veya çağrılan yeni dizeyi oluşturur ve döndürür ve yeni dize hiç kullanılmaz ya da COM veya P/Invoke yöntemi, bir HRESULT ya da hiç kullanılmayan hata kodu döndürür.|
|[CA1816: GC çağırın. IDisposable.Dispose doğru](../code-quality/ca1816-call-gc-suppressfinalize-correctly.md)|Dispose uygulamasını bir yöntemi, GC çağırmaz. IDisposable.Dispose; ya da GC Dispose uygulamasını değil bir yöntemi çağırır. IDisposable.Dispose; ya da GC yöntemi çağırır. IDisposable.Dispose ve bu (Visual Basic'te Me) dışında bir şey geçirir.|
|[CA2200: Yığın ayrıntılarını korumak için yeniden fırlatma](../code-quality/ca2200-rethrow-to-preserve-stack-details.md)|Tekrar fırlatılan bir özel durum ve fırlatma açıklamasında açıkça belirtilen özel durum. Bir özel durum throw deyiminde özel durum belirterek yeniden fırlatılırsa yöntem listesi özel durum döndüren özgün yöntem ile kaybolan geçerli yöntem arasında çağırır.|
|[CA2201: Ayrılmış özel durum türlerini harekete geçirmeyin](../code-quality/ca2201-do-not-raise-reserved-exception-types.md)|Bu özgün hata algılama ve hata ayıklamayı sabit hale getirir.|
|[CA2202: Nesneleri birden çok kez atmayın](../code-quality/ca2202-do-not-dispose-objects-multiple-times.md)|Yöntem uygulaması, aynı nesne üzerinde System.IDisposable.Dispose veya bir Dispose eşdeğer (örneğin, bazı türleri üzerinde Close() yöntemi) için birden fazla çağrı kodu yolları içerir.|
|[CA2204: Değişmez değerler doğru yazılmalıdır](../code-quality/ca2204-literals-should-be-spelled-correctly.md)|Bir yöntemin gövdesi içinde hazır bilgi dizesi Microsoft yazım denetimi kitaplığı tarafından tanınmayan bir veya birkaç sözcük içerir.|
|[CA2205: Win32 API'sının yönetilen eşdeğerlerini kullanın](../code-quality/ca2205-use-managed-equivalents-of-win32-api.md)|Bir platform çağırma yöntemi tanımlanır ve bir .NET yöntemiyle eşdeğer bir işlevselliği kullanılabilir.|
|[CA2207: Değer türü statik alanları satır içi başlatın](../code-quality/ca2207-initialize-value-type-static-fields-inline.md)|Bir değer türü açık bir statik oluşturucu bildirir. Bu kural ihlalini düzeltmek için bildirildiğinde, tüm statik veriyi başlatın ve statik oluşturucuyu kaldırın.|
|[CA2208: Bağımsız değişken özel durumlarını doğru örnekleyin](../code-quality/ca2208-instantiate-argument-exceptions-correctly.md)|Varsayılan (parametresiz) kurucu veya ArgumentException türeyen özel bir durum türü için çağrı yapılır veya hatalı dize bağımsız değişkeni parametreli bir kurucu veya ArgumentException türeyen bir özel durum türü iletilir.|
|[CA2211: Sabit olmayan alanlar görünür olmamalıdır](../code-quality/ca2211-non-constant-fields-should-not-be-visible.md)|Söz konusu olan sabit veya salt okunur olan statik alanlar iş parçacığı güvenli değildir. Böyle bir alana erişim dikkatli bir şekilde denetlenebilir ve sınıf nesnesi erişimi eşitlemek için Gelişmiş programlama tekniklerini gerektirir.|
|[CA2212: Servis verilen bileşenleri WebMethod ile işaretlemeyin](../code-quality/ca2212-do-not-mark-serviced-components-with-webmethod.md)|System.EnterpriseServices.ServicedComponent'dan devralan türde bir yöntem System.Web.Services.WebMethodAttribute ile işaretlenir. WebMethodAttribute ve bir ServicedComponent yönteminin çakışan davranışları ve bağlam ve işlem akışı için gereksinimleri olduğu için, bazı senaryolarda yöntemin davranışı yanlış olacaktır.|
|[CA2213: Atılabilen alanlar atılmalıdır](../code-quality/ca2213-disposable-fields-should-be-disposed.md)|IDisposable uygulayan türlerin alanları System.IDisposable uygulayan bir türle bildirilir. Bir Dispose yöntemi alanının tanıtıcısının bildirim türü Dispose yöntemi tarafından çağrılmaz.|
|[CA2214: Geçersiz kılınabilir yöntemleri oluşturucular içinde çağırmayın](../code-quality/ca2214-do-not-call-overridable-methods-in-constructors.md)|Bir kurucu sanal bir yöntemi çağırdığında, yapıcı yöntemini çağıran örneği için değil yürütüldü mümkündür.|
|[CA2215: Atma yöntemleri taban sınıf atmayı çağırmalıdır](../code-quality/ca2215-dispose-methods-should-call-base-class-dispose.md)|Tür atılabilen bir türden devralınırsa, kendi Dispose yönteminden basit tür olan Dispose yöntemini çağırmalıdır.|
|[CA2216: Atılabilir türler sonlandırıcıyı bildirmelidir](../code-quality/ca2216-disposable-types-should-declare-finalizer.md)|System.IDisposable uygulayan yöntem ve yönetilmeyen kaynakların kullanımını öneren alanlar sahip bir tür tarafından Object.Finalize açıklandığı bir sonlandırıcı uygulamıyor.|
|[CA2217: Sabit listelerini FlagsAttribute ile işaretlemeyin](../code-quality/ca2217-do-not-mark-enums-with-flagsattribute.md)|Dışarıdan görünen bir numaralandırma FlagsAttribute ile işaretlenmiş ve iki ya da numaralandırma üzerinde tanımlanan diğer değerlerin bir birleşimi tabanların olmayan bir veya daha fazla değerleri vardır.|
|[CA2218: Gethashcode'u eşittir geçersiz kılmada geçersiz kıl](../code-quality/ca2218-override-gethashcode-on-overriding-equals.md)|GetHashCode, karma algoritmalar ve karma tablolar gibi veri yapıları için uygun olan geçerli örneği temel alan bir değer döndürür. Aynı türdeki ve eşit olan iki nesnenin aynı karma kodu döndürmesi gerekir.|
|[CA2219: Özel durum yan tümceleri içinde özel durum harekete geçirmeyin](../code-quality/ca2219-do-not-raise-exceptions-in-exception-clauses.md)|Bir istisna sonlandırıcı ya da arıza yan tümcesine neden olduğunda, yeni istisna aktif istisnayı saklar. Filtre yan tümcesinde bir özel durum ortaya çıktığında, çalışma zamanı özel durumu sessizce yakalar. Bu özgün hata algılama ve hata ayıklamayı sabit hale getirir.|
|[CA2220: Sonlandırıcılar taban Sonlandırıcıları çağırmalıdır](../code-quality/ca2220-finalizers-should-call-base-class-finalizer.md)|Sonlandırılma, devralma hiyerarşisi aracılığıyla gönderilmelidir. Bunu güvence altına almak için, türler basit sınıflarının kendi Finalize yönteminde Finalize yöntemini çağırmalıdır.|
|[CA2221: Sonlandırıcılar korunmalıdır](../code-quality/ca2221-finalizers-should-be-protected.md)|Sonlandırıcılar aile erişim değiştiricisi kullanmalıdır.|
|[CA2222: Devralınan üye görünürlüğünü azaltmayın](../code-quality/ca2222-do-not-decrease-inherited-member-visibility.md)|Erişim değiştiricisi devralınan üyeler için değişmez. Devralınmış bir üyeyi özel olarak değiştirme, arayanların yöntemin temel sınıf uygulamasına erişmesini engellemez.|
|[CA2223: Üyeler dönüş türünden daha fazla tarafından farklı olmalıdır](../code-quality/ca2223-members-should-differ-by-more-than-return-type.md)|Ortak dil çalışma zamanı, aynı üyeler arasında ayrım yapmak için dönüş türleri kullanımına izin verir, ancak bu özelliği ne ortak dil belirtimi ne de .NET programlama dillerinin ortak özelliğidir.|
|[CA2224: Eşittir işlecini aşırı yüklemesi üzerinde geçersiz kılma değerine eşittir](../code-quality/ca2224-override-equals-on-overloading-operator-equals.md)|Ortak tür eşitlik işlecini uygular, ancak Object.equals'ı geçersiz kılmaz.|
|[CA2225: İşleç aşırı yüklemeleri adlandırılmış Alternatiflere sahiptir](../code-quality/ca2225-operator-overloads-have-named-alternates.md)|Operatör aşırı yüklemesi bulundu ve beklenen adlandırılmış alternatif yöntem bulunamadı. Adlandırılmış alternatif üye işleci ile aynı işlevlere erişim sağlar ve aşırı yüklenmiş operatörlere destek olmayan dilleri içinde program geliştiriciler için sağlanır.|
|[CA2226: İşleçler simetrik aşırı yüklemelere sahip olmalıdır](../code-quality/ca2226-operators-should-have-symmetrical-overloads.md)|Bir tür, eşitlik ya da eşitsizlik operatörünü uygular ve ters işleci uygulamaz.|
|[CA2227: Koleksiyon Özellikleri salt okunur olmalıdır](../code-quality/ca2227-collection-properties-should-be-read-only.md)|Yazılabilir koleksiyon özelliği kullanıcının koleksiyonun tamamını farklı bir koleksiyonla değiştirmesine izin verir. Salt okunur özelliği değiştirilmesini durdurur ancak yine de tekil üyelerin ayarlamasına izin verir.|
|[CA2228: Yayımlanmamış kaynak biçimlerini yollamayın](../code-quality/ca2228-do-not-ship-unreleased-resource-formats.md)|Yayın öncesi .NET sürümleri kullanılarak oluşturulan kaynak dosyaları .NET desteklenen sürümleri tarafından kullanılamayabilir.|
|[CA2229: Serileştirme oluşturucularını uygulayın](../code-quality/ca2229-implement-serialization-constructors.md)|Bu kural ihlalini düzeltmek için seri hale getirme yapıcısını uygular. Kapalı bir sınıf için kurucusunu özel yapın; aksi takdirde korunmuş yapın.|
|[CA2230: Değişken bağımsız değişkenler için params kullanın](../code-quality/ca2230-use-params-for-variable-arguments.md)|Ortak veya korumalı tür VarArgs çağırma kuralı params anahtar sözcüğünü kullanan bir ortak veya korumalı yöntem içerir.|
|[CA2231: Eşittir işlecini ValueType.equals'ı geçersiz kılarak üzerinde](../code-quality/ca2231-overload-operator-equals-on-overriding-valuetype-equals.md)|Bir değer türü geçersiz kılmalar `Object.Equals` ama eşitlik işlecini uygulamaz.|
|[CA2232: İşareti Windows Forms giriş noktalarını STAThread ile işaretleyin](../code-quality/ca2232-mark-windows-forms-entry-points-with-stathread.md)|STAThreadAttribute, COM uygulama modelinin tek bir iş parçacıklı grup olduğunu gösterir. Bu öznitelik Windows Forms kullanan herhangi bir uygulamanın girişinde sunulur; atlanırsa, Windows bileşenleri doğru çalışmayabilir.|
|[CA2233: İşlemler taşmamalıdır](../code-quality/ca2233-operations-should-not-overflow.md)|Aritmetik işlemler işleminin sonucu dahil veri türleri için olası değerler aralığının dışında olduğundan emin olmak için işlenenleri doğrulamadan gerçekleştirilmemelidir.|
|[CA2234: Dizeler yerine System.Uri nesneleri geçirin](../code-quality/ca2234-pass-system-uri-objects-instead-of-strings.md)|Adında "URI", "URI", "urn", "urn", "url" veya "url" içeren bir dize parametresi olan yöntem çağrısı yapıldı.  Bildirim türü yöntemi, System.Uri parametresini aşırı yüklemeye uyan yöntemi içerir.|
|[CA2235: Tüm serileştirilebilir olmayan alanları işaretleyin](../code-quality/ca2235-mark-all-non-serializable-fields.md)|Seri hale getirilemeyen bir örnek alan türü seri hale getirilebilir bir tür içinde bildirilir.|
|[CA2236: ISerializable türler üzerinde taban sınıf yöntemlerini çağırın](../code-quality/ca2236-call-base-class-methods-on-iserializable-types.md)|Bu kural ihlalini düzeltmek için, taban türü GetObjectData yöntemini veya karşılık gelen türetilmiş yöntemden ya da oluşturucudan serileştirme oluşturucusunu çağırın.|
|[CA2237: İşareti ISerializable türleri SerializableAttribute ile işaretleyin](../code-quality/ca2237-mark-iserializable-types-with-serializableattribute.md)|Türü ISerializable arabirimini uygulaması aracılığıyla bir özel seri hale getirme yordamı kullansa bile ortak dil çalışma zamanı tarafından seri hale getirilebilir olarak tanınması için türleri SerializableAttribute özniteliği ile işaretlenmelidir.|
|[CA2238: Serileştirme yöntemlerini doğru uygulama](../code-quality/ca2238-implement-serialization-methods-correctly.md)|Seri hale getirme olayı tanıtan yöntem türü, doğru imzaya, dönüş türüne veya görünürlüğe sahip değil.|
|[CA2239: İsteğe bağlı alanlar için seri halden çıkarma yöntemleri sağlar.](../code-quality/ca2239-provide-deserialization-methods-for-optional-fields.md)|System.Runtime.Serialization.OptionalFieldAttribute özniteliği ile işaretlenmiş bir alana bir türe sahip ve tür, yöntemlerinin yönetilmesi serinin olayını sağlamaz.|
|[CA2240: ISerializable'ı doğru uygulayın](../code-quality/ca2240-implement-iserializable-correctly.md)|Bu kural ihlalini düzeltmek için GetObjectData yöntemi geçersiz kılınabilir yapın ve tüm örnek alanları seri hale getirme işlemine dahil veya açıkça NonSerializedAttribute özniteliği ile işaretlenmiş olduğundan emin olun.|
|[CA2241: Biçimlendirme yöntemlerine doğru bağımsız değişkenleri sağlayın](../code-quality/ca2241-provide-correct-arguments-to-formatting-methods.md)|System.String.Format için geçirilen biçim bağımsız değişken her nesne değişkeni veya tam tersi karşılık gelen bir biçim öğesi içermiyor.|
|[CA2242: NaN için doğru sınayın](../code-quality/ca2242-test-for-nan-correctly.md)|Bu ifade, değeri Single.Nan veya Double.Nan'a karşı test eder. Single.IsNan(Single) ya da Double.IsNan(Double) değerini test etmek için kullanın.|
|[CA2243: Öznitelik dize harfleri doğru çözümlenmelidir](../code-quality/ca2243-attribute-string-literals-should-parse-correctly.md)|Bir öznitelik dize literal parametresi, URL, GUID ya da bir sürüm için doğru ayrıştırmaz.|
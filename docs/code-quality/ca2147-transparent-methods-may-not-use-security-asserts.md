---
title: 'CA2147: Saydam metotlar güvenlik onay deyimlerini kullanmamalıdır'
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- SecurityTransparentCodeShouldNotAssert
- CA2147
- CA2128
helpviewer_keywords:
- CA2128
- SecurityTransparentCodeShouldNotAssert
ms.assetid: 5d31e940-e599-4b23-9b28-1c336f8d910e
author: gewarren
ms.author: gewarren
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 8fa5a17e7ec1438f104c9bf2f746df26dd97ed51
ms.sourcegitcommit: 0c2523d975d48926dd2b35bcd2d32a8ae14c06d8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/24/2019
ms.locfileid: "71231963"
---
# <a name="ca2147-transparent-methods-may-not-use-security-asserts"></a>CA2147: Saydam metotlar güvenlik onay deyimlerini kullanmamalıdır

|||
|-|-|
|TypeName|SecurityTransparentCodeShouldNotAssert|
|CheckId|CA2147|
|Kategori|Microsoft.Security|
|Son değişiklik|Yeni|

## <a name="cause"></a>Sebep
Olarak <xref:System.Security.SecurityTransparentAttribute> işaretlenen koda, onay için yeterli izin verilmez.

## <a name="rule-description"></a>Kural açıklaması
Bu kural,% 100 saydam veya karışık/kritik bir derlemede bulunan tüm yöntemleri ve türleri analiz eder ve bildirim temelli ya da kesinlik kullanımını <xref:System.Security.CodeAccessPermission.Assert%2A>işaretler.

Çalışma zamanında, saydam koddan yapılan <xref:System.Security.CodeAccessPermission.Assert%2A> tüm çağrılar bir <xref:System.InvalidOperationException> oluşturulmasına neden olur. Bu, hem% 100 saydam derlemede hem de bir yöntem ya da türün saydam olarak bildirildiği, ancak bildirime dayalı veya zorunlu bir onay içeren karışık saydam/kritik derlemelerde meydana gelebilir.

.NET Framework 2,0, *Saydamlık*adlı bir özellik sunmuştur. Tek tek Yöntemler, alanlar, arabirimler, sınıflar ve türler saydam ya da kritik olabilir.

Saydam kodun güvenlik ayrıcalıklarını yükseltmesine izin verilmiyor. Bu nedenle, verilen veya talep edilen tüm izinler otomatik olarak kod aracılığıyla arayan veya ana bilgisayar uygulama etki alanına geçirilir. Yükseltme örnekleri, onaylar, linktaleplerini, SuppressUnmanagedCode ve `unsafe` Code içerir.

## <a name="how-to-fix-violations"></a>İhlalleri çözme
Sorunu çözmek için, onayı <xref:System.Security.SecurityCriticalAttribute>çağıran kodu işaretleyin ya da onayı kaldırın.

## <a name="when-to-suppress-warnings"></a>Uyarıların ne zaman bastırılamıyor
Bu kuraldan bir ileti bastırmayın.

## <a name="example"></a>Örnek
Bu kod, saydam ise `SecurityTestClass` , `Assert` Yöntem bir <xref:System.InvalidOperationException>oluşturduğunda başarısız olur.

[!code-csharp[FxCop.Security.CA2147.TransparentMethodsMustNotUseSecurityAsserts#1](../code-quality/codesnippet/CSharp/ca2147-transparent-methods-may-not-use-security-asserts_1.cs)]

## <a name="example"></a>Örnek
Bir seçenek, aşağıdaki örnekteki SecurityTransparentMethod yöntemini gözden geçirmeniz ve yöntemin yükseltme için güvenli olarak kabul edilmesi durumunda, güvenli-kritik ile SecurityTransparentMethod Mark. Bunun yapılması, yöntem üzerinde ayrıntılı, tam ve hata içermeyen bir güvenlik denetiminin, onay altındaki yöntemde gerçekleşen tüm çağrı aşımlarını birlikte gerçekleştirilmesi gerekir:

[!code-csharp[FxCop.Security.SecurityTransparentCode2#1](../code-quality/codesnippet/CSharp/ca2147-transparent-methods-may-not-use-security-asserts_2.cs)]

Diğer bir seçenek de koddan yapılan onayı kaldırmak ve sonraki dosya g/ç izin taleplerini, SecurityTransparentMethod ' nin çağıranına dışına akmasını sağlar. Bu, güvenlik denetimlerini mümkün bir şekilde sunar. Bu durumda, izin talepleri arayan ve/veya uygulama etki alanına akacağından, güvenlik denetimi gerekmez. İzin talepleri, güvenlik ilkesi, barındırma ortamı ve kod kaynağı izin onayları aracılığıyla yakından denetlenir.

## <a name="see-also"></a>Ayrıca bkz.
[Güvenlik Uyarıları](../code-quality/security-warnings.md)
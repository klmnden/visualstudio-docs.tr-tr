---
title: 'CA2100: SQL sorgularını güvenlik açıkları için inceleyin'
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- Review SQL queries for security vulnerabilities
- ReviewSqlQueriesForSecurityVulnerabilities
- CA2100
helpviewer_keywords:
- CA2100
- ReviewSqlQueriesForSecurityVulnerabilities
ms.assetid: 79670604-c02a-448d-9c0e-7ea0120bc5fe
author: gewarren
ms.author: gewarren
manager: jillfra
dev_langs:
- CPP
- CSharp
- VB
ms.workload:
- multiple
ms.openlocfilehash: 837abb051467135b6332b53b2c59e5016d3adff6
ms.sourcegitcommit: 0c2523d975d48926dd2b35bcd2d32a8ae14c06d8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/24/2019
ms.locfileid: "71233060"
---
# <a name="ca2100-review-sql-queries-for-security-vulnerabilities"></a>CA2100: SQL sorgularını güvenlik açıkları için inceleyin

|||
|-|-|
|TypeName|ReviewSqlQueriesForSecurityVulnerabilities|
|CheckId|CA2100|
|Kategori|Microsoft.Security|
|Son değişiklik|Kırılmamış|

## <a name="cause"></a>Sebep

Yöntemi, yöntemine dize <xref:System.Data.IDbCommand.CommandText%2A?displayProperty=fullName> bağımsız değişkeninden oluşturulan bir dize kullanarak özelliği ayarlar.

## <a name="rule-description"></a>Kural açıklaması

Bu kural, dize değişkeninin kullanıcı girişi içerdiğini varsayar. Kullanıcı girişi ile oluşturulan SQL komut dizesi, SQL enjeksiyon saldırılarına karşı savunmasız durumdadır. Bir SQL ekleme saldırısında, kötü niyetli bir Kullanıcı, bir sorgunun tasarımını değiştiren ve temel alınan veritabanına yetkisiz erişim elde eden bir giriş sağlar. Tipik teknikler, SQL sabit dize sınırlayıcısı olan tek tırnak işareti veya kesme işareti ekleme işlemini içerir; bir SQL yorumunu belirten iki tire; ve yeni bir komutun izlediği noktalı virgül. Kullanıcı girişi sorgunun bir parçası olmalıdır, saldırı riskini azaltmak için, verimlilik sırasıyla listelenen aşağıdakilerden birini kullanın.

- Saklı yordam kullanın.

- Parametreli bir komut dizesi kullanın.

- Komut dizesini oluşturmadan önce hem tür hem de içerik için Kullanıcı girişini doğrulayın.

Aşağıdaki .net türleri <xref:System.Data.IDbCommand.CommandText%2A> özelliği uygular veya bir dize bağımsız değişkeni kullanarak özelliği ayarlamış olan oluşturucular sağlar.

- <xref:System.Data.Odbc.OdbcCommand?displayProperty=fullName> ve <xref:System.Data.Odbc.OdbcDataAdapter?displayProperty=fullName>

- <xref:System.Data.OleDb.OleDbCommand?displayProperty=fullName> ve <xref:System.Data.OleDb.OleDbDataAdapter?displayProperty=fullName>

- <xref:System.Data.OracleClient.OracleCommand?displayProperty=fullName> ve <xref:System.Data.OracleClient.OracleDataAdapter?displayProperty=fullName>

- <xref:System.Data.SqlClient.SqlCommand?displayProperty=fullName> ve <xref:System.Data.SqlClient.SqlDataAdapter?displayProperty=fullName>

Bir türün ToString yöntemi açıkça veya sorgu dizesini oluşturmak için örtük olarak kullanıldığında bu kuralın ihlal edildiğini unutmayın. Bir örnek verilmiştir.

```csharp
int x = 10;
string query = "SELECT TOP " + x.ToString() + " FROM Table";
```

Kötü amaçlı bir Kullanıcı ToString () metodunu geçersiz kılabildiğinden kural ihlal edilir.

Ayrıca, ToString örtük olarak kullanıldığında kural da çiğnendir.

```csharp
int x = 10;
string query = String.Format("SELECT TOP {0} FROM Table", x);
```

## <a name="how-to-fix-violations"></a>İhlalleri çözme

Bu kuralın ihlalini onarmak için parametreli bir sorgu kullanın.

## <a name="when-to-suppress-warnings"></a>Uyarıların ne zaman bastırılamıyor

Komut metni herhangi bir kullanıcı girişi içermiyorsa, bu kuraldan bir uyarıyı gizlemek güvenlidir.

## <a name="example"></a>Örnek

Aşağıdaki örnek, kuralı ve parametreli bir `UnsafeQuery`komut dizesi kullanarak kuralı karşılayan `SaferQuery`yöntemini ihlal eden bir yöntemi gösterir.

[!code-vb[FxCop.Security.ReviewSqlQueries#1](../code-quality/codesnippet/VisualBasic/ca2100-review-sql-queries-for-security-vulnerabilities_1.vb)]
[!code-csharp[FxCop.Security.ReviewSqlQueries#1](../code-quality/codesnippet/CSharp/ca2100-review-sql-queries-for-security-vulnerabilities_1.cs)]
[!code-cpp[FxCop.Security.ReviewSqlQueries#1](../code-quality/codesnippet/CPP/ca2100-review-sql-queries-for-security-vulnerabilities_1.cpp)]

## <a name="see-also"></a>Ayrıca bkz.

- [Güvenliğe Genel Bakış](/dotnet/framework/data/adonet/security-overview)
---
title: 'CA5351: Bozuk Şifreleme Algoritmaları Kullanmayın'
ms.date: 11/04/2016
ms.topic: reference
ms.assetid: 483f51b3-e186-4433-b48e-5ca24a9a9c94
author: gewarren
ms.author: gewarren
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: f2729e74e3abf6be2ae5b17a836d920c1376decd
ms.sourcegitcommit: 0c2523d975d48926dd2b35bcd2d32a8ae14c06d8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/24/2019
ms.locfileid: "71236944"
---
# <a name="ca5351-do-not-use-broken-cryptographic-algorithms"></a>CA5351: Bozuk Şifreleme Algoritmaları Kullanmayın

|||
|-|-|
|TypeName|Donotusebrokencryptographicalgoritmaları|
|CheckId|CA5351|
|Kategori|Microsoft. Cryptography|
|Son değişiklik|Kırılmamış|

> [!NOTE]
> Bu uyarı en son 2015 Kasım tarihinde güncelleştirildi.

## <a name="cause"></a>Sebep

Ve gibi şifreleme algoritmaları <xref:System.Security.Cryptography.MD5> <xref:System.Security.Cryptography.DES> <xref:System.Security.Cryptography.RC2> gibi işlevleri karma hale getirebilir ve önemli risk oluşturabilir ve bu durum, deneme yanılma saldırıları gibi önemsiz saldırı teknikleriyle hassas bilgilerin açığa çıkmasına neden olabilir. karma çakışmaları.

Aşağıdaki şifreleme algoritmaları listesi, bilinen şifreleme saldırılarına tabidir. Şifreleme karma algoritması <xref:System.Security.Cryptography.MD5> , karma çakışma saldırılarına tabidir.  Bir karma çarpışması, kullanıma bağlı olarak, karma işlevinin benzersiz şifreleme çıktısına bağlı olan sistemlerde kimliğe bürünme, izinsiz değişiklik veya diğer saldırı türlerine yol açabilir. Şifreleme algoritmaları <xref:System.Security.Cryptography.DES> ve <xref:System.Security.Cryptography.RC2> şifrelenmiş verilerin istenmeden açıklanmasına neden olabilecek şifreleme saldırılarına tabidir.

## <a name="rule-description"></a>Kural açıklaması

Bozuk şifreleme algoritmaları güvenli olarak kabul edilmez ve kullanımları önerilmez. MD5 karma algoritması bilinen çakışma saldırılarına açıktır, ancak belirli güvenlik açığı kullanım bağlamına göre farklılık gösterir.  Veri bütünlüğünü sağlamak için kullanılan karma algoritmalar (örneğin, dosya imzası veya dijital sertifika) özellikle savunmasız.  Bu bağlamda, saldırganlar iki ayrı veri parça oluşturabilir. bu şekilde, kötü amaçlı veriler, karma değer değiştirilmeksizin veya ilişkili dijital imzayı geçersiz kılarak kötü amaçlı verilerle değiştirilebilir.

Şifreleme algoritmaları için:

- <xref:System.Security.Cryptography.DES>şifreleme, bir günden kısa bir sürede deneme yanılma olabilecek küçük bir anahtar boyutu içeriyor.

- <xref:System.Security.Cryptography.RC2>şifreleme, saldırganın tüm anahtar değerleri arasında matematik ilişkileri bulduğu ilgili anahtar saldırılarına açıktır.

Bu kural, kaynak kodundaki yukarıdaki şifreleme işlevlerinden herhangi birini bulduğunda tetiklenir ve kullanıcıya bir uyarı oluşturur.

## <a name="how-to-fix-violations"></a>İhlalleri çözme

Şifreleme daha güçlü seçenekleri kullanın:

- MD5 için, [SHA-2](/windows/desktop/SecCrypto/hash-and-signature-algorithms) ailesindeki karmaları kullanın (örneğin <xref:System.Security.Cryptography.SHA512> <xref:System.Security.Cryptography.SHA384> <xref:System.Security.Cryptography.SHA256>,,,).

- DES ve RC2 için şifreleme kullanın <xref:System.Security.Cryptography.Aes> .

## <a name="when-to-suppress-warnings"></a>Uyarıların ne zaman bastırılamıyor

Bir şifreleme uzmanı tarafından incelenmediği takdirde bu kuraldan bir uyarıyı bastırmayın.

## <a name="pseudo-code-examples"></a>Sözde kod örnekleri

Aşağıdaki sözde kod örnekleri, bu kural tarafından algılanan ve olası alternatifler gösterir.

### <a name="md5-hashing-violation"></a>MD5 karma Ihlali

```csharp
using System.Security.Cryptography;
...
var hashAlg = MD5.Create();
```

Çözümden

```csharp
using System.Security.Cryptography;
...
var hashAlg = SHA256.Create();
```

### <a name="rc2-encryption-violation"></a>RC2 şifreleme Ihlali

```csharp
using System.Security.Cryptography;
...
RC2 encAlg = RC2.Create();
```

Çözümden

```csharp
using System.Security.Cryptography;
...
using (AesManaged encAlg = new AesManaged())
{
  ...
}
```

### <a name="des-encryption-violation"></a>DES şifreleme Ihlali

```csharp
using System.Security.Cryptography;
...
DES encAlg = DES.Create();
```

Çözümden

```csharp
using System.Security.Cryptography;
...
using (AesManaged encAlg = new AesManaged())
{
  ...
}
```
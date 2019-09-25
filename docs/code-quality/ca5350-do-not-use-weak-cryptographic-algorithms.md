---
title: 'CA5350: Zayıf Şifreleme Algoritmaları Kullanmayın'
ms.date: 11/04/2016
ms.topic: reference
ms.assetid: 4c51bb8a-fcfa-46aa-ab61-634be84c4a7a
author: gewarren
ms.author: gewarren
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 4aecd052e86a4c0366a1a43cb985ad50ab8862d8
ms.sourcegitcommit: 0c2523d975d48926dd2b35bcd2d32a8ae14c06d8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/24/2019
ms.locfileid: "71236960"
---
# <a name="ca5350-do-not-use-weak-cryptographic-algorithms"></a>CA5350: Zayıf Şifreleme Algoritmaları Kullanmayın

|||
|-|-|
|TypeName|Donotuseweakcryptographicalgoritma|
|CheckId|CA5350|
|Kategori|Microsoft. Cryptography|
|Son değişiklik|Kırılmamış|

> [!NOTE]
> Bu uyarı en son 2015 Kasım tarihinde güncelleştirildi.

## <a name="cause"></a>Sebep

Ve gibi şifreleme algoritmaları <xref:System.Security.Cryptography.TripleDES> ve gibi karma algoritmalar <xref:System.Security.Cryptography.SHA1> <xref:System.Security.Cryptography.RIPEMD160> zayıf kabul edilir.

Bu şifreleme algoritmaları, daha modern karşılıklarıyla çok güvenlik güvencesi sağlamaz. Daha modern karma <xref:System.Security.Cryptography.SHA1> algoritmalardan daha az çakışma <xref:System.Security.Cryptography.RIPEMD160> sağlayan şifreleme algoritmaları. Şifreleme algoritması <xref:System.Security.Cryptography.TripleDES> , daha fazla modern şifreleme algoritmalarından daha az sayıda güvenlik sağlar.

## <a name="rule-description"></a>Kural açıklaması

Zayıf şifreleme algoritmaları ve karma işlevleri bugün çok sayıda nedenden dolayı kullanılır, ancak korudukları verilerin gizliliğini garanti etmek için kullanılmamalıdır.

Kural, koddaki 3DES, SHA1 veya RIPEMD160 algoritmaları bulduğunda tetiklenir ve kullanıcıya bir uyarı oluşturur.

## <a name="how-to-fix-violations"></a>İhlalleri çözme

Şifreleme daha güçlü seçenekleri kullanın:

- TripleDES şifrelemesi için şifreleme kullanın <xref:System.Security.Cryptography.Aes> .

- SHA1 veya RIPEMD160 karma işlevleri için [SHA-2](/windows/desktop/SecCrypto/hash-and-signature-algorithms) ailesinden (ör. <xref:System.Security.Cryptography.SHA512>, <xref:System.Security.Cryptography.SHA384>, <xref:System.Security.Cryptography.SHA256>) olanları kullanın.

## <a name="when-to-suppress-warnings"></a>Uyarıların ne zaman bastırılamıyor

Veriler için gereken koruma düzeyi bir güvenlik garantisi gerektirmiyorsa bu kuraldan bir uyarı gizleyin.

## <a name="pseudo-code-examples"></a>Sözde kod örnekleri

Bu yazma sırasında, aşağıdaki sözde kod örneği, bu kural tarafından algılanan kalıbı gösterir.

### <a name="sha-1-hashing-violation"></a>SHA-1 karma Ihlali

```csharp
using System.Security.Cryptography;
...
var hashAlg = SHA1.Create();
```

Çözümden

```csharp
using System.Security.Cryptography;
...
var hashAlg = SHA256.Create();
```

### <a name="ripemd160-hashing-violation"></a>RIPEMD160 karma Ihlali

```csharp
using System.Security.Cryptography;
...
var hashAlg = RIPEMD160Managed.Create();
```

Çözümden

```csharp
using System.Security.Cryptography;
...
var hashAlg = SHA256.Create();
```

### <a name="tripledes-encryption-violation"></a>TripleDES şifreleme Ihlali

```csharp
using System.Security.Cryptography;
...
using (TripleDES encAlg = TripleDES.Create())
{
  ...
}
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
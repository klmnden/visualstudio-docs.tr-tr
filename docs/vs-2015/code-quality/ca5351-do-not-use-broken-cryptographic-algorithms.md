---
title: 'Ca5351: Bozuk şifreleme algoritmaları kullanmayın | Microsoft Docs'
ms.date: 11/15/2016
ms.technology: vs-ide-code-analysis
ms.topic: reference
ms.assetid: 483f51b3-e186-4433-b48e-5ca24a9a9c94
caps.latest.revision: 12
author: gewarren
ms.author: gewarren
manager: wpickett
ms.openlocfilehash: 780745e2b4213d8fdd130fe03cac292b233c5b0c
ms.sourcegitcommit: 47eeeeadd84c879636e9d48747b615de69384356
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "63430675"
---
# <a name="ca5351-do-not-use-broken-cryptographic-algorithms"></a>CA5351: Bozuk Şifreleme Algoritmaları Kullanmayın
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

|||  
|-|-|  
|TypeName|DoNotUseBrokenCryptographicAlgorithms|  
|CheckId|CA5351|  
|Kategori|Microsoft.Cryptography|  
|Yeni Değişiklik|Bozucu olmayan|  
  
> [!NOTE]
> Bu uyarı, Kasım 2015 tarihinde güncelleştirildiği.  
  
## <a name="cause"></a>Sebep  
 İşlevleri gibi karma <xref:System.Security.Cryptography.MD5> ve şifreleme algoritmaları gibi <xref:System.Security.Cryptography.DES> ve <xref:System.Security.Cryptography.RC2> önemli risk getirebilir ve önemsiz saldırı teknikleri üzerinden hassas bilgiler açığa yanılma saldırıları gibi sonuçlanabilir ve karma çakışmaları.  
  
 Bilinen bir şifreleme saldırılarına maruz aşağıdaki şifreleme algoritmaları listede var. Şifreleme karma algoritması <xref:System.Security.Cryptography.MD5> karma çakışma saldırılarına maruz olduğu.  Kullanımınıza bağlı olarak, bir karma çakışması kimliğe bürünme, değiştirilmesine veya diğer tür saldırıları, bir karma işlevi şifreleme benzersiz çıktısını kullanan sistemlerinde neden olabilir. Şifreleme algoritmaları <xref:System.Security.Cryptography.DES> ve <xref:System.Security.Cryptography.RC2> şifrelenmiş verilerin istenmeyen açıklanmasıyla sonuçlanabilir şifreleme saldırılara maruz şunlardır.  
  
## <a name="rule-description"></a>Kural Tanımı  
 Bozuk şifreleme algoritmaları güvenli kabul edilmeyen ve bunların kullanılması önerilmez. Belirli güvenlik açığı kullanım bağlam göre farklılık gösterir ancak MD5 karma algoritması bilinen çakışma saldırılara açıktır.  (Örneğin, dosya imzası veya dijital sertifika) veri bütünlüğünü sağlamak için kullanılan karma algoritmaları özellikle savunmasızdır.  Zararsız veri kötü amaçlı veri ile karma değeri değiştirme veya ilişkili bir dijital imza geçersiz kılmalarını yerine kullanılabileceği gibi bu bağlamda, verilerinizin iki ayrı parçaları saldırganlar oluşturabilir.  
  
 Şifreleme algoritmaları için:  
  
- <xref:System.Security.Cryptography.DES> Şifreleme, daha az bir gün içinde deneme yanılma yoluyla yapılan zorla olabilir küçük bir anahtar boyutu içerir.  
  
- <xref:System.Security.Cryptography.RC2> Şifreleme ilgili anahtar saldırısına maruz burada saldırganın tüm anahtar değerleri matematiksel ilişkilerini bulur.  
  
  Bu kural kaynak kodunda yukarıdaki şifreleme işlevlerden herhangi birinin bulur ve kullanıcı için bir uyarı oluşturduğunda tetiklenir.  
  
## <a name="how-to-fix-violations"></a>İhlaller Nasıl Düzeltilir?  
 Şifreleme bakımından daha güçlü seçenekleri kullanın:  
  
- MD5 karmaları kullanın [SHA-2](https://msdn.microsoft.com/library/windows/desktop/aa382459.aspx) ailesi (örneğin <xref:System.Security.Cryptography.SHA512>, <xref:System.Security.Cryptography.SHA384>, <xref:System.Security.Cryptography.SHA256>).  
  
- DES ve RC2 <xref:System.Security.Cryptography.Aes> şifreleme.  
  
## <a name="when-to-suppress-warnings"></a>Uyarılar Bastırıldığında  
 Bu şifreleme bir uzmana göre gözden geçirilir sürece bu kuraldan bir uyarıyı bastırmayın.  
  
## <a name="pseudo-code-example"></a>Sözde kod örneği  
 Aşağıdaki sözde kod örneği, bu kural ve olası alternatifler tarafından algılanan düzeni göstermektedir.  
  
### <a name="md5-hashing-violation"></a>MD5 Karma ihlali  
  
```  
using System.Security.Cryptography;   
...   
var hashAlg = MD5.Create();  
  
```  
  
### <a name="solution"></a>Çözüm  
  
```  
using System.Security.Cryptography;   
...   
var hashAlg = SHA256.Create();  
  
```  
  
### <a name="rc2-encryption-violation"></a>RC2 Şifreleme ihlali  
  
```  
using System.Security.Cryptography;   
...    
RC2 encAlg = RC2.Create();  
  
```  
  
### <a name="solution"></a>Çözüm  
  
```  
using System.Security.Cryptography;   
...   
using (AesManaged encAlg = new AesManaged())   
{   
  ...   
}  
```  
  
### <a name="des-br-br-encryption-violation"></a>DES <br /><br />Şifreleme ihlali  
  
```  
using System.Security.Cryptography;   
...   
DES encAlg = DES.Create();  
  
```  
  
### <a name="solution"></a>Çözüm  
  
```  
using System.Security.Cryptography;   
...   
using (AesManaged encAlg = new AesManaged())   
{   
  ...   
}  
```
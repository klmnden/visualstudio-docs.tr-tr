---
title: 'CA5350: Zayıf şifreleme algoritmaları kullanmayın | Microsoft Docs'
ms.date: 11/15/2016
ms.technology: vs-ide-code-analysis
ms.topic: reference
ms.assetid: 4c51bb8a-fcfa-46aa-ab61-634be84c4a7a
caps.latest.revision: 11
author: gewarren
ms.author: gewarren
manager: wpickett
ms.openlocfilehash: 0f1aee9fb3790a5ba7b766eba22f2ec6420dacfd
ms.sourcegitcommit: 1fc6ee928733e61a1f42782f832ead9f7946d00c
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/22/2019
ms.locfileid: "60041775"
---
# <a name="ca5350-do-not-use-weak-cryptographic-algorithms"></a>CA5350: Zayıf Şifreleme Algoritmaları Kullanmayın
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

|||  
|-|-|  
|TypeName|DoNotUseWeakCryptographicAlgorithms|  
|CheckId|CA5350|  
|Kategori|Microsoft.Cryptography|  
|Yeni Değişiklik|Bozucu olmayan|  
  
> [!NOTE]
>  Bu uyarı, Kasım 2015 tarihinde güncelleştirildiği.  
  
## <a name="cause"></a>Sebep  
 Şifreleme algoritmaları gibi <xref:System.Security.Cryptography.TripleDES> ve karma algoritmaları gibi <xref:System.Security.Cryptography.SHA1> ve <xref:System.Security.Cryptography.RIPEMD160> zayıf olarak değerlendirilir.  
  
 Bu şifreleme algoritmaları kadar güvenlik güvencesi daha modern ortaklarınıza olarak sağlamaz. Şifreleme karma algoritmaları <xref:System.Security.Cryptography.SHA1> ve <xref:System.Security.Cryptography.RIPEMD160> daha modern karma algoritmaları daha az çakışma Direnci sağlayın. Şifreleme algoritması <xref:System.Security.Cryptography.TripleDES> daha az güvenlik bitten daha modern şifreleme algoritmaları sağlar.  
  
## <a name="rule-description"></a>Kural Tanımı  
 Zayıf şifreleme algoritmalarını ve karma işlevler bir dizi nedenden ötürü bugün kullanılır, ancak bunlar bunların koruduğu verilerin gizliliği güvence altına almak için kullanılmamalıdır.  
  
 Kural tetikler 3DES, SHA1 veya RIPEMD160 algoritmaları oluşturur ve kod içinde bulduğunda kullanıcıya bir uyarı.  
  
## <a name="how-to-fix-violations"></a>İhlaller Nasıl Düzeltilir?  
 Şifreleme bakımından daha güçlü seçenekleri kullanın:  
  
- TripleDES şifreleme için <xref:System.Security.Cryptography.Aes> şifreleme.  
  
- SHA1 veya RIPEMD160 karma işlevler için olanları içinde kullanmak [SHA-2](https://msdn.microsoft.com/library/windows/desktop/aa382459.aspx) ailesi (örneğin <xref:System.Security.Cryptography.SHA512>, <xref:System.Security.Cryptography.SHA384>, <xref:System.Security.Cryptography.SHA256>).  
  
## <a name="when-to-suppress-warnings"></a>Uyarılar Bastırıldığında  
 Verileri için gereken koruma düzeyini güvenlik garantisi gerekmiyorsa, bu kuraldan bir uyarıyı gizler.  
  
## <a name="pseudo-code-example"></a>Sözde kod örneği  
 Bu makalenin yazıldığı zaman itibariyle, aşağıdaki sözde kod örneği bu kural tarafından algılanan düzeni göstermektedir.  
  
### <a name="sha-1-hashing-violation"></a>SHA-1 karma ihlali  
  
```  
using System.Security.Cryptography;   
...   
var hashAlg = SHA1.Create();  
  
```  
  
### <a name="solution"></a>Çözüm  
  
```  
using System.Security.Cryptography;   
...   
var hashAlg = SHA256.Create();  
  
```  
  
### <a name="ripemd160-br-br-hashing-violation"></a>RIPEMD160 <br /><br />Karma ihlali  
  
```  
using System.Security.Cryptography;   
...   
var hashAlg = RIPEMD160Managed.Create();  
  
```  
  
### <a name="solution"></a>Çözüm  
  
```  
using System.Security.Cryptography;   
...   
var hashAlg = SHA256.Create();  
  
```  
  
### <a name="tripledes-encryption-violation"></a>TripleDES şifreleme ihlali  
  
```  
using System.Security.Cryptography;   
...    
using (TripleDES encAlg = TripleDES.Create())   
{   
  ...   
}  
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
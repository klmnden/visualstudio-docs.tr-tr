---
title: 'CA1702: Bileşik sözcüklerin büyük küçük harfleri doğru | Microsoft Docs'
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-code-analysis
ms.topic: reference
f1_keywords:
- CA1702
- CompoundWordsShouldBeCasedCorrectly
helpviewer_keywords:
- CA1702
- CompoundWordsShouldBeCasedCorrectly
ms.assetid: 05481245-7ad8-48c3-a456-3aa44b6160a6
caps.latest.revision: 21
author: gewarren
ms.author: gewarren
manager: wpickett
ms.openlocfilehash: 9f4844431215d952f03ab9acc3f11ab57644abde
ms.sourcegitcommit: 3201da3499051768ab59f492699a9049cbc5c3c6
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/22/2019
ms.locfileid: "58355214"
---
# <a name="ca1702-compound-words-should-be-cased-correctly"></a>CA1702: Bileşik sözcüklerin büyük küçük harfleri doğru olmalıdır
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Visual Studio ile ilgili en son belgeler için bkz. [CA1702: Bileşik sözcüklerin büyük küçük harfleri doğru](https://docs.microsoft.com/visualstudio/code-quality/ca1702-compound-words-should-be-cased-correctly) docs.microsoft.com'da.  
  
|||  
|-|-|  
|TypeName|CompoundWordsShouldBeCasedCorrectly|  
|CheckId|CA1702|  
|Kategori|Microsoft.Naming|  
|Yeni Değişiklik|En son ne zaman derlemelerini tetiklenir.<br /><br /> Bölünemez - tür parametrelerinde tetiklendiğinde.|  
  
## <a name="cause"></a>Sebep  
 Bir tanımlayıcının adı birden çok sözcük içerir ve en az bir kelimelerin sözcüklerden değil bir bileşik sözcük olarak görünür.  
  
## <a name="rule-description"></a>Kural Tanımı  
 Tanımlayıcı adı büyük/küçük harf üzerinde dayalı sözcükler bölündüğünü. Bitişik her iki word birleşimi, Microsoft Yazım kitaplığı tarafından denetlenir. Tanımlıysa, tanımlayıcı bir kural ihlali üretir. "CheckSum" ve "Checksum" ve "Multipart" sırasıyla yazılmalıdır "MultiPart" bir ihlaline neden bileşik sözcüklerin örnekleridir. Önceki yaygın kullanım nedeniyle, kurala birkaç özel durum oluşturulur ve birden fazla tek sözcük işaretlenmiş, "Araç çubuğu" ve "Dosya adı" gibi büyük/küçük harfleri olarak iki ayrı sözcükleri (Bu durumda, "Araç çubuğu" ve "Dosya adı").  
  
 Adlandırma kuralları, ortak dil çalışma zamanını hedefleyen kitaplıkları için genel bir bakış sağlar. Bu, yeni yazılım kitaplıkları için gereklidir ve kitaplık geliştirme yönetilen kodda uzmanlığına sahip olan kişi tarafından geliştirilmiştir müşterilerinizin size olan güvenini artırır öğrenme eğrisini azaltır.  
  
## <a name="how-to-fix-violations"></a>İhlaller Nasıl Düzeltilir?  
 Böylece bu sözcüklerden adını değiştirin.  
  
## <a name="when-to-suppress-warnings"></a>Uyarılar Bastırıldığında  
 Bileşik sözcük kısımlarını yazım sözlüğüyle tanınır ve amacı iki kelimeye kullanmaktır. Bu kuraldan bir uyarıyı bastırmak güvenlidir.  
  
## <a name="related-rules"></a>İlgili kuralları  
 [CA1701: Kaynak dize bileşik sözcüklerinin doğru yazılmalıdır](../code-quality/ca1701-resource-string-compound-words-should-be-cased-correctly.md)  
  
 [CA1709: Tanımlayıcılar doğru yazılmalıdır](../code-quality/ca1709-identifiers-should-be-cased-correctly.md)  
  
 [CA1708: Tanımlayıcılar örnekten daha fazla farklı olmalıdır](../code-quality/ca1708-identifiers-should-differ-by-more-than-case.md)  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Adlandırma kuralları](http://msdn.microsoft.com/library/fc076d66-9b5f-42d3-aa65-61d970c794a3)   
 [Büyük/Küçük Harf Kuralları](http://msdn.microsoft.com/library/4c4ea526-9203-486f-b72d-29d61c5b3c6d)

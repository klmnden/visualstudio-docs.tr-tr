---
title: 'CA1709: Tanımlayıcıları büyük/küçük harfleri doğru | Microsoft Docs'
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-code-analysis
ms.topic: reference
f1_keywords:
- IdentifiersShouldBeCasedCorrectly
- CA1709
helpviewer_keywords:
- CA1709
- IdentifiersShouldBeCasedCorrectly
ms.assetid: f633d1a7-4ca4-40ae-b207-ec571c5fb083
caps.latest.revision: 30
author: gewarren
ms.author: gewarren
manager: wpickett
ms.openlocfilehash: b447b111cedc30aa23f3aaad0fbc964a5d8a2bd2
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "68189171"
---
# <a name="ca1709-identifiers-should-be-cased-correctly"></a>CA1709: Tanımlayıcılar doğru büyük küçük harfe sahip olmalıdır
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Visual Studio ile ilgili en son belgeler için bkz. [CA1709: Tanımlayıcıları büyük/küçük harfleri doğru](https://docs.microsoft.com/visualstudio/code-quality/ca1709-identifiers-should-be-cased-correctly).  
  
|||  
|-|-|  
|TypeName|IdentifiersShouldBeCasedCorrectly|  
|CheckId|CA1709|  
|Kategori|Microsoft.Naming|  
|Yeni Değişiklik|-Derlemeler, ad alanlarını, türleri, üyeleri ve parametreleri oluştuğunda kesiliyor.<br /><br /> Bölünemez - genel tür parametrelerinde tetiklendiğinde.|  
  
## <a name="cause"></a>Sebep  
 Tanımlayıcı adı sözcüklerden değil.  
  
 \- veya -  
  
 İki harfli kısaltması tanımlayıcı adını içeren ve ikinci harf, küçük ise.  
  
 \- veya -  
  
 Bir tanımlayıcının adı bir kısaltma üç veya daha fazla büyük harf içeriyor.  
  
## <a name="rule-description"></a>Kural Tanımı  
 Adlandırma kuralları, ortak dil çalışma zamanını hedefleyen kitaplıkları için genel bir bakış sağlar. Bu, yeni yazılım kitaplıkları için gereklidir ve kitaplık geliştirme yönetilen kodda uzmanlığına sahip olan kişi tarafından geliştirilmiştir müşterilerinizin size olan güvenini artırır öğrenme eğrisini azaltır.  
  
 Kural gereği, parametre adları camel casing kullanır; ad alanı, tür ve üye adları Pascal kullanmak büyük/küçük harf. Ortası büyük küçük harfleri adı ilk harfini, küçük harf ve adında kalan bir kelimelerin ilk harfi büyük harf olan. "PacketSniffer", "ioFile" ve "fatalErrorCode" adlarını ortası büyük küçük harfleri örnekleridir. Pascal büyük küçük harfleri adı ilk harfi büyük harf olan ve adında kalan bir kelimelerin ilk harfi büyük harf olan. "PacketSniffer", "IOFile" ve "FatalErrorCode" Pascal büyük küçük harfleri adları örnekleridir.  
  
 Bu kural adı büyük/küçük harf üzerinde dayalı sözcükler ayıran ve herhangi iki harfli bir sözcük "İçinde" gibi yaygın iki harfli sözcükleri veya "My" bir listesiyle denetler. Bir eşleşme bulunmazsa, word, bir kısaltma olarak kabul edilir. Ayrıca, bu kural adı bir satır dört büyük harf ya da üç büyük harflerle adın sonuna bir satır içerdiğinde bir kısaltma bulduğu varsayar.  
  
 Kural gereği, tüm büyük harfleri iki harfli kısaltmalar kullanın ve üç veya daha fazla karakter kısaltmalar kullanın Pascal büyük/küçük harf. Aşağıdaki örnekler, bu adlandırma kuralını kullanır: 'DB', 'CR', 'Cpa' ve 'Ecma'. Aşağıdaki örnekler, kuralı ihlal ediyor: 'GÇ', 'XML' ve 'DoD' nonparameter adları, 'xp' ve 'cpl'.  
  
 Bu kural ihlalini neden özel harfleri 'ID'. 'Id' bir kısaltma değildir, ancak 'kimlik' kısaltmasıdır.  
  
## <a name="how-to-fix-violations"></a>İhlaller Nasıl Düzeltilir?  
 Böylece bu sözcüklerden adını değiştirin.  
  
## <a name="when-to-suppress-warnings"></a>Uyarılar Bastırıldığında  
 Adlandırma kurallarınıza varsa veya örneğin, bir şirket veya bir teknoloji adı uygun bir ad tanımlayıcısı temsil ediyorsa Bu uyarının gösterilmemesi güvenlidir.  
  
 Belirli koşulları kısaltmalar ve kısaltmalar de ekleyebilirsiniz, için Kod Analizi özel sözlük. Bu kural ihlalleri özel sözlükte belirtilen koşulları neden olmaz. Daha fazla bilgi için [nasıl yapılır: Kod çözümleme dizinini özelleştirme](../code-quality/how-to-customize-the-code-analysis-dictionary.md)  
  
## <a name="related-rules"></a>İlgili kuralları  
 [CA1708: Tanımlayıcılar örnekten daha fazla farklı olmalıdır](../code-quality/ca1708-identifiers-should-differ-by-more-than-case.md)

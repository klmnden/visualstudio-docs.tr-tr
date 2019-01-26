---
title: 'CA1709: Tanımlayıcılar doğru büyük küçük harfe sahip olmalıdır'
ms.date: 11/04/2016
ms.prod: visual-studio-dev15
ms.topic: reference
f1_keywords:
- IdentifiersShouldBeCasedCorrectly
- CA1709
helpviewer_keywords:
- CA1709
- IdentifiersShouldBeCasedCorrectly
ms.assetid: f633d1a7-4ca4-40ae-b207-ec571c5fb083
author: gewarren
ms.author: gewarren
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 8cc8ee2f406c858bc06427327a453542fbaed2a8
ms.sourcegitcommit: 2193323efc608118e0ce6f6b2ff532f158245d56
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/25/2019
ms.locfileid: "55037545"
---
# <a name="ca1709-identifiers-should-be-cased-correctly"></a>CA1709: Tanımlayıcılar doğru büyük küçük harfe sahip olmalıdır

|||
|-|-|
|TypeName|IdentifiersShouldBeCasedCorrectly|
|CheckId|CA1709|
|Kategori|Microsoft.Naming|
|Yeni Değişiklik|-Derlemeleri, ad alanları, türler, üyeler ve parametreler oluştuğunda kesiliyor.<br /><br /> Bölünemez - genel tür parametrelerinde tetiklendiğinde.|

## <a name="cause"></a>Sebep
 Tanımlayıcı adı sözcüklerden değil.

 \- veya -

 İki harfli kısaltması tanımlayıcı adını içeren ve ikinci harf, küçük ise.

 \- veya -

 Bir tanımlayıcının adı bir kısaltma üç veya daha fazla büyük harf içeriyor.

## <a name="rule-description"></a>Kural açıklaması
 Adlandırma kuralları, ortak dil çalışma zamanını hedefleyen kitaplıkları için genel bir bakış sağlar. Bu tutarlılık, yeni yazılım kitaplıkları için gerekli ve kitaplık geliştirme yönetilen kodda uzmanlığına sahip olan kişi tarafından geliştirilmiştir müşterilerinizin size olan güvenini artırır öğrenme eğrisini azaltır.

 Kural gereği, parametre adları camel casing ve ad alanı, tür kullanın, ve üye adları Pascal casing. Ortası büyük küçük harfleri adı ilk harfini, küçük harf ve adında kalan bir kelimelerin ilk harfi büyük harf olan. Ortası büyük küçük harfleri adları örnekleri `packetSniffer`, `ioFile`, ve `fatalErrorCode`. Pascal büyük küçük harfleri adı ilk harfi büyük harf olan ve adında kalan bir kelimelerin ilk harfi büyük harf olan. Adları Pascal büyük küçük harfleri örnekler `PacketSniffer`, `IOFile`, ve `FatalErrorCode`.

 Bu kural adı büyük/küçük harf üzerinde dayalı sözcükler ayıran ve herhangi iki harfli bir sözcük "İçinde" gibi yaygın iki harfli sözcükleri veya "My" bir listesiyle denetler. Bir eşleşme bulunmazsa, word, bir kısaltma olarak kabul edilir. Ayrıca, bu kural adı bir satır dört büyük harf ya da üç büyük harflerle adın sonuna bir satır içerdiğinde bir kısaltma bulduğu varsayar.

 Kural gereği, tüm büyük harfleri iki harfli kısaltmalar kullanın ve üç veya daha fazla karakter kısaltmalar kullanın Pascal büyük/küçük harf. Aşağıdaki örnekler, bu adlandırma kuralını kullanır: 'DB', 'CR', 'Cpa' ve 'Ecma'. Aşağıdaki örnekler, kuralı ihlal ediyor: 'GÇ', 'XML' ve 'DoD' olmayan parametre adları, 'xp' ve 'cpl'.

 Bu kural ihlalini neden özel harfleri 'ID'. 'Id' bir kısaltma değildir, ancak 'kimlik' kısaltmasıdır.

## <a name="how-to-fix-violations"></a>İhlaller nasıl düzeltilir?
 Böylece bu sözcüklerden adını değiştirin.

## <a name="when-to-suppress-warnings"></a>Uyarılar bastırıldığında
 Adlandırma kurallarınıza varsa veya örneğin, bir şirket veya bir teknoloji adı uygun bir ad tanımlayıcısı temsil ediyorsa Bu uyarının gösterilmemesi güvenlidir.

 Belirli koşulları kısaltmalar ve kısaltmalar de ekleyebilirsiniz, için Kod Analizi özel sözlük. Bu kural ihlalleri özel sözlükte belirtilen koşulları neden olmaz. Daha fazla bilgi için [nasıl yapılır: Kod çözümleme dizinini özelleştirme](../code-quality/how-to-customize-the-code-analysis-dictionary.md)

## <a name="related-rules"></a>İlgili kuralları
 [CA1708: Tanımlayıcılar örnekten daha fazla farklı olmalıdır](../code-quality/ca1708-identifiers-should-differ-by-more-than-case.md)
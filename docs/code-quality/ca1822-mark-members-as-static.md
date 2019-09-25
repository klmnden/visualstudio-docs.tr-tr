---
title: 'CA1822: Üyeleri static olarak işaretleyin'
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- MarkMembersAsStatic
- CA1822
helpviewer_keywords:
- MarkMembersAsStatic
- CA1822
ms.assetid: 743f0af7-41d1-4852-8d97-af0688b31118
author: gewarren
ms.author: gewarren
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 11f210b9d37f15b3ea92b92112e48eecd3c8b9e1
ms.sourcegitcommit: 0c2523d975d48926dd2b35bcd2d32a8ae14c06d8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/24/2019
ms.locfileid: "71233415"
---
# <a name="ca1822-mark-members-as-static"></a>CA1822: Üyeleri static olarak işaretleyin

|||
|-|-|
|TypeName|MarkMembersAsStatic|
|CheckId|CA1822|
|Kategori|Microsoft. Performance|
|Son değişiklik|Bozuk olmayan-üye, yaptığınız değişiklikten bağımsız olarak, derleme dışında görünür değilse. Parçalara ayırma olmayan bir üyeyi yalnızca `this` anahtar sözcüğü olan bir örnek üye olarak değiştirirseniz.<br /><br /> Parçalama-üyeyi bir örnek üyesinden statik üyeye değiştirirseniz ve derleme dışında görünür durumdaysa.|

## <a name="cause"></a>Sebep
Örnek verilerine erişmeyen bir üye statik olarak işaretlenmemiş (içinde [!INCLUDE[vbprvb](../code-quality/includes/vbprvb_md.md)]paylaşılan).

## <a name="rule-description"></a>Kural açıklaması
Örnek veri veya çağrı örnek yöntemlerinin erişmez üyeleri işaretlenebilir olarak statik (paylaşılan [!INCLUDE[vbprvb](../code-quality/includes/vbprvb_md.md)]). Yöntemleri statik olarak işaretledikten sonra, derleyici sanal olmayan arama sitelerini bu üyelere yayar. Sanal olmayan çağrı sitelerini yayma, geçerli nesne işaretçisinin null olmadığından emin olan her bir çağrı için çalışma zamanında bir denetim yapılmasını engeller. Bu, performansa duyarlı kod için ölçülebilir bir performans kazancı elde edebilir. Bazı durumlarda, geçerli nesne örneğine erişim hatası, doğruluk sorununu temsil eder.

## <a name="how-to-fix-violations"></a>İhlalleri çözme
Üyeyi statik (veya paylaşılan [!INCLUDE[vbprvb](../code-quality/includes/vbprvb_md.md)]) olarak işaretleyin ya da uygunsa Yöntem gövdesinde ' this '/' Me ' kullanın.

## <a name="when-to-suppress-warnings"></a>Uyarıların ne zaman bastırılamıyor
Daha önce sevk edilen kodun bir uyarı olması için bu kuraldan daha önce sevkedilme bir uyarı görüntülenmesini güvenlidir.

## <a name="related-rules"></a>İlgili kurallar
[CA1811 Çağrılmadı özel koddan kaçının](../code-quality/ca1811-avoid-uncalled-private-code.md)

[CA1812 Örneklenmemiş iç sınıflardan kaçının](../code-quality/ca1812-avoid-uninstantiated-internal-classes.md)

[CA1804 Kullanılmayan yerelleri kaldır](../code-quality/ca1804-remove-unused-locals.md)
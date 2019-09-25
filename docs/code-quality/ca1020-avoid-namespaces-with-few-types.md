---
title: 'CA1020: Az tür içeren ad alanlarından kaçının'
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- CA1020
- AvoidNamespacesWithFewTypes
helpviewer_keywords:
- CA1020
- AvoidNamespacesWithFewTypes
ms.assetid: 9cb272f6-a3ff-45af-b35d-70dea620b074
author: gewarren
ms.author: gewarren
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 6e5c50f607253304b05dd7ab9350646a0df05e70
ms.sourcegitcommit: 0c2523d975d48926dd2b35bcd2d32a8ae14c06d8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/24/2019
ms.locfileid: "71236239"
---
# <a name="ca1020-avoid-namespaces-with-few-types"></a>CA1020: Az tür içeren ad alanlarından kaçının

|||
|-|-|
|TypeName|AvoidNamespacesWithFewTypes|
|CheckId|CA1020|
|Kategori|Microsoft.Design|
|Son değişiklik|Yeni|

## <a name="cause"></a>Sebep

Genel ad alanı dışındaki bir ad alanı beşten az tür içerir.

## <a name="rule-description"></a>Kural açıklaması

Ad alanlarınızın her birinin mantıksal bir kuruluşa sahip olduğundan ve türleri çok seyrek doldurulmuş bir ad alanına koymak için geçerli bir nedenin bulunduğundan emin olun. Ad alanları Çoğu senaryoda birlikte kullanılan türleri içermelidir. Uygulamaları birbirini dışlıyor olduğunda türler ayrı ad alanlarında bulunmalıdır. Örneğin, <xref:System.Web.UI> ad alanı Web uygulamalarında kullanılan türleri içerir <xref:System.Windows.Forms> ve ad alanı, tabanlı uygulamalarda kullanılan [!INCLUDE[TLA#tla_mswin](../code-quality/includes/tlasharptla_mswin_md.md)]türleri içerir. Her iki ad alanı da Kullanıcı arabiriminin yönlerini denetleyen türlere sahip olsa da, bu türler aynı uygulamada kullanılmak üzere tasarlanmamıştır. Bu nedenle, ayrı ad alanlarında bulunur. Bir özelliğin bulunabilirliği arttığı için dikkatli bir ad alanı organizasyonu da yararlı olabilir. Ad alanı hiyerarşisini inceleyerek, kitaplık tüketicileri bir özelliği uygulayan türleri bulabilmelidir.

> [!NOTE]
> Tasarım zamanı türleri ve izinleri, bu kılavuza uyum sağlamak için diğer ad alanlarıyla birleştirilmemelidir. Bu türler, ana ad alanlarınızın altındaki kendi ad alanlarına aittir ve ad alanları sırasıyla `.Design` ve ile `.Permissions`bitmelidir.

## <a name="how-to-fix-violations"></a>İhlalleri çözme

Bu kuralın ihlalini onarmak için, yalnızca birkaç tür içeren ad alanlarını tek bir ad alanında birleştirmeyi deneyin.

## <a name="when-to-suppress-warnings"></a>Uyarıların ne zaman bastırılamıyor

Ad alanı diğer ad boşluklarınızın türleriyle kullanılan türler içermiyorsa, bu kuraldan bir uyarının görüntülenmesini güvenli hale gelir.
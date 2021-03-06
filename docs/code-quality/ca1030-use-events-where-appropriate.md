---
title: 'CA1030: Uygun yerlerde olayları kullanın'
ms.date: 03/11/2019
ms.topic: reference
f1_keywords:
- UseEventsWhereAppropriate
- CA1030
helpviewer_keywords:
- CA1030
- UseEventsWhereAppropriate
ms.assetid: ea051367-deeb-40f9-9b65-eb818f1e133a
author: gewarren
ms.author: gewarren
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 28d71fbfc10532f7c9420ea7e847ef4c29b88854
ms.sourcegitcommit: 0c2523d975d48926dd2b35bcd2d32a8ae14c06d8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/24/2019
ms.locfileid: "71236073"
---
# <a name="ca1030-use-events-where-appropriate"></a>CA1030: Uygun yerlerde olayları kullanın

|||
|-|-|
|TypeName|UseEventsWhereAppropriate|
|CheckId|CA1030|
|Kategori|Microsoft.Design|
|Son değişiklik|Kırılmamış|

## <a name="cause"></a>Sebep

Bir yöntem adı aşağıdakilerden biriyle başlar:

- Eklenti
- RemoveOn
- Ateş
- yükseltmek

Bu kural varsayılan olarak yalnızca dışarıdan görünen yöntemlere bakar, ancak bu [yapılandırılabilir](#configurability).

## <a name="rule-description"></a>Kural açıklaması

Bu kural, normalde olaylar için kullanılan adlara sahip yöntemleri algılar. Olaylar gözlemci veya yayımla-abone ol tasarım modelini izler; bir nesnedeki durum değişikliği diğer nesnelere iletilmesi gerektiğinde kullanılırlar. Bir yöntem açıkça tanımlanmış bir durum değişikliğine yanıt olarak çağrılırsa, yöntemi bir olay işleyicisi tarafından çağrılmalıdır. Yöntemi direkt olarak çağırmak yerine olayları yükselterek çağıran nesneler.

Bazı yaygın olay örnekleri, bir düğmeye tıklanması gibi bir kullanıcı eyleminin bir kod segmentinin yürütülmesine neden olduğu kullanıcı arabirimi uygulamalarında bulunur. .NET olay modeli, Kullanıcı arabirimleriyle sınırlı değildir. Durum değişikliklerini bir veya daha fazla nesnede iletmelisiniz her yerde kullanılmalıdır.

## <a name="how-to-fix-violations"></a>İhlalleri çözme

Bir nesnenin durumu değiştiğinde yöntemi çağrılırsa, tasarımı .NET olay modelini kullanacak şekilde değiştirmeyi göz önünde bulundurun.

## <a name="when-to-suppress-warnings"></a>Uyarıların ne zaman bastırılamıyor

Yöntem .NET olay modeliyle çalışmazsa bu kuraldan bir uyarı gizleyin.

## <a name="configurability"></a>Yapılandırılabilirlik

Bu kuralı [FxCop çözümleyicilerinin](install-fxcop-analyzers.md) (eski analizler olmadan) çalıştırıyorsanız, kod tabanınızın hangi bölümlerinin bu kuralı çalıştırmak için erişilebilirliğini temel alarak yapılandırabilirsiniz. Örneğin, kuralın yalnızca genel olmayan API yüzeyine karşı çalışması gerektiğini belirtmek için, aşağıdaki anahtar-değer çiftini projenizdeki bir. editorconfig dosyasına ekleyin:

```ini
dotnet_code_quality.ca1030.api_surface = private, internal
```

Bu seçeneği yalnızca bu kural için, tüm kurallar için veya bu kategorideki tüm kurallar (tasarım) için yapılandırabilirsiniz. Daha fazla bilgi için bkz. [FxCop çözümleyicileri yapılandırma](configure-fxcop-analyzers.md).

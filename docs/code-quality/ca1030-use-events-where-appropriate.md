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
ms.openlocfilehash: f9a3d2ef30018c7fe57f1e7d728ba1dd152f56f5
ms.sourcegitcommit: 5483e399f14fb01f528b3b194474778fd6f59fa6
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/05/2019
ms.locfileid: "66714287"
---
# <a name="ca1030-use-events-where-appropriate"></a>CA1030: Uygun yerlerde olayları kullanın

|||
|-|-|
|TypeName|UseEventsWhereAppropriate|
|CheckId|CA1030|
|Kategori|Microsoft.Design|
|Yeni Değişiklik|Bölünemez|

## <a name="cause"></a>Sebep

Bir yöntem adı aşağıdakilerden biri ile başlar:

- Eklenti fiyatı
- RemoveOn
- Ateş
- artırma

Varsayılan olarak, bu kural yalnızca dışarıdan görünen bir yöntem ele alınmakta, ancak bu [yapılandırılabilir](#configurability).

## <a name="rule-description"></a>Kural açıklaması

Bu kural, normalde olaylar için kullanılan adlara sahip yöntemleri algılar. Olayları gözlemci ya da Yayımla-abone ol tasarım desenini izler; Bunlar, bir nesnede bir durum değişikliği diğer nesnelere iletileceği olduğunda kullanılır. Yanıt olarak açıkça tanımlanmış bir durum değişikliği bir yöntem çağrıldığında, bir olay işleyicisi tarafından yöntemin çağrılması gerekir. Yöntemi direkt olarak çağırmak yerine olayları yükselterek çağıran nesneler.

Olayların bazı genel örnekleri burada bir düğmeye tıklanması gibi bir kullanıcı eylemi yürütmek için kod kesiminin neden olan kullanıcı arabirimi uygulamalarında bulunur. .NET olay modeli için kullanıcı arabirimleri sınırlı değildir. Bir veya daha fazla nesneye durum değişikliklerini iletişim kurması gereken herhangi bir yere kullanılmalıdır.

## <a name="how-to-fix-violations"></a>İhlaller nasıl düzeltilir?

Bir nesnenin durumu değiştiğinde yöntemi çağrılırsa, .NET olay modelini kullanmak için tasarım değiştirmeyi göz önünde bulundurun.

## <a name="when-to-suppress-warnings"></a>Uyarılar bastırıldığında

Yöntemi .NET olay modeliyle çalışmazsa bu kuraldan bir uyarıyı gizler.

## <a name="configurability"></a>Etkiler ve yapılandırma

Bu kuraldan çalıştırıyorsanız [FxCop Çözümleyicileri](install-fxcop-analyzers.md) (ve statik kod analizi üzerinden değil), hangi parçalarının yapılandırabilirsiniz, bu kuralı çalıştırmak için kod tabanı, kendi erişilebilirliği temel. Örneğin, kural yalnızca genel olmayan API yüzeyi karşı çalışması gerektiğini belirtmek için projenizi bir .editorconfig dosyasında şu anahtar-değer çifti ekleyin:

```ini
dotnet_code_quality.ca1030.api_surface = private, internal
```

Bu kategoride (tasarımı), bu seçenek yalnızca bu kural, tüm kuralları veya tüm kuralları yapılandırabilirsiniz. Daha fazla bilgi için [yapılandırma FxCop Çözümleyicileri](configure-fxcop-analyzers.md).

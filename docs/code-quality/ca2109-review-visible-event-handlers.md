---
title: 'CA2109: Görünen olay işleyicilerini gözden geçirin'
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- CA2109
- ReviewVisibleEventHandlers
helpviewer_keywords:
- ReviewVisibleEventHandlers
- CA2109
ms.assetid: 8f8fa0ee-e94e-400e-b516-24d8727725d7
author: gewarren
ms.author: gewarren
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 88fbd5bbe873ae8bec9a506efbdb20d3fc77a2c1
ms.sourcegitcommit: 0c2523d975d48926dd2b35bcd2d32a8ae14c06d8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/24/2019
ms.locfileid: "71232795"
---
# <a name="ca2109-review-visible-event-handlers"></a>CA2109: Görünen olay işleyicilerini gözden geçirin

|||
|-|-|
|TypeName|ReviewVisibleEventHandlers|
|CheckId|CA2109|
|Kategori|Microsoft.Security|
|Son değişiklik|Yeni|

## <a name="cause"></a>Sebep
Ortak veya korunan olay işleme yöntemi algılandı.

## <a name="rule-description"></a>Kural açıklaması
Dışarıdan görünür bir olay işleme yöntemi, gözden geçirme gerektiren bir güvenlik sorunu gösterir.

Kesinlikle gerekli olmadığı takdirde olay işleme yöntemlerini açığa çıkarın. İşleyici ve olay imzaları eşleştiği sürece, sunulan yöntemi çağıran bir temsilci türü olan bir olay işleyicisi, herhangi bir olaya eklenebilir. Olaylar büyük olasılıkla herhangi bir kod tarafından oluşturulabilir ve bir düğmeye tıklanması gibi kullanıcı eylemlerine yanıt olarak yüksek düzeyde güvenilen sistem kodu tarafından sık ortaya çıkar. Bir olay işleme yöntemine güvenlik denetimi eklemek kodun yöntemi çağıran bir olay işleyicisini kaydetmesini engellemez.

Talep bir olay işleyicisi tarafından çağrılan bir yöntemi güvenilir bir şekilde koruyamaz. Güvenlik talepleri, Çağrı yığınındaki çağıranları inceleyerek güvenilmeyen çağıranlardan kod korumanıza yardımcı olur. Olay işleyicisinin bir olaya bir olay işleyicisi ekleyen kod, olay işleyicisinin yöntemleri çalıştırıldığında çağrı yığınında mevcut değildir. Bu nedenle, çağrı yığınında olay işleyicisi yöntemi çağrıldığında yalnızca son derece güvenilen çağıranlar olabilir. Bu, olay işleyicisi yöntemi tarafından yapılan taleplerin başarılı olmasına neden olur. Ayrıca, yöntem çağrıldığında, talep edilen izin belirtilebilir. Bu nedenlerden dolayı, bu kural ihlalini düzeltmeyen risk yalnızca olay işleme yöntemi gözden geçirildikten sonra değerlendirilebiliyor. Kodunuzu gözden geçirdikten sonra aşağıdaki sorunları göz önünde bulundurun:

- Olay işleyiciniz, izinleri tamamlamak veya yönetilmeyen kod iznini gizleme gibi tehlikeli veya açıktan yararlanmayan işlemleri gerçekleştirmesini ister misiniz?

- Yalnızca yığında son derece güvenilen çağıranlar ile herhangi bir zamanda çalıştırabildiğinden, kodunuza yönelik güvenlik tehditleri nelerdir?

## <a name="how-to-fix-violations"></a>İhlalleri çözme
Bu kural ihlalini onarmak için, yöntemini gözden geçirin ve aşağıdakileri değerlendirin:

- Olay işleme yöntemini genel olmayan hale getirebilirsiniz musunuz?

- Tüm tehlikeli işlevleri olay işleyicisinden dışarı taşıyabilir miyim?

- Bir güvenlik talebi belirtilmişse, bu başka bir şekilde gerçekleştirilebilir mi?

## <a name="when-to-suppress-warnings"></a>Uyarıların ne zaman bastırılamıyor
Kodunuzun bir güvenlik tehdidi oluşturmadığından emin olmak için dikkatli bir güvenlik incelemesinin ardından bu kuraldan bir uyarı gizleyin.

## <a name="example"></a>Örnek
Aşağıdaki kod kötü amaçlı kod tarafından kötüye kullanılabilecek bir olay işleme yöntemi gösterir.

[!code-csharp[FxCop.Security.EventSecLib#1](../code-quality/codesnippet/CSharp/ca2109-review-visible-event-handlers_1.cs)]

## <a name="see-also"></a>Ayrıca bkz.

- <xref:System.Security.CodeAccessPermission.Demand%2A?displayProperty=fullName>
- <xref:System.EventArgs?displayProperty=fullName>
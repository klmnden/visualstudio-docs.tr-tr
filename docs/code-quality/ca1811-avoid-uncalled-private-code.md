---
title: 'CA1811: Çağırılmayan özel kodlardan kaçının'
ms.date: 11/04/2016
ms.prod: visual-studio-dev15
ms.topic: reference
f1_keywords:
- AvoidUncalledPrivateCode
- CA1811
helpviewer_keywords:
- CA1811
- AvoidUncalledPrivateCode
ms.assetid: aadbba74-7821-475f-8980-34d17c0a0a8b
author: gewarren
ms.author: gewarren
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 6fca30671616dbe1e9d1c3468420d4526aa02250
ms.sourcegitcommit: 2193323efc608118e0ce6f6b2ff532f158245d56
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/25/2019
ms.locfileid: "54975159"
---
# <a name="ca1811-avoid-uncalled-private-code"></a>CA1811: Çağırılmayan özel kodlardan kaçının

|||
|-|-|
|TypeName|AvoidUncalledPrivateCode|
|CheckId|CA1811|
|Kategori|Microsoft.Performance|
|Yeni Değişiklik|Bölünemez|

## <a name="cause"></a>Sebep
 Özel veya iç (derleme düzeyi) üye Arayanların derlemede çağırıcısı değil, ortak dil çalışma zamanı tarafından çağrılan değildir ve temsilci tarafından çağrılan da değildir. Aşağıdaki üyeleri bu kural tarafından denetlenmez:

- Açık arabirim üyeleri.

- Statik oluşturucular.

- Serileştirme oluşturucularını uygulayın.

- İle işaretlenmiş yöntemler <xref:System.Runtime.InteropServices.ComRegisterFunctionAttribute?displayProperty=fullName> veya <xref:System.Runtime.InteropServices.ComUnregisterFunctionAttribute?displayProperty=fullName>.

- Geçersiz kılmalar olan üyeleri.

## <a name="rule-description"></a>Kural açıklaması
 Bu kural, giriş noktaları, gerçekleşirse, hatalı pozitif sonuçları kural mantığı tarafından şu anda belirtilmemiş bildirebilirsiniz. Ayrıca, derleyici bir derlemeye noncallable kod yayabilir.

## <a name="how-to-fix-violations"></a>İhlaller nasıl düzeltilir?
 Bu kural ihlalini düzeltmek için noncallable kodunu kaldırmak veya onu çağıran kodu ekleyin.

## <a name="when-to-suppress-warnings"></a>Uyarılar bastırıldığında
 Bu kuraldan bir uyarıyı bastırmak güvenlidir.

## <a name="related-rules"></a>İlgili kuralları
 [CA1812: Örneklenmemiş iç sınıflardan kaçının](../code-quality/ca1812-avoid-uninstantiated-internal-classes.md)

 [CA1801: Kullanılmayan parametreleri gözden geçir](../code-quality/ca1801-review-unused-parameters.md)

 [CA1804: Kullanılmayan yerel öğeleri kaldırın](../code-quality/ca1804-remove-unused-locals.md)
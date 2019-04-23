---
title: 'CA1811: Çağrılmayan özel kodlardan kaçının | Microsoft Docs'
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-code-analysis
ms.topic: reference
f1_keywords:
- AvoidUncalledPrivateCode
- CA1811
helpviewer_keywords:
- CA1811
- AvoidUncalledPrivateCode
ms.assetid: aadbba74-7821-475f-8980-34d17c0a0a8b
caps.latest.revision: 22
author: gewarren
ms.author: gewarren
manager: wpickett
ms.openlocfilehash: 373ccaa6552079a8995d61ef09bf6e0845c299d6
ms.sourcegitcommit: 1fc6ee928733e61a1f42782f832ead9f7946d00c
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/22/2019
ms.locfileid: "60113527"
---
# <a name="ca1811-avoid-uncalled-private-code"></a>CA1811: Çağırılmayan özel kodlardan kaçının
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

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

## <a name="rule-description"></a>Kural Tanımı
 Bu kural, giriş noktaları, gerçekleşirse, hatalı pozitif sonuçları kural mantığı tarafından şu anda belirtilmemiş bildirebilirsiniz. Ayrıca, derleyici bir derlemeye noncallable kod yayabilir.

## <a name="how-to-fix-violations"></a>İhlaller Nasıl Düzeltilir?
 Bu kural ihlalini düzeltmek için noncallable kodunu kaldırmak veya onu çağıran kodu ekleyin.

## <a name="when-to-suppress-warnings"></a>Uyarılar Bastırıldığında
 Bu kuraldan bir uyarıyı bastırmak güvenlidir.

## <a name="related-rules"></a>İlgili kuralları
 [CA1812: Örneklenmemiş iç sınıflardan kaçının](../code-quality/ca1812-avoid-uninstantiated-internal-classes.md)

 [CA1801: Kullanılmayan parametreleri gözden geçir](../code-quality/ca1801-review-unused-parameters.md)

 [CA1804: Kullanılmayan yerel öğeleri kaldırın](../code-quality/ca1804-remove-unused-locals.md)

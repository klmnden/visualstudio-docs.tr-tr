---
title: 'CA2106: Onay deyimlerinin güvenliğini sağlayın'
ms.date: 11/04/2016
ms.prod: visual-studio-dev15
ms.topic: reference
f1_keywords:
- CA2106
- SecureAsserts
helpviewer_keywords:
- CA2106
- SecureAsserts
ms.assetid: 91feb36e-6e2c-436c-8272-5aee31f77e98
author: gewarren
ms.author: gewarren
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: b0877ee06083a051ed38cdfdb8cf248407f663e1
ms.sourcegitcommit: 2193323efc608118e0ce6f6b2ff532f158245d56
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/25/2019
ms.locfileid: "54953853"
---
# <a name="ca2106-secure-asserts"></a>CA2106: Onay deyimlerinin güvenliğini sağlayın

|||
|-|-|
|TypeName|SecureAsserts|
|CheckId|CA2106|
|Kategori|Microsoft.Security|
|Yeni Değişiklik|Yeni|

## <a name="cause"></a>Sebep
 Bir yöntem bir izinleri bildiren ve çağıran üzerinde herhangi bir güvenlik denetimi gerçekleştirir.

## <a name="rule-description"></a>Kural açıklaması
 Güvenlik denetimleri yapmadan herhangi bir güvenlik izni ileri sürmek, kodunuzdaki güvenlik zayıflıklarını yararlanılabilir bırakır. Bir güvenlik izni onaylanan güvenlik yığın ilerlemesi sona erer. Çağıran tüm denetimleri yapmadan bir izin onaylama işlemi ise çağıranın dolaylı olarak kod izinlerinizi kullanarak yürütebilir. Assert zararlı bir biçimde kullanılamaz eminseniz izin verilen güvenlik denetimleri olmadan onaylar. Assert çağırmanızı kod zararsız ise ya da kullanıcıların çağırdığınız koda rastgele bilgi geçemezse zararsızdır.

## <a name="how-to-fix-violations"></a>İhlaller nasıl düzeltilir?
 Bu kural ihlalini düzeltmek için yöntemi veya metodu bildirim türünün için bir güvenlik talebi ekleyin.

## <a name="when-to-suppress-warnings"></a>Uyarılar bastırıldığında
 Bu kuraldan bir uyarıyı dikkatli bir güvenlik incelemesinden sonra yalnızca gösterme.

## <a name="see-also"></a>Ayrıca bkz.

- <xref:System.Security.CodeAccessPermission.Assert%2A?displayProperty=fullName>
- [Güvenli Kodlama Yönergeleri](/dotnet/standard/security/secure-coding-guidelines)
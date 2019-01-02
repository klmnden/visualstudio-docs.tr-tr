---
title: 'CA2106: BİLDİRİMLERİN Bildirimlerin güvenliğini sağlayın'
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
manager: douge
ms.workload:
- multiple
ms.openlocfilehash: 164d2bbe335f4b69892cf069bade5cf0df1e0787
ms.sourcegitcommit: 37fb7075b0a65d2add3b137a5230767aa3266c74
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/02/2019
ms.locfileid: "53864679"
---
# <a name="ca2106-secure-asserts"></a>CA2106: BİLDİRİMLERİN Bildirimlerin güvenliğini sağlayın

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
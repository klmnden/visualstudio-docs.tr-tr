---
title: 'CA2106: Onay deyimlerinin güvenliğini sağlayın'
ms.date: 11/04/2016
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
ms.openlocfilehash: df19d31abe88c6d12bafc933ba740badb832eb16
ms.sourcegitcommit: 5216c15e9f24d1d5db9ebe204ee0e7ad08705347
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/09/2019
ms.locfileid: "68921067"
---
# <a name="ca2106-secure-asserts"></a>CA2106: Onay deyimlerinin güvenliğini sağlayın

|||
|-|-|
|TypeName|SecureAsserts|
|CheckId|CA2106|
|Kategori|Microsoft.Security|
|Yeni Değişiklik|Yeni|

## <a name="cause"></a>Sebep
Bir yöntem, bir izni onaylar ve arayan üzerinde güvenlik denetimi gerçekleştirmesiz.

## <a name="rule-description"></a>Kural açıklaması
Güvenlik denetimleri yapmadan herhangi bir güvenlik izni ileri sürmek, kodunuzdaki güvenlik zayıflıklarını yararlanılabilir bırakır. Güvenlik yığını, bir güvenlik izni belirtildiğine göre ilerleme gösterir. Arayan üzerinde herhangi bir denetim gerçekleştirmeksizin bir izin belirtirseniz, çağıran, izinlerinizi kullanarak kodu dolaylı olarak yürütebilir. Onayın zararlı bir şekilde kullanılmadığından emin olduğunuzda güvenlik denetimleri olmadan onay için izin verilmez. Çağırdığınız kodun zararsız olması veya kullanıcıların çağırdığınız koda rastgele bilgiler geçiremezse bir onaylama işlemi zararsız olur.

## <a name="how-to-fix-violations"></a>İhlalleri çözme
Bu kural ihlalini onarmak için yönteme veya bildirim türüne bir güvenlik talebi ekleyin.

## <a name="when-to-suppress-warnings"></a>Uyarıların ne zaman bastırılamıyor
Bu kuraldan bir uyarıyı yalnızca dikkatli bir güvenlik incelemesi sonrasında gizleyin.

## <a name="see-also"></a>Ayrıca bkz.

- <xref:System.Security.CodeAccessPermission.Assert%2A?displayProperty=fullName>
- [Güvenli Kodlama Yönergeleri](/dotnet/standard/security/secure-coding-guidelines)
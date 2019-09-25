---
title: 'CA1726: Tercih edilen terimleri kullanın'
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- UsePreferredTerms
- CA1726
helpviewer_keywords:
- UsePreferredTerms
ms.assetid: 642b2acd-3a33-4d1f-b0a7-67073ae73be2
author: gewarren
ms.author: gewarren
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 3f359f7aa24ada0edf2c98a7d527ed715df85086
ms.sourcegitcommit: 0c2523d975d48926dd2b35bcd2d32a8ae14c06d8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/24/2019
ms.locfileid: "71233918"
---
# <a name="ca1726-use-preferred-terms"></a>CA1726: Tercih edilen terimleri kullanın

|||
|-|-|
|TypeName|UsePreferredTerms|
|CheckId|CA1726|
|Kategori|Microsoft. Naming|
|Son değişiklik|Parçalara ayırma-derlemeler üzerinde harekete geçirildiğinde<br /><br /> Tür parametrelerinde harekete geçirildiğinde, bozmasız|

## <a name="cause"></a>Sebep

Dışarıdan görünen bir tanımlayıcının adı, tercih edilen terim varolduğunda alternatif olarak bir terim içerir. Ya da ad, bayrak ya da bayrakları içerir.

## <a name="rule-description"></a>Kural açıklaması

Bu kural, bir tanımlayıcıyı belirteçlere ayrıştırır. Her bir tek belirteç ve her bitişik çift belirteci birleşimi, kurala ve özel sözlüklerin kullanım dışı bölümüne yerleştirilmiş koşullarla karşılaştırılır. Aşağıdaki tabloda, kuralda yerleşik olan koşullar ve tercih edilen alternatifler gösterilmektedir.

|Kullanılmayan dönem|Tercih edilen dönem|
|-------------------|--------------------|
|`Arent`|`AreNot`|
|`Cancelled`|`Canceled`|
|`Cant`|`Cannot`|
|`ComPlus`|`EnterpriseServices`|
|`Couldnt`|`CouldNot`|
|`Didnt`|`DidNot`|
|`Doesnt`|`DoesNot`|
|`Dont`|`DoNot`|
|`Flag` veya `Flags`|Bir değiştirme dönemi yoktur. Kullanmayın.|
|`Hadnt`|`HadNot`|
|`Hasnt`|`HasNot`|
|`Havent`|`HaveNot`|
|`Indices`|`Indexes`|
|`Isnt`|`IsNot`|
|`LogIn`|`LogOn`|
|`LogOut`|`LogOff`|
|`Shouldnt`|`ShouldNot`|
|`SignOn`|`SignIn`|
|`SignOff`|`SignOut`|
|`Wasnt`|`WasNot`|
|`Werent`|`WereNot`|
|`Wont`|`WillNot`|
|`Wouldnt`|`WouldNot`|
|`Writeable`|`Writable`|

## <a name="how-to-fix-violations"></a>İhlalleri çözme
Bu kuralın ihlalini onarmak için terimi tercih edilen alternatif terim ile değiştirin.

## <a name="when-to-suppress-warnings"></a>Uyarıların ne zaman bastırılamıyor
Yalnızca tanımlayıcının adı kasıtlı olarak belirtilmişse ve özellikle de tercih edilen dönem yerine özgün terimiyle ilişkili olduğunda bu kuraldan bir uyarı gizleyin.

## <a name="related-rules"></a>İlgili kurallar
[Adlandırma Uyarıları](../code-quality/naming-warnings.md)
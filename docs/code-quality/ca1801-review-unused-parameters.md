---
title: 'CA1801: Kullanılmayan parametreleri gözden geçirin'
ms.date: 06/24/2019
ms.topic: reference
f1_keywords:
- AvoidUnusedParameters
- CA1801
- ReviewUnusedParameters
helpviewer_keywords:
- CA1801
- ReviewUnusedParameters
ms.assetid: 5d73545c-e153-4b7c-a7b2-be6bf5aca5be
author: gewarren
ms.author: gewarren
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 6de48bf273a5c93afcd14e7bab2c5d4c4c4b5a7c
ms.sourcegitcommit: 0c2523d975d48926dd2b35bcd2d32a8ae14c06d8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/24/2019
ms.locfileid: "71233833"
---
# <a name="ca1801-review-unused-parameters"></a>CA1801: Kullanılmayan parametreleri gözden geçirin

|||
|-|-|
|TypeName|ReviewUnusedParameters|
|CheckId|CA1801|
|Kategori|Microsoft. Usage|
|Son değişiklik|Bozuk olmayan-üye, yaptığınız değişiklikten bağımsız olarak, derleme dışında görünür değilse.<br /><br /> Parçalama-üyeyi, gövdesi içinde parametresini kullanacak şekilde değiştirirseniz.<br /><br /> Parçalama-parametreyi kaldırırsanız ve derleme dışında görünür hale gelir.|

## <a name="cause"></a>Sebep

Yöntem imzası, metot gövdesinde kullanılmayan bir parametre içerir.

Bu kural aşağıdaki tür yöntemleri incelemez:

- Bir temsilci tarafından başvurulan Yöntemler.

- Olay işleyicileri olarak kullanılan yöntemler.

- `abstract` (`MustOverride` Visual Basic) değiştiricisiyle belirtilen Yöntemler.

- `virtual` (`Overridable` Visual Basic) değiştiricisiyle belirtilen Yöntemler.

- `override` (`Overrides` Visual Basic) değiştiricisiyle belirtilen Yöntemler.

- `extern` (`Declare` Visual Basic) değiştiricisiyle belirtilen Yöntemler.

[FxCop çözümleyicileri](install-fxcop-analyzers.md)kullanıyorsanız, bu kural [atma](/dotnet/csharp/discards) simgesiyle adlandırılan parametrelere bayrak eklemez, `_` `_1`Örneğin,, ve `_2`. Bu, imza gereksinimleri için gerekli olan parametrelerde (örneğin, temsilci olarak kullanılan bir yöntem, özel özniteliklere sahip bir parametre) veya bir Framework tarafından çalışma zamanında değeri örtük olarak erişilen ancak içinde başvurulmayan bir parametreyle uyarı gürültüsünü azaltır. kodudur.

## <a name="rule-description"></a>Kural açıklaması

Yöntem gövdesinde kullanılmayan sanal olmayan metotlarda bulunan parametreleri gözden geçirin ve bunlara erişmek için hata etrafında yanlışlık bulunmadığından emin olun. Kullanılmayan parametreler bakım ve performans maliyetleri doğurur.

Bazen, bu kuralın ihlali yöntemdeki bir uygulama hatasına işaret edebilir. Örneğin, parametresi metot gövdesinde kullanılmış olmalıdır. Geriye dönük uyumluluk nedeniyle parametrenin mevcut olması gerekiyorsa, bu kuralın uyarılarını gizleyin.

## <a name="how-to-fix-violations"></a>İhlalleri çözme

Bu kural ihlalini onarmak için kullanılmayan parametreyi (bir son değişiklik) kaldırın ya da yöntemi gövdesinde (kırılmamış değişiklik) parametreyi kullanın.

## <a name="when-to-suppress-warnings"></a>Uyarıların ne zaman bastırılamıyor

Bu kuraldan bir uyarıyı gizlemek güvenlidir:

- Daha önce sevk edilen kodda, düzeltilmesi gereken bir değişiklik olacaktır.

- `this` İçin<xref:Microsoft.VisualStudio.TestTools.UnitTesting.Assert?displayProperty=nameWithType>özel bir genişletme yönteminde parametresi için. <xref:Microsoft.VisualStudio.TestTools.UnitTesting.Assert> Sınıfındaki işlevler statiktir, bu nedenle Yöntem gövdesindeki `this` parametreye erişmeniz gerekmez.

## <a name="example"></a>Örnek

Aşağıdaki örnekte iki yöntem gösterilmektedir. Bir yöntem kuralı çiğneniyor ve diğer yöntem kuralı karşılar.

[!code-csharp[FxCop.Usage.ReviewUnusedParameters#1](../code-quality/codesnippet/CSharp/ca1801-review-unused-parameters_1.cs)]

## <a name="related-rules"></a>İlgili kurallar

[CA1811 Çağrılmadı özel koddan kaçının](../code-quality/ca1811-avoid-uncalled-private-code.md)

[CA1812 Örneklenmemiş iç sınıflardan kaçının](../code-quality/ca1812-avoid-uninstantiated-internal-classes.md)

[CA1804 Kullanılmayan yerelleri kaldır](../code-quality/ca1804-remove-unused-locals.md)

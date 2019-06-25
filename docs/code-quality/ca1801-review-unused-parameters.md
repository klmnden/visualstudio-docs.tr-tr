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
ms.openlocfilehash: f9a0714082e0fce744fe74eaa4e4aefee5a41867
ms.sourcegitcommit: 01c3c9dcade5d913bde2c7efa8c931a7b04e6cd0
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/25/2019
ms.locfileid: "67365375"
---
# <a name="ca1801-review-unused-parameters"></a>CA1801: Kullanılmayan parametreleri gözden geçirin

|||
|-|-|
|TypeName|ReviewUnusedParameters|
|CheckId|CA1801|
|Kategori|Microsoft.Usage|
|Yeni Değişiklik|Üyesi yaptığınız değişiklikler ne olursa olsun derlemenin dışında görünür değilse olmayan son -.<br /><br /> Üye kendi gövdesi içindeki bir parametre kullanmak için değiştirmeniz halinde olmayan en son -.<br /><br /> -Parametresini kaldırın ve derlemenin dışında görünür olup olmadığını kesiliyor.|

## <a name="cause"></a>Sebep

Yöntem imzası yöntemin gövdesinde kullanılmayan bir parametre içerir.

Bu kural, yöntemleri aşağıdaki türde incelemez:

- Temsilci tarafından başvurulan yöntemleri.

- Olay işleyicileri kullanılan yöntemleri.

- Yöntemleri ile bildirilmiş `abstract` (`MustOverride` Visual Basic) değiştirici.

- Yöntemleri ile bildirilmiş `virtual` (`Overridable` Visual Basic) değiştirici.

- Yöntemleri ile bildirilmiş `override` (`Overrides` Visual Basic) değiştirici.

- Yöntemleri ile bildirilmiş `extern` (`Declare` deyimi Visual Basic) değiştirici.

## <a name="rule-description"></a>Kural açıklaması

Parametreleri onlara erişmek için hata doğruluk hiçbir olduğundan emin olmak için yöntemin gövdesinde kullanılmayan sanal olmayan yöntemlerde gözden geçirin. Kullanılmayan parametreler Bakım ve performans ücret yansıtılmaz.

Bazen bu kuralın ihlalini yöntemi bir uygulama hatasını işaret edebilir. Örneğin, bir parametre yöntemin gövdesinde kullanılmış. Parametre geriye dönük uyumluluk nedeniyle zorundaysa bu kuralın uyarılarını gizle.

## <a name="how-to-fix-violations"></a>İhlaller nasıl düzeltilir?

Bu kural ihlalini düzeltmek için kullanılmayan (önemli bir değişiklik) parametreyi kaldırın veya yöntem gövdesi (bir hataya neden olmayan değişiklik) parametresini kullanın.

## <a name="when-to-suppress-warnings"></a>Uyarılar bastırıldığında

Bu kuraldan bir uyarıyı bastırmak güvenlidir:

- Daha önce sevk edilen kod düzeltme bir değişiklik olur.

- İçin `this` özel bir genişletme yöntemi için parametre <xref:Microsoft.VisualStudio.TestTools.UnitTesting.Assert?displayProperty=nameWithType>. İşlevler <xref:Microsoft.VisualStudio.TestTools.UnitTesting.Assert> erişimi gerekmez. Bu nedenle sınıfı statik olduğundan `this` yöntem gövdesini parametresi.

## <a name="example"></a>Örnek

Aşağıdaki örnek, iki yöntem gösterir. Bir yöntem kuralı ihlal etmektedir ve kural başka bir yöntem karşılar.

[!code-csharp[FxCop.Usage.ReviewUnusedParameters#1](../code-quality/codesnippet/CSharp/ca1801-review-unused-parameters_1.cs)]

## <a name="related-rules"></a>İlgili kuralları

[CA1811: Çağrılmayan özel kodlardan kaçının](../code-quality/ca1811-avoid-uncalled-private-code.md)

[CA1812: Örneklenmemiş iç sınıflardan kaçının](../code-quality/ca1812-avoid-uninstantiated-internal-classes.md)

[CA1804: Kullanılmayan yerel öğeleri kaldırın](../code-quality/ca1804-remove-unused-locals.md)
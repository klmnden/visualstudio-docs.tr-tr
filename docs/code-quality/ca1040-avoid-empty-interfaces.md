---
title: 'CA1040: Boş arabirimlerden kaçının'
ms.date: 03/11/2019
ms.topic: reference
f1_keywords:
- CA1040
- AvoidEmptyInterfaces
helpviewer_keywords:
- AvoidEmptyInterfaces
- CA1040
ms.assetid: 120a741b-5fd1-4836-8453-7857e0cd0380
author: gewarren
ms.author: gewarren
manager: jillfra
dev_langs:
- CPP
- CSharp
- VB
ms.workload:
- multiple
ms.openlocfilehash: 726953de0a92c0237ecaf7b724d9586a5d0f4c16
ms.sourcegitcommit: f7c401a376ce410336846835332a693e6159c551
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/14/2019
ms.locfileid: "57868736"
---
# <a name="ca1040-avoid-empty-interfaces"></a>CA1040: Boş arabirimlerden kaçının

|||
|-|-|
|TypeName|AvoidEmptyInterfaces|
|CheckId|CA1040|
|Kategori|Microsoft.Design|
|Yeni Değişiklik|Yeni|

## <a name="cause"></a>Sebep

Arabirim herhangi bir üye bildirmek veya iki veya daha fazla diğer arabirimleri de uygulamak desteklemez.

Varsayılan olarak, bu kural dışarıdan görünebilir arabirimler yalnızca görünür, ancak bu [yapılandırılabilir](#configurability).

## <a name="rule-description"></a>Kural açıklaması

Arayüzler bir davranış veya kullanım sözleşmesi sağlayan üyeleri tanımlar. Arabirim tarafından tanımlanan fonksiyonellik herhangi bir tür tarafından türün kalıtım hiyerarşisinde nerede belirdiği önemsenmeksizin devralınabilir. Tür arabirimin üyeleri için uygulamaları sağlayarak bir arayüz uygular. Boş bir arabirim herhangi bir üye tanımlamıyor. Bu nedenle, uygulanabilir bir sözleşme tanımlamaz.

Tasarımınızı boş içeriyorsa türleri arabirimleri uygulayan beklenir, büyük olasılıkla bir işaretçi veya bir grup türleri tanımlamak için bir yol olarak bir arabirim kullanıyorsunuz. Bu kimliği, çalışma zamanında meydana gelir, bunu gerçekleştirmek için doğru şekilde özel bir öznitelik kullanmaktır. Hedef türlerini tanımlamak için varlığı veya öznitelik olmaması veya öznitelik özelliklerini kullanın. Ardından derleme zamanında kimliği olmalıdır, boş bir arabirim kullanmak için kabul edilebilir.

## <a name="how-to-fix-violations"></a>İhlaller nasıl düzeltilir?

Arabirimi Kaldır veya üyeleri ekleyin. Boş arabirim türleri kümesi etiketlemek için kullanılıyorsa, arabirim özel bir öznitelik ile değiştirin.

## <a name="when-to-suppress-warnings"></a>Uyarılar bastırıldığında

Arabirimi, derleme zamanında türleri kümesini tanımlamak için kullanıldığında, bu kuraldan bir uyarıyı bastırmak güvenlidir.

## <a name="configurability"></a>Etkiler ve yapılandırma

Bu kuraldan çalıştırıyorsanız [FxCop Çözümleyicileri](install-fxcop-analyzers.md) (ve statik kod analizi üzerinden değil), hangi parçalarının yapılandırabilirsiniz, bu kuralı çalıştırmak için kod tabanı, kendi erişilebilirliği temel. Örneğin, kural yalnızca genel olmayan API yüzeyi karşı çalışması gerektiğini belirtmek için projenizi bir .editorconfig dosyasında şu anahtar-değer çifti ekleyin:

```
dotnet_code_quality.ca1040.api_surface = private, internal
```

Bu kategoride (tasarımı), bu seçenek yalnızca bu kural, tüm kuralları veya tüm kuralları yapılandırabilirsiniz. Daha fazla bilgi için [yapılandırma FxCop Çözümleyicileri](configure-fxcop-analyzers.md).

## <a name="example"></a>Örnek

Aşağıdaki örnek, boş bir arabirim gösterir.

[!code-csharp[FxCop.Design.InterfacesNotEmpty#1](../code-quality/codesnippet/CSharp/ca1040-avoid-empty-interfaces_1.cs)]
[!code-cpp[FxCop.Design.InterfacesNotEmpty#1](../code-quality/codesnippet/CPP/ca1040-avoid-empty-interfaces_1.cpp)]
[!code-vb[FxCop.Design.InterfacesNotEmpty#1](../code-quality/codesnippet/VisualBasic/ca1040-avoid-empty-interfaces_1.vb)]
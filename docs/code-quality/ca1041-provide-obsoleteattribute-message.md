---
title: 'CA1041: ObsoleteAttribute iletisi sağla'
ms.date: 03/11/2019
ms.topic: reference
f1_keywords:
- CA1041
- ProvideObsoleteAttributeMessage
helpviewer_keywords:
- ProvideObsoleteAttributeMessage
- CA1041
ms.assetid: be5bee69-d2d2-44e1-be2e-3ea451969003
author: gewarren
ms.author: gewarren
manager: jillfra
dev_langs:
- CPP
- CSharp
- VB
ms.workload:
- multiple
ms.openlocfilehash: 354d1d2fe99fa55bba7f8a00bf3e9f760ff1dbaf
ms.sourcegitcommit: 2ee11676af4f3fc5729934d52541e9871fb43ee9
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/17/2019
ms.locfileid: "65842183"
---
# <a name="ca1041-provide-obsoleteattribute-message"></a>CA1041: ObsoleteAttribute iletisi sağla

|||
|-|-|
|TypeName|ProvideObsoleteAttributeMessage|
|CheckId|CA1041|
|Kategori|Microsoft.Design|
|Yeni Değişiklik|Bölünemez|

## <a name="cause"></a>Sebep

Bir tür veya üye kullanılarak işaretlenmiş bir <xref:System.ObsoleteAttribute?displayProperty=fullName> sahip olmayan bir öznitelik kendi <xref:System.ObsoleteAttribute.Message%2A?displayProperty=fullName> özelliği belirtilmelidir.

Varsayılan olarak, bu kural yalnızca dışarıdan görülebilen türler ve üyeler görünüyor, ancak bu [yapılandırılabilir](#configurability).

## <a name="rule-description"></a>Kural açıklaması

<xref:System.ObsoleteAttribute> kullanım dışı kitaplığı türleri ve üyeleri işaretlemek için kullanılır. Kitaplık Tüketiciler, herhangi bir tür veya üye artık kullanılmıyor olarak işaretlendiğinden kullanımı kaçınmanız gerekir. Desteklenmiyor ve sonunda Kitaplığı'nın daha yeni sürümlerinden kaldırılacak olmasıdır. Bir tür veya üye işaretlendiğinde kullanarak <xref:System.ObsoleteAttribute> derlenir, <xref:System.ObsoleteAttribute.Message%2A> özniteliğinin özelliği görüntülenir. Bu eski türü veya üye kullanıcı bilgilerini sağlar. Bu bilgiler genellikle ne kadar eski türü içerir veya üye kullanılacak kitaplık tasarımcılar ve tercih edilen değişiklik tarafından desteklenecektir.

## <a name="how-to-fix-violations"></a>İhlaller nasıl düzeltilir?

Bu kural ihlalini düzeltmek için ekleme `message` parametresi <xref:System.ObsoleteAttribute> Oluşturucusu.

## <a name="when-to-suppress-warnings"></a>Uyarılar bastırıldığında

Çünkü bu kuraldan bir uyarıyı bastırmayın <xref:System.ObsoleteAttribute.Message%2A> özelliği geçersiz bir türe veya üyeye hakkında önemli bilgiler sağlar.

## <a name="configurability"></a>Etkiler ve yapılandırma

Bu kuraldan çalıştırıyorsanız [FxCop Çözümleyicileri](install-fxcop-analyzers.md) (ve statik kod analizi üzerinden değil), hangi parçalarının yapılandırabilirsiniz, bu kuralı çalıştırmak için kod tabanı, kendi erişilebilirliği temel. Örneğin, kural yalnızca genel olmayan API yüzeyi karşı çalışması gerektiğini belirtmek için projenizi bir .editorconfig dosyasında şu anahtar-değer çifti ekleyin:

```ini
dotnet_code_quality.ca1041.api_surface = private, internal
```

Bu kategoride (tasarımı), bu seçenek yalnızca bu kural, tüm kuralları veya tüm kuralları yapılandırabilirsiniz. Daha fazla bilgi için [yapılandırma FxCop Çözümleyicileri](configure-fxcop-analyzers.md).

## <a name="example"></a>Örnek

Aşağıdaki örnek, doğru bildirilmiş olan eski bir üye gösterir <xref:System.ObsoleteAttribute>.

[!code-cpp[FxCop.Design.ObsoleteAttributeOnMember#1](../code-quality/codesnippet/CPP/ca1041-provide-obsoleteattribute-message_1.cpp)]
[!code-csharp[FxCop.Design.ObsoleteAttributeOnMember#1](../code-quality/codesnippet/CSharp/ca1041-provide-obsoleteattribute-message_1.cs)]
[!code-vb[FxCop.Design.ObsoleteAttributeOnMember#1](../code-quality/codesnippet/VisualBasic/ca1041-provide-obsoleteattribute-message_1.vb)]

## <a name="see-also"></a>Ayrıca bkz.

- <xref:System.ObsoleteAttribute?displayProperty=fullName>
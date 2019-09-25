---
title: 'CA1303: Harfleri yerelleştirilmiş parametreler olarak göndermeyin'
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- Do not pass literals as localized parameters
- DoNotPassLiteralsAsLocalizedParameters
- CA1303
helpviewer_keywords:
- DoNotPassLiteralsAsLocalizedParameters
- CA1303
ms.assetid: 904d284e-76d0-4b8f-a4df-0094de8d7aac
author: gewarren
ms.author: gewarren
manager: jillfra
dev_langs:
- CPP
- CSharp
- VB
ms.workload:
- multiple
ms.openlocfilehash: 2700dc2ade7ba901f15f67045e3170e2bbb40ff8
ms.sourcegitcommit: 0c2523d975d48926dd2b35bcd2d32a8ae14c06d8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/24/2019
ms.locfileid: "71235110"
---
# <a name="ca1303-do-not-pass-literals-as-localized-parameters"></a>CA1303: Harfleri yerelleştirilmiş parametreler olarak göndermeyin

|||
|-|-|
|TypeName|DoNotPassLiteralsAsLocalizedParameters|
|CheckId|CA1303|
|Kategori|Microsoft. Globalization|
|Son değişiklik|Kırılmamış|

## <a name="cause"></a>Sebep

Bir yöntem, bir dize sabit değerini bir .NET oluşturucusuna veya yöntemine parametre olarak geçirir ve bu dize yerelleştirilebilir olmalıdır.

Bu uyarı, bir sabit dize bir parametre veya özelliğe değer olarak geçirildiğinde ve aşağıdaki durumlardan biri veya daha fazlası doğru olduğunda tetiklenir:

- Parametrenin veya özelliğin özniteliği true olarak ayarlandı. <xref:System.ComponentModel.LocalizableAttribute>

- Parametre veya özellik adı "metin", "Ileti" veya "başlık" içerir.

- Console. Write veya Console. WriteLine yöntemine geçirilen dize parametresinin adı "Value" ya da "Format" değeridir.

## <a name="rule-description"></a>Kural açıklaması

Kaynak koda gömülü olan dize sabit değerleri yerelleşebilir.

## <a name="how-to-fix-violations"></a>İhlalleri çözme

Bu kuralın ihlalini onarmak için, dize sabit değerini <xref:System.Resources.ResourceManager> , sınıfının bir örneği aracılığıyla alınan bir dizeyle değiştirin.

## <a name="when-to-suppress-warnings"></a>Uyarıların ne zaman bastırılamıyor

Kod kitaplığı yerelleştirilemez veya dize son kullanıcıya ya da kod kitaplığı kullanan bir geliştiriciye açık değilse, bu kuraldan bir uyarı bastırmak güvenlidir.

Kullanıcılar, yerelleştirilmiş dizeleri bir parametre ya da özelliği yeniden adlandırarak ya da bu öğelerin koşullu olarak işaretleyerek bu yöntemlere karşı bir gürültü ortadan kaldırabilir.

## <a name="example"></a>Örnek

Aşağıdaki örnek, iki bağımsız değişkeni aralık dışında bir özel durum oluşturan bir yöntemi gösterir. İlk bağımsız değişken için, özel durum Oluşturucusu bu kuralı ihlal eden bir sabit dize aktardı. İkinci bağımsız değişken için, Oluşturucu bir <xref:System.Resources.ResourceManager>ile alınan bir dizeyi doğru şekilde geçirdi.

[!code-cpp[FxCop.Globalization.DoNotPassLiterals#1](../code-quality/codesnippet/CPP/ca1303-do-not-pass-literals-as-localized-parameters_1.cpp)]
[!code-vb[FxCop.Globalization.DoNotPassLiterals#1](../code-quality/codesnippet/VisualBasic/ca1303-do-not-pass-literals-as-localized-parameters_1.vb)]
[!code-csharp[FxCop.Globalization.DoNotPassLiterals#1](../code-quality/codesnippet/CSharp/ca1303-do-not-pass-literals-as-localized-parameters_1.cs)]

## <a name="see-also"></a>Ayrıca bkz.

- [Masaüstü uygulamalarındaki kaynaklar](/dotnet/framework/resources/index)
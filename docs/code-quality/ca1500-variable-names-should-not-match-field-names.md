---
title: 'CA1500: Değişken adları alan adları ile eşleşmemelidir'
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- VariableNamesShouldNotMatchFieldNames
- CA1500
helpviewer_keywords:
- VariableNamesShouldNotMatchFieldNames
- CA1500
ms.assetid: fa0e5029-79e9-4a33-8576-787ac3c26c39
author: gewarren
ms.author: gewarren
manager: jillfra
dev_langs:
- CSharp
- VB
ms.workload:
- multiple
ms.openlocfilehash: 740edb9861d2e3e758a36dfc067cb85fe4fc2c7e
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62807166"
---
# <a name="ca1500-variable-names-should-not-match-field-names"></a>CA1500: Değişken adları alan adları ile eşleşmemelidir

|||
|-|-|
|TypeName|VariableNamesShouldNotMatchFieldNames|
|CheckId|CA1500|
|Kategori|Microsoft.Maintainability|
|Yeni Değişiklik|Bir alan olarak aynı ada sahip bir parametreyi tetiklendiğinde:<br /><br /> -Hataya neden olmayan - varsa alan ve parametre bildirir yöntemi derlemenin dışından görülemeyen bağımsız olarak, değişiklik.<br />-Bozucu - alanın adını değiştirip derlemesi dışında görülebilir.<br />-- Parametrenin adını değiştirirseniz ve onu bildiren yöntemin, derlemenin dışından görülebilir kesiliyor.<br /><br /> Bir alan olarak aynı ada sahip yerel bir değişken üzerinde tetiklendiğinde:<br /><br /> Alanın yaptığınız değişiklikler ne olursa olsun derlemenin dışından görülemeyen, hataya neden olmayan -.<br />Yerel değişken adını değiştirin ve alan adını değiştirmeyin hataya neden olmayan -.<br />-- Alanın adını değiştirip derlemesi dışında görülebilir kesiliyor.|

## <a name="cause"></a>Sebep

Bir örnek yöntemi, bir parametre veya bildirim türü bir örnek alan adı ile eşleşen yerel bir değişken bildirir. Kural ihlal yerel değişkenler yakalamak için test edilen derleme hata ayıklama bilgileri kullanarak oluşturulması gereken ve ilişkili bir program veritabanı (.pdb) dosyası kullanılabilir olmalıdır.

## <a name="rule-description"></a>Kural açıklaması

Örnek alan adı, parametre veya yerel bir değişken adı eşleştiğinde, örnek alanı kullanılarak erişilen `this` (`Me` içinde [!INCLUDE[vbprvb](../code-quality/includes/vbprvb_md.md)]), yöntem gövdesi içindeki anahtar sözcüğü. Kod muhafaza ederken, bu fark aklınızdan çıkarın ve parametre/yerel değişkeni hataları müşteri adayları örneği alanına başvuruyor varsayar daha kolaydır. Bu, özellikle uzun metot gövdeleri için geçerlidir.

## <a name="how-to-fix-violations"></a>İhlaller nasıl düzeltilir?

Bu kural ihlalini düzeltmek için parametre/değişkeni veya alanı yeniden adlandırın.

## <a name="when-to-suppress-warnings"></a>Uyarılar bastırıldığında

Bu kuraldan uyarıyı bastırmayın.

## <a name="example"></a>Örnek

Aşağıdaki örnek, iki kural ihlalleri gösterir.

[!code-vb[FxCop.Maintainability.VarMatchesField#1](../code-quality/codesnippet/VisualBasic/ca1500-variable-names-should-not-match-field-names_1.vb)]
[!code-csharp[FxCop.Maintainability.VarMatchesField#1](../code-quality/codesnippet/CSharp/ca1500-variable-names-should-not-match-field-names_1.cs)]
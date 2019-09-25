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
ms.openlocfilehash: fbc3fbeac6d01b718af2022a09bddb92e9c7c2c6
ms.sourcegitcommit: 0c2523d975d48926dd2b35bcd2d32a8ae14c06d8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/24/2019
ms.locfileid: "71234565"
---
# <a name="ca1500-variable-names-should-not-match-field-names"></a>CA1500: Değişken adları alan adları ile eşleşmemelidir

|||
|-|-|
|TypeName|VariableNamesShouldNotMatchFieldNames|
|CheckId|CA1500|
|Kategori|Microsoft. Bakımolmaması|
|Son değişiklik|Bir alanla aynı ada sahip bir parametre üzerinde harekete geçirildiğinde:<br /><br /> -Parçalama-Eğer parametreyi bildiren alan ve yöntem, yaptığınız değişiklikten bağımsız olarak, derleme dışında görülemez.<br />-Parçalama-alanın adını değiştirirseniz ve derleme dışında görünebilirler.<br />-Parçalama-parametrenin adını ve bunu bildiren yöntemi derleme dışında görülebilir.<br /><br /> Bir alanla aynı ada sahip yerel bir değişkende harekete geçirildiğinde:<br /><br /> -Bölünmez-siz yaptığınız değişiklikten bağımsız olarak, alan derleme dışında görülemez.<br />-Kırılmamış-yerel değişkenin adını değiştirirseniz ve alanın adını değiştirmeyin.<br />-Parçalama-alanın adını değiştirirseniz ve derleme dışında görünebilirler.|

## <a name="cause"></a>Sebep

Örnek yöntemi bir parametre ya da adı bildirim türünün bir örnek alanıyla eşleşen yerel bir değişken bildirir. Kuralı ihlal eden yerel değişkenleri yakalamak için, sınanan derlemenin hata ayıklama bilgileri kullanılarak oluşturulması gerekir ve ilişkili program veritabanı (. pdb) dosyası kullanılabilir olmalıdır.

## <a name="rule-description"></a>Kural açıklaması

Bir örnek alanının adı bir parametre veya yerel değişken adıyla eşleştiğinde, örnek alana Yöntem gövdesinin içindeyken `this` (`Me` ın [!INCLUDE[vbprvb](../code-quality/includes/vbprvb_md.md)]) anahtar sözcüğü kullanılarak erişilir. Kodu koruma sırasında, bu farkı unutmak kolaydır ve parametre/yerel değişkenin, hatalara yol eden örnek alana başvurduğunu varsayın. Bu, özellikle uzun yöntem gövdeleri için geçerlidir.

## <a name="how-to-fix-violations"></a>İhlalleri çözme

Bu kuralın ihlalini onarmak için parametreyi/değişkeni ya da alanını yeniden adlandırın.

## <a name="when-to-suppress-warnings"></a>Uyarıların ne zaman bastırılamıyor

Bu kuraldan uyarıyı bastırmayın.

## <a name="example"></a>Örnek

Aşağıdaki örnek, kuralın iki ihlalini gösterir.

[!code-vb[FxCop.Maintainability.VarMatchesField#1](../code-quality/codesnippet/VisualBasic/ca1500-variable-names-should-not-match-field-names_1.vb)]
[!code-csharp[FxCop.Maintainability.VarMatchesField#1](../code-quality/codesnippet/CSharp/ca1500-variable-names-should-not-match-field-names_1.cs)]
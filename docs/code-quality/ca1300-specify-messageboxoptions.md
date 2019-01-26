---
title: 'CA1300: MessageBoxOptions belirt'
ms.date: 11/04/2016
ms.prod: visual-studio-dev15
ms.topic: reference
f1_keywords:
- SpecifyMessageBoxOptions
- CA1300
helpviewer_keywords:
- SpecifyMessageBoxOptions
- CA1300
ms.assetid: 9357a724-026e-4a3d-a03a-f14635064ec6
author: gewarren
ms.author: gewarren
manager: jillfra
dev_langs:
- CSharp
- VB
ms.workload:
- multiple
ms.openlocfilehash: 0000b66302e0dbb549b2832210573d1b3b174b84
ms.sourcegitcommit: 2193323efc608118e0ce6f6b2ff532f158245d56
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/25/2019
ms.locfileid: "54943279"
---
# <a name="ca1300-specify-messageboxoptions"></a>CA1300: MessageBoxOptions belirt

|||
|-|-|
|TypeName|SpecifyMessageBoxOptions|
|CheckId|CA1300|
|Kategori|Microsoft.Globalization|
|Yeni Değişiklik|Bölünemez|

## <a name="cause"></a>Sebep

Bir yöntemi çağıran bir aşırı yüklemesini <xref:System.Windows.Forms.MessageBox.Show%2A?displayProperty=fullName> görüntüsünü yöntemi bir <xref:System.Windows.Forms.MessageBoxOptions?displayProperty=fullName> bağımsız değişken.

## <a name="rule-description"></a>Kural açıklaması

Doğru olarak sağdan sola okuma düzeni kullanan kültürler için bir ileti kutusu görüntülemek için geçirmek [MessageBoxOptions.RightAlign](<xref:System.Windows.Forms.MessageBoxOptions.RightAlign>) ve [MessageBoxOptions.RtlReading](<xref:System.Windows.Forms.MessageBoxOptions.RtlReading>) alanlarını <xref:System.Windows.Forms.MessageBox.Show%2A> yöntem. İnceleme <xref:System.Windows.Forms.Control.RightToLeft%2A?displayProperty=fullName> sağdan sola okuma düzeni kullanan belirlemek için içeren denetiminin özelliği.

## <a name="how-to-fix-violations"></a>İhlaller nasıl düzeltilir?

Bu kural ihlalini düzeltmek için bir aşırı yüklemesini çağırmak <xref:System.Windows.Forms.MessageBox.Show%2A> gereken yöntemini bir <xref:System.Windows.Forms.MessageBoxOptions> bağımsız değişken.

## <a name="when-to-suppress-warnings"></a>Uyarılar bastırıldığında

Kod kitaplığı sağdan sola okuma düzeni kullanan bir kültür için yerelleştirilmiş değil olduğunda bu kuraldan bir uyarıyı bastırmak güvenlidir.

## <a name="example"></a>Örnek

Aşağıdaki örnek, kültürün okuma düzeni için uygun olan seçenekleri içeren bir ileti kutusu görüntüleyen bir yöntem gösterilmektedir. Görünmeyen bir kaynak dosyası örneği oluşturmak için gereklidir. Örnek bir kaynak dosyası olmadan örneği oluşturmak ve sağdan sola özelliği test etmek için yorumlarda izleyin.

[!code-vb[FxCop.Globalization.SpecifyMBOptions#1](../code-quality/codesnippet/VisualBasic/ca1300-specify-messageboxoptions_1.vb)]
[!code-csharp[FxCop.Globalization.SpecifyMBOptions#1](../code-quality/codesnippet/CSharp/ca1300-specify-messageboxoptions_1.cs)]

## <a name="see-also"></a>Ayrıca bkz.

- <xref:System.Resources.ResourceManager?displayProperty=fullName>
- [(.NET Framework) Masaüstü uygulamalarındaki kaynaklar](/dotnet/framework/resources/index)
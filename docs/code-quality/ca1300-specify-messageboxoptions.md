---
title: 'CA1300: MessageBoxOptions belirt'
ms.date: 11/04/2016
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
ms.openlocfilehash: 746475e60bbe72c4ebfc51f13d0b2d4d0552ff62
ms.sourcegitcommit: 0c2523d975d48926dd2b35bcd2d32a8ae14c06d8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/24/2019
ms.locfileid: "71235191"
---
# <a name="ca1300-specify-messageboxoptions"></a>CA1300: MessageBoxOptions belirt

|||
|-|-|
|TypeName|SpecifyMessageBoxOptions|
|CheckId|CA1300|
|Kategori|Microsoft. Globalization|
|Son değişiklik|Kırılmamış|

## <a name="cause"></a>Sebep

Yöntemi, <xref:System.Windows.Forms.MessageBox.Show%2A?displayProperty=fullName> <xref:System.Windows.Forms.MessageBoxOptions?displayProperty=fullName> bağımsız değişken olmayan yöntemin aşırı yüklemesini çağırır.

## <a name="rule-description"></a>Kural açıklaması

Sağdan sola okuma düzeni kullanan kültürler için bir ileti kutusunu doğru bir şekilde göstermek için, [MessageBoxOptions. soltalign](<xref:System.Windows.Forms.MessageBoxOptions.RightAlign>) ve [MessageBoxOptions. rtlokuyor](<xref:System.Windows.Forms.MessageBoxOptions.RtlReading>) <xref:System.Windows.Forms.MessageBox.Show%2A> alanlarını metoduna geçirin. Sağdan sola okuma düzeni kullanılıp kullanılmayacağını öğrenmek için içeren denetimin özelliğiniinceleyin.<xref:System.Windows.Forms.Control.RightToLeft%2A?displayProperty=fullName>

## <a name="how-to-fix-violations"></a>İhlalleri çözme

Bu kuralın ihlalini onarmak için, bir <xref:System.Windows.Forms.MessageBox.Show%2A> <xref:System.Windows.Forms.MessageBoxOptions> bağımsız değişken alan metodun aşırı yüklemesini çağırın.

## <a name="when-to-suppress-warnings"></a>Uyarıların ne zaman bastırılamıyor

Kod kitaplığı, sağdan sola okuma düzeni kullanan bir kültür için yerelleştirilmez, bu kuraldan bir uyarı bastırmak güvenlidir.

## <a name="example"></a>Örnek

Aşağıdaki örnek, kültürün okuma düzeni için uygun olan seçeneklere sahip bir ileti kutusu görüntüleyen bir yöntemi gösterir. Örnek oluşturmak için, gösterilmemiş bir kaynak dosyası gereklidir. Örneği bir kaynak dosyası olmadan derlemek ve sağdan sola özelliği test etmek için örnekteki açıklamaları izleyin.

[!code-vb[FxCop.Globalization.SpecifyMBOptions#1](../code-quality/codesnippet/VisualBasic/ca1300-specify-messageboxoptions_1.vb)]
[!code-csharp[FxCop.Globalization.SpecifyMBOptions#1](../code-quality/codesnippet/CSharp/ca1300-specify-messageboxoptions_1.cs)]

## <a name="see-also"></a>Ayrıca bkz.

- <xref:System.Resources.ResourceManager?displayProperty=fullName>
- [Masaüstü uygulamalarındaki kaynaklar (.NET Framework)](/dotnet/framework/resources/index)
---
title: Genel Windows Formları ve Web Formları İçin Kültüre Özgü Sınıflar
ms.date: 11/04/2016
ms.prod: visual-studio-dev15
ms.topic: conceptual
helpviewer_keywords:
- globalization [Windows Forms], classes
- Web applications [.NET Framework], globalization
- culture, culture-specific classes
- numbers, international
- localization [Windows Forms], classes
- globalization [Visual Studio], culture-specific classes
- Windows Forms, localization
- international applications [Visual Studio], data formats
- time [Visual Studio], international
- dates [Visual Studio], international
- culture
- international characters
- currency formats
- ASP.NET, globalization
- classes [Visual Studio], culture-specific
- localization [Visual Studio], culture-specific classes
ms.assetid: 0d06a0a4-f887-4f7c-bde7-1d543c06f803
author: gewarren
ms.author: gewarren
manager: jillfra
dev_langs:
- CSharp
- VB
ms.workload:
- multiple
ms.openlocfilehash: c311e9c79e4f2861b8b52852ff7bb9b0217bf22c
ms.sourcegitcommit: 2193323efc608118e0ce6f6b2ff532f158245d56
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/25/2019
ms.locfileid: "54948043"
---
# <a name="culture-specific-classes-for-global-windows-forms-and-web-forms"></a>Genel Windows Formları ve web formları için kültüre özgü sınıflar

Her bir kültürün tarih, zaman, sayı, para birimi ve diğer bilgileri görüntülemek için farklı kurallara sahiptir. <xref:System.Globalization> Ad alanı, kültüre özgü değerlerini değiştirmek için kullanılan sınıfları içerir, aşağıdaki gibi görüntülenir:
- <xref:System.Globalization.DateTimeFormatInfo>
- **Takvim**
- <xref:System.Globalization.NumberFormatInfo>

## <a name="using-the-culture-setting"></a>Kültür ayarı kullanma

Uygulama veya depolanan kültür ayarı kullanmak **Bölgesel Seçenekler** kültür kuralları, çalışma zamanı ve bilgi biçimlendirebilmek belirlemek için Denetim Masası'nı tıklatın,. Kültürü ayarlama hakkında daha fazla bilgi için bkz. [nasıl yapılır: Kültür ve ASP.NET web sayfası Genelleştirme için UI kültürü](https://msdn.microsoft.com/Library/76091f86-f967-4687-a40f-de87bd8cc9a0). Bilgi kültür ayarı göre otomatik olarak Biçimlendir sınıfları çağrılır *kültüre özgü*. Kültüre özgü bazı yöntemler
- <xref:System.IFormattable.ToString%2A?displayProperty=fullName>
- <xref:System.Console.WriteLine%2A?displayProperty=fullName>
- <xref:System.String.Format%2A?displayProperty=fullName>

Bazı kültüre özgü işlevleri (Visual Basic dilindeki) `MonthName` ve `WeekDayName`.

Örneğin, aşağıdaki kod nasıl kullanabileceğinizi gösterir. <xref:System.IFormattable.ToString%2A> biçimi para birimi bir yönteme geçerli kültür için:

```vb
' Put the Imports statements at the beginning of the code module
Imports System.Threading
Imports System.Globalization
' Display a number with the culture-specific currency formatting
Dim MyInt As Integer = 100
Console.WriteLine(MyInt.ToString("C", Thread.CurrentThread.CurrentCulture))
```

```csharp
// Put the using statements at the beginning of the code module
using System.Threading;
using System.Globalization;
// Display a number with the culture-specific currency formatting
int myInt = 100;
Console.WriteLine(myInt.ToString("C", Thread.CurrentThread.CurrentCulture));
```

Kültür, "fr-FR" olarak ayarlanırsa, aşağıdaki çıktı penceresinde görürsünüz:

`100,00`

Kültürü "en-US" olarak ayarlanırsa, aşağıdaki çıktı penceresinde görürsünüz:

`$100.00`

## <a name="see-also"></a>Ayrıca bkz.

- <xref:System.IFormattable.ToString%2A?displayProperty=fullName>
- <xref:System.Globalization.DateTimeFormatInfo>
- <xref:System.Globalization.NumberFormatInfo>
- <xref:System.Globalization.Calendar>
- <xref:System.Console.WriteLine%2A?displayProperty=fullName>
- <xref:System.String.Format%2A?displayProperty=fullName>
- [Uygulamaları Genelleştirme ve yerelleştirme](../ide/globalizing-and-localizing-applications.md)
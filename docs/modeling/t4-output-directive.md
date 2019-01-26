---
title: T4 Çıkış Yönergesi
ms.date: 11/04/2016
ms.topic: reference
author: gewarren
ms.author: gewarren
manager: jillfra
ms.workload:
- multiple
ms.prod: visual-studio-dev15
ms.openlocfilehash: 25e59e4e0273e22a1b11ea9c3e0d593f70568758
ms.sourcegitcommit: 2193323efc608118e0ce6f6b2ff532f158245d56
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/25/2019
ms.locfileid: "54929659"
---
# <a name="t4-output-directive"></a>T4 Çıkış Yönergesi

Visual Studio metin şablonlarında `output` yönergesi, dosya adı uzantısı ve dönüştürülen dosyanın kodlamasını tanımlamak için kullanılır.

 Örneğin, Visual Studio projenize adlı şablon dosyası içeriyorsa **MyTemplate.tt** aşağıdaki yönerge içerir:

 `<#@output extension=".cs"#>`

 Visual Studio adlı bir dosya oluşturur sonra **MyTemplate.cs**

 `output` Çalışma zamanı (önceden işlenmiş) metin şablonunda yönergesi gerekli değildir. Bunun yerine, çağırarak uygulamanızı oluşturulan dizesi edinir `TextTransform()`. Daha fazla bilgi için [T4 metin şablonları ile çalışma süresi metni oluşturma](../modeling/run-time-text-generation-with-t4-text-templates.md).

## <a name="using-the-output-directive"></a>Çıkış yönergesini kullanma

```
<#@ output extension=".fileNameExtension" [encoding="encoding"] #>
```

 Olmalıdır en fazla bir `output` her metin şablonunda yönergesi.

## <a name="extension-attribute"></a>Uzantı özniteliğine
 Oluşturulan metin çıktı dosyasının dosya adı uzantısını belirtir.

 Varsayılan değer **.cs**

 Örnekler: `<#@ output extension=".txt" #>`

 `<#@ output extension=".htm" #>`

 `<#@ output extension=".cs" #>`

 `<#@ output extension=".vb" #>`

 Kabul edilebilir değerler: Tüm geçerli dosya adı uzantısı.

## <a name="encoding-attribute"></a>kodlama özniteliği
 Çıkış dosyası oluşturulurken kullanılacak kodlamayı belirtir. Örneğin:

 `<#@ output encoding="utf-8"#>`

 Metin şablonu dosyası tarafından kullanılan kodlama varsayılan değerdir.

 Kabul edilebilir değerler: `us-ascii`

 `utf-16BE`

 `utf-16`

 `utf-8`

 `utf-7`

 `utf-32`

 `0` (Sistem varsayılanı)

 Genel olarak, Web adı dizesi veya herhangi biri tarafından döndürülen kodlamalarının kod sayfası numarası kullanabilirsiniz <xref:System.Text.Encoding.GetEncodings%2A?displayProperty=fullName>.
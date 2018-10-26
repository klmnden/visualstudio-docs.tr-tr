---
title: Mantıksal işleçler ve arama ifadelerindeki Gelişmiş operatörler
ms.date: 11/02/2017
ms.prod: visual-studio-dev15
ms.technology: vs-help-viewer
ms.topic: reference
helpviewer_keywords:
- Help Viewer, logical operators in search
- logical operators in search [Help Viewer]
ms.assetid: 0c38ae7d-3e20-4d47-a020-9677cd285916
author: gewarren
ms.author: gewarren
manager: douge
ms.workload:
- multiple
ms.openlocfilehash: a2c189afe9051d0f85c7f5f24a928d475d0eaca9
ms.sourcegitcommit: 240c8b34e80952d00e90c52dcb1a077b9aff47f6
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/23/2018
ms.locfileid: "49872856"
---
# <a name="logical-and-advanced-operators-in-search-expressions"></a>Arama ifadelerindeki mantıksal ve Gelişmiş işleçler

Yardım içerik, aramanızı daraltmak için mantıksal işleçler ve Gelişmiş arama işleçleri kullanabilirsiniz **Yardım Görüntüleyici**.

## <a name="logical-operators"></a>Mantıksal işleçler

Mantıksal işleçler, arama sorgusu birden çok arama terimlerini birleştirilmelidir belirtin. Aşağıdaki tabloda, mantıksal AND, OR işleçlerini gösterir değil ve NEREDEYSE.

|Aramak için|Bir yönetim grubuna bağlanmak veya bağlı bir yönetim grubunun özelliklerini düzenlemek için Yönetim çalışma alanında|Örnek|Sonuç|
|-------------------|---------|-------------|------------|
|Aynı makalede bulunan her iki terim|AND|DIB ve paleti|Hem "DIB" ve "palet" içeren konulardır.|
|Bir makalede her iki terim|VEYA|Izgara veya vektör|"Tarama" veya "vektör" içeren konulardır.|
|Aynı makalede bulunan ikinci terimi olmadan ilk terimi|DEĞİL|"işletim sistemi" DOS değil|"İşletim sistemi" ancak değil "DOS" içeren konulardır.|
|Birbirine yakın bir makaledeki her iki terim|YAKIN|Kullanıcı yakın çekirdek|Yakınlık "çekirdek" içinde "kullanıcı" içeren konuların kapatın.|

> [!IMPORTANT]
> Mantıksal işleçler tanıması arama motoru için tüm büyük harfler girmeniz gerekir.

## <a name="advanced-operators"></a>Gelişmiş operatörler

Gelişmiş arama işleçleri, ilişkin arama terimi aramak için bir makaledeki nerede belirterek içerik için aramanızı daraltın. Aşağıdaki tabloda dört kullanılabilir gelişmiş arama işleçleri açıklanmaktadır.

|Aramak için|Bir yönetim grubuna bağlanmak veya bağlı bir yönetim grubunun özelliklerini düzenlemek için Yönetim çalışma alanında|Örnek|Sonuç|
|-------------------|---------|-------------|------------|
|Bir terimi makalesinin başlığı|`title:`|`title:binaryreader`|Kendi başlıklarında "binaryreader" içeren konulardır.|
|Bir kod örneği bir terimi|`code:`|`code:readdouble`|Bir kod örneğinde "readdouble" içeren konulardır.|
|Bir terimi belirli bir programlama dili örneği|`code:vb:`|`code:vb:string`|Visual Basic kod örneğinde "dize" içeren konulardır.|
|Belirli bir dizin anahtar sözcüğüyle ilişkili olan bir makale|`keyword:`|`keyword:readbyte`|"Readbyte" dizin anahtar sözcüğü ile ilgili konular.|

> [!IMPORTANT]
> Son iki nokta üst üste ve arama motoru için iki noktadan önce boşluk olmaması Gelişmiş arama işleçleri tanıması için girmeniz gerekir.

### <a name="programming-languages-for-code-examples"></a>Kod örnekleri için programlama dilleri

Kullanabileceğiniz `code:` çeşitli programlama dillerini ilgili içeriği bulmak için işleci. Belirli bir programlama dili için örnekler döndürmek için programlama dili aşağıdaki değerlerden birini kullanın:

|Programlama dili|Arama işleci söz dizimi|
| - |---------|
|Visual Basic|`code:vb`<br/>`code:visualbasic`|
|C#|`code:c#`<br/>`code:csharp`|
|C++|`code:cpp`<br/>`code:c++`<br/>`code:cplusplus`|
|F#|`code:f#`<br/>`code:fsharp`|
|JavaScript|`code:javascript`<br/>`code:js`|
|XAML|`code:xaml`|

> [!NOTE]
> `code:` İşleci yalnızca genel kodu olarak işaretlenmiş içerik aksine bir programlama dili etiketi ile işaretlenmiş içeriği bulur.

## <a name="see-also"></a>Ayrıca bkz.

- [Nasıl yapılır: Konu Arama](how-to-search-for-topics.md)
- [Microsoft Yardım Görüntüleyicisi](microsoft-help-viewer.md)

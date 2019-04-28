---
title: Arama işleçlerini arama ifadelerindeki Gelişmiş | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-general
ms.topic: conceptual
helpviewer_keywords:
- Help Viewer 2.0, searching for keywords
- Help Viewer 2.0, searching code
- Help Viewer 2.0, searching code by programming language
- Help Viewer 2.0, searching titles
- searching code [Help Viewer 2.0]
- searching titles [Help Viewer 2.0]
ms.assetid: 0cdc1746-8481-45ec-9c53-d0d89cdcbd5e
caps.latest.revision: 11
author: gewarren
ms.author: gewarren
manager: jillfra
ms.openlocfilehash: 6befa20bcda7f30896fb2b04fadefb0eb5f21f8d
ms.sourcegitcommit: 47eeeeadd84c879636e9d48747b615de69384356
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "63408400"
---
# <a name="advanced-search-operators-in-search-expressions"></a>Arama İfadelerindeki Gelişmiş Arama İşleçleri
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Gelişmiş arama işleçleri kullanarak aramanızı içerik için daha basit olanlardan daha karmaşık arama ifadeler oluşturarak iyileştirebilirsiniz. Aşağıdaki tabloda gösterildiği gibi bu işleçler, bir sorgu çalıştığı bağlam kısıtlayın.  
  
> [!WARNING]
> Son iki nokta üst üste ve arama motoru için iki noktadan önce boşluk olmaması Gelişmiş arama işleçleri tanıması için girmeniz gerekir.  
  
|Aramak için|Bir yönetim grubuna bağlanmak veya bağlı bir yönetim grubunun özelliklerini düzenlemek için Yönetim çalışma alanında|Örnek|Sonuç|  
|-------------------|---------|-------------|------------|  
|Bir konu başlığının terimi|başlık:|title:binaryreader|Kendi başlıklarında "binaryreader" içeren konulardır.|  
|Bir kod örneği bir terimi|Kod:|Kod: readdouble|Bir kod örneğinde "readdouble" içeren konulardır.|  
|Bir terimi belirli bir programlama dili örneği|Kod: vb:|code:vb:string|Visual Basic örneği "dize" içeren konulardır.|  
|Belirli bir dizin anahtar sözcüğüyle ilişkili konu|Anahtar:|keyword:readbyte|"Readbyte" dizin anahtar sözcüğü ile ilgili konular.|  
  
 Kodu kullanabilirsiniz: işleç çeşitli programlama dilleri, ancak ilgili içeriği bulmak için belirli bir programlama dili ile işaretlenmiş içerik için sonuçları döndürür. Aşağıdaki tabloda bu işleci destekleyen programlama dilleri listeler:  
  
|Programlama dili|Bir yönetim grubuna bağlanmak veya bağlı bir yönetim grubunun özelliklerini düzenlemek için Yönetim çalışma alanında|  
|--------------------------|---------|  
|Visual Basic|Kod: vb<br /><br /> veya<br /><br /> code:visualbasic|  
|C#|code:c#<br /><br /> veya<br /><br /> code:csharp|  
|C++|Kod: cpp<br /><br /> veya<br /><br /> Kod: c ++<br /><br /> veya<br /><br /> code:cplusplus|  
|F#|Kod: f #<br /><br /> veya<br /><br /> code:fsharp|  
|JavaScript|code:javascript<br /><br /> veya<br /><br /> Kod: js|  
|XAML|Kod: xaml|  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Arama ifadelerindeki mantıksal işleçler](../ide/logical-operators-in-search-expressions.md)   
 [Tam Metin Arama İpuçları](../ide/full-text-search-tips.md)

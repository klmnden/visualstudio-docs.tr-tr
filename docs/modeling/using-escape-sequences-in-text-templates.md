---
title: Metin Şablonlarında Çıkış Sıraları Kullanma
ms.date: 11/04/2016
ms.topic: conceptual
helpviewer_keywords:
- text templates, escape sequences
author: gewarren
ms.author: gewarren
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 9c88c9c8769051724855d292bfefb56f69cb8dee
ms.sourcegitcommit: 1fc6ee928733e61a1f42782f832ead9f7946d00c
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/22/2019
ms.locfileid: "60053175"
---
# <a name="using-escape-sequences-in-text-templates"></a>Metin Şablonlarında Çıkış Sıraları Kullanma
Metin şablonu etiketleri oluşturulacak metin şablonlarında ve (C# kodunda yalnızca) kaçış dizileri kullanabilirsiniz kaçış denetim karakterlerini ve tırnak işaretleri.

 Çıkış dosyasının standart kod bloğu için açık ve kapalı etiketleri yazdırmak için etiketler gibi çıkış:

```
\<# ... \#>
```

 Diğer metin şablonu yönerge ve kod bloğu etiketleri ile aynı yapabilirsiniz.

 Ardından bir metin bloğu için kullanılan metin şablonu etiketleri kaçış dizelerini içeriyorsa, aşağıdaki kaçış dizileri kullanabilirsiniz:

- Bir metin şablonu etikete bir kaçış tarafından çift sayıda bulunduğuna (\\) şablonu karakterleri ayrıştırıcı yarısı kaçış karakterleri içerir ve bir metin şablonu etiketi olarak dizisi içerir. Örneğin, metin şablonunda dört kaçış karakterleri varsa, olacaktır iki "\\" oluşturulan dosyanın karakter.

- Metin şablonu etiketi kaçış tek sayıda tarafından öncesinde, (\\) karakterleri, şablon ayrıştırıcının içerecektir yarısını "\\" karakterleri etiketi (\<# veya #>). Etiket, metin şablon etiketi olmasını dikkate alınmaz.

- Kaçış dizisi, (\\) karakter istediğiniz sırayla burada bir denetim karakteri veya bir tırnak işareti (yalnızca C#) çıkışları dışındaki başka bir yerde görünür, karakter doğrudan çıkarır.

## <a name="see-also"></a>Ayrıca Bkz.

- [Nasıl yapılır: Kaçış Dizileri Kullanarak Şablonlardan Şablon Oluşturma](../modeling/how-to-generate-templates-from-templates-by-using-escape-sequences.md)
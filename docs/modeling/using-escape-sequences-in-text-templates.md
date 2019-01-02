---
title: Metin Şablonlarında Çıkış Sıraları Kullanma
ms.date: 11/04/2016
ms.topic: conceptual
helpviewer_keywords:
- text templates, escape sequences
author: gewarren
ms.author: gewarren
manager: douge
ms.workload:
- multiple
ms.prod: visual-studio-dev15
ms.openlocfilehash: 4f38d82ab220b348ad9e74d3c257be1d4e3b9c87
ms.sourcegitcommit: 37fb7075b0a65d2add3b137a5230767aa3266c74
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/02/2019
ms.locfileid: "53887097"
---
# <a name="using-escape-sequences-in-text-templates"></a>Metin Şablonlarında Çıkış Sıraları Kullanma
Metin şablonu etiketleri oluşturulacak metin şablonlarında ve (C# kodunda yalnızca) kaçış dizileri kullanabilirsiniz kaçış denetim karakterlerini ve tırnak işaretleri.

 Çıkış dosyasının standart kod bloğu için açık ve kapalı etiketleri yazdırmak için etiketler gibi çıkış:

```
\<# ... \#>
```

 Diğer metin şablonu yönerge ve kod bloğu etiketleri ile aynı yapabilirsiniz.

 Ardından bir metin bloğu için kullanılan metin şablonu etiketleri kaçış dizelerini içeriyorsa, aşağıdaki kaçış dizileri kullanabilirsiniz:

-   Bir metin şablonu etikete bir kaçış tarafından çift sayıda bulunduğuna (\\) şablonu karakterleri ayrıştırıcı yarısı kaçış karakterleri içerir ve bir metin şablonu etiketi olarak dizisi içerir. Örneğin, metin şablonunda dört kaçış karakterleri varsa, olacaktır iki "\\" oluşturulan dosyanın karakter.

-   Metin şablonu etiketi kaçış tek sayıda tarafından öncesinde, (\\) karakterleri, şablon ayrıştırıcının içerecektir yarısını "\\" karakterleri etiketi (\<# veya #>). Etiket, metin şablon etiketi olmasını dikkate alınmaz.

-   Kaçış dizisi, (\\) karakter istediğiniz sırayla burada bir denetim karakteri veya bir tırnak işareti (yalnızca C#) çıkışları dışındaki başka bir yerde görünür, karakter doğrudan çıkarır.

## <a name="see-also"></a>Ayrıca Bkz.

- [Nasıl yapılır: Çıkış sıraları kullanarak şablonlardan şablon oluşturma](../modeling/how-to-generate-templates-from-templates-by-using-escape-sequences.md)
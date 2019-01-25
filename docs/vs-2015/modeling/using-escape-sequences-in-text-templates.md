---
title: Metin şablonlarında çıkış sıraları kullanma | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-modeling
ms.topic: conceptual
helpviewer_keywords:
- text templates, escape sequences
ms.assetid: 36fff542-2f42-460f-a2d5-03fc76817f3b
caps.latest.revision: 31
author: gewarren
ms.author: gewarren
manager: jillfra
ms.openlocfilehash: aecd53f9321108d429c732cc8b802ee5dfc8a99c
ms.sourcegitcommit: 8b538eea125241e9d6d8b7297b72a66faa9a4a47
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54758418"
---
# <a name="using-escape-sequences-in-text-templates"></a>Metin Şablonlarında Çıkış Sıraları Kullanma
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

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
 [Nasıl yapılır: Çıkış sıraları kullanarak şablonlardan şablon oluşturma](../modeling/how-to-generate-templates-from-templates-by-using-escape-sequences.md)

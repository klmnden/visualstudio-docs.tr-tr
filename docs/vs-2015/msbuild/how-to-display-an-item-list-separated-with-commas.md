---
title: 'Nasıl yapılır: Virgülle ayrılmış bir öğe listesini görüntüleme | Microsoft Docs'
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: msbuild
ms.topic: conceptual
helpviewer_keywords:
- MSBuild, separating items with semicolons
- MSBuild, formatting item collections
ms.assetid: 3cae844c-7c6d-4144-82dc-efad10ba458f
caps.latest.revision: 15
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.openlocfilehash: 93451d6d49082621df48c734de951e6a4bc7e281
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "68156634"
---
# <a name="how-to-display-an-item-list-separated-with-commas"></a>Nasıl yapılır: Virgülle Ayrılmış Bir Öğe Listesini Görüntüleme
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Öğesi ile çalışırken listeleri [!INCLUDE[vstecmsbuildengine](../includes/vstecmsbuildengine-md.md)] ([!INCLUDE[vstecmsbuild](../includes/vstecmsbuild-md.md)]), bu öğe listeleri içeriğini okumak kolay bir şekilde görüntülemek bazen kullanışlıdır. Veya özel ayırıcı dize ile ayrılmış olan öğelerin listesini alan bir görev olabilir. Her iki durumda, bir öğe listesi için bir ayırıcı dize belirtebilirsiniz.  
  
## <a name="separating-items-in-a-list-with-commas"></a>Bir listedeki öğeler virgülle ayırma  
 Varsayılan olarak, [!INCLUDE[vstecmsbuild](../includes/vstecmsbuild-md.md)] listedeki öğeleri ayırmak için noktalı virgül kullanır. Örneğin, bir `Message` şu değere sahip öğe:  
  
 `<Message Text="This is my list of TXT files: @(TXTFile)"/>`  
  
 Zaman `@(TXTFile)` öğe listesi App1.txt App2.txt ve App3.txt öğeleri içeren, ileti şöyle:  
  
 `This is my list of TXT files: App1.txt;App2.txt;App3.txt`  
  
 Varsayılan davranışı değiştirmek isterseniz, kendi ayırıcı belirtebilirsiniz. Bir öğe liste ayırıcı belirtmek için sözdizimi aşağıdaki gibidir:  
  
 `@(ItemListName, '<separator>')`  
  
 Ayırıcı, tek bir karakter veya bir dize olabilir ve tek tırnak içine alınmalıdır.  
  
#### <a name="to-insert-a-comma-and-a-space-between-items"></a>Bir virgül ve öğeleri arasına boşluk eklemek için  
  
- Aşağıdakine benzer bir öğe gösterimini kullanın:  
  
     `@(TXTFile, ', ')`  
  
## <a name="example"></a>Örnek  
 Bu örnekte, [Exec](../msbuild/exec-task.md) görev Phrases.txt dosyasında belirtilen metin dizelerini bulmak için findstr aracını çalıştırır. Findstr komut içinde değişmez değer dizeleri tarafından belirtilen **/c:** geçiş, bunu öğesi ayırıcısı `/c:` bulunan öğeler arasındaki eklenen `@(Phrase)` öğe listesi.  
  
 Bu örnekte, eşdeğer komut satırı komutudur:  
  
 `findstr /i /c:hello /c:world /c:msbuild phrases.txt`  
  
```  
<Project DefaultTargets = "Find"  
    xmlns="http://schemas.microsoft.com/developer/msbuild/2003" >  
  
    <ItemGroup>  
        <Phrase Include="hello"/>  
        <Phrase Include="world"/>  
        <Phrase Include="msbuild"/>  
    </ItemGroup>  
  
    <Target Name = "Find">  
        <!-- Find some strings in a file -->  
        <Exec Command="findstr /i /c:@(Phrase, ' /c:') phrases.txt"/>  
    </Target>  
</Project>  
```  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [MSBuild başvurusu](../msbuild/msbuild-reference.md)   
 [Öğeler](../msbuild/msbuild-items.md)

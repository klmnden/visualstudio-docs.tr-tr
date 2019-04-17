---
title: Kaçış için özel karakterler | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: msbuild
ms.topic: conceptual
dev_langs:
- VB
- CSharp
- C++
- jsharp
helpviewer_keywords:
- special characters to escape
- msbuild, special characters to escape
ms.assetid: 5b5172c3-41e4-4f38-a16f-2aeac831a5fc
caps.latest.revision: 12
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.openlocfilehash: beeed84db240ecf57ca18dd9aef08622f14b06fc
ms.sourcegitcommit: 53aa5a413717a1b62ca56a5983b6a50f7f0663b3
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/17/2019
ms.locfileid: "59659689"
---
# <a name="special-characters-to-escape"></a>Kaçış İçin Özel Karakterler
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Yalnızca özel bir anlamı, kullanıldıkları bağlam içinde oluşturulduysa özel karakterleri kaçış karakterleri eklenmelidir. Örneğin, yıldız işareti (*) bir özel karakter yalnızca bir öğe tanımının "Ekleme" ve "Dışarıda bırak" öznitelikleri veya bir çağrıda olduğu <xref:Microsoft.Build.Tasks.CreateItem>. Diğer durumlarda, yıldız işareti değişmez bir yıldız işareti kabul edilir. Her yerde proje dosyaları yıldız işareti kaçış gerekmez ancak bunun yapılması bir zararı şekilde yapar.  
  
 Gösterim % kullanmak*xx* özel karakter yerine burada *xx* ASCII karakter onaltılık değerini temsil eder. Örneğin, sabit karakter olarak yıldız işareti (*) kullanmak için değerini kullanın. `%2A`.  
  
 Kaçış için özel karakterler tam listesini aşağıdaki gibidir:  
  
|Karakter|Açıklama|  
|---------------|-----------------|  
|%|Meta veri başvurmak için kullanılan yüzde işareti.|  
|$|Dolar işareti, özellikleri başvurmak için kullanılır.|  
|@|Öğe listeleri başvurmak için kullanılan oturum sırasında.|  
|(|Açık parantez, listelerinde kullanılır.|  
|)|Kapatma parantezleri, listelerinde kullanılır.|  
|`| Kesme işareti (veya değer çizgisi), koşullar ve diğer ifadeleri kullanılır.|  
|;|Noktalı virgül, liste ayırıcı.|  
|?|Soru işareti, bir öğenin dahil edin/dışlayın bölümünde bir dosya belirtimi tanımlarken bir joker karakter.|  
|*|Yıldız işareti, bir öğenin dahil edin/dışlayın bölümünde bir dosya belirtimi tanımlarken bir joker karakter.|  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Nasıl yapılır: Msbuild'de kaçış özel karakterleri](../msbuild/how-to-escape-special-characters-in-msbuild.md)   
 [MSBuild Başvurusu](../msbuild/msbuild-reference.md)

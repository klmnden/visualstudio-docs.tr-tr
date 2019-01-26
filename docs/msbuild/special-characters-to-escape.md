---
title: Kaçış için özel karakterler | Microsoft Docs
ms.date: 11/04/2016
ms.topic: reference
dev_langs:
- VB
- CSharp
- C++
- jsharp
helpviewer_keywords:
- special characters to escape
- msbuild, special characters to escape
ms.assetid: 5b5172c3-41e4-4f38-a16f-2aeac831a5fc
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: e0e26755c61960786b37bce5c4be3c21b42630b4
ms.sourcegitcommit: 2193323efc608118e0ce6f6b2ff532f158245d56
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/25/2019
ms.locfileid: "54942159"
---
# <a name="special-characters-to-escape"></a>Kaçış için özel karakterler
Yalnızca özel bir anlamı, kullanıldıkları bağlam içinde oluşturulduysa özel karakterleri kaçış karakterleri eklenmelidir. Örneğin, yıldız işareti (*) bir özel karakter yalnızca bir öğe tanımının "Ekleme" ve "Dışarıda bırak" öznitelikleri veya bir çağrıda olduğu <xref:Microsoft.Build.Tasks.CreateItem>. Diğer durumlarda, yıldız işareti değişmez bir yıldız işareti kabul edilir. Her yerde proje dosyaları yıldız işareti kaçış gerekmez ancak bunun yapılması bir zararı şekilde yapar.  
  
 Gösterim % kullanmak\<xx > özel karakter yerine burada \<xx > ASCII karakter onaltılık değerini temsil eder. Örneğin, sabit karakter olarak yıldız işareti (*) kullanmak için değerini kullanın. `%2A`.  
  
 Kaçış için özel karakterler tam listesini aşağıdaki gibidir:  
  
|Karakter|Açıklama|  
|---------------|-----------------|  
|%|Meta veri başvurmak için kullanılan yüzde işareti.|  
|$|Dolar işareti, özellikleri başvurmak için kullanılır.|  
|@|Öğe listeleri başvurmak için kullanılan oturum sırasında.|  
|(|Açık parantez, listelerinde kullanılır.|  
|)|Kapatma parantezleri, listelerinde kullanılır.|  
|`|Kesme işareti (veya değer çizgisi), koşullar ve diğer ifadeleri kullanılır.|  
|;|Noktalı virgül, liste ayırıcı.|  
|?|Soru işareti, bir öğenin dahil edin/dışlayın bölümünde bir dosya belirtimi tanımlarken bir joker karakter.|  
|*|Yıldız işareti, bir öğenin dahil edin/dışlayın bölümünde bir dosya belirtimi tanımlarken bir joker karakter.|  
  
## <a name="see-also"></a>Ayrıca bkz.  
 [Nasıl yapılır: Msbuild'de kaçış özel karakterleri](../msbuild/how-to-escape-special-characters-in-msbuild.md)   
 [MSBuild başvurusu](../msbuild/msbuild-reference.md)
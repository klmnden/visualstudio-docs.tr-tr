---
title: MSBuild tanınmış öğe meta verileri | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: msbuild
ms.topic: reference
dev_langs:
- VB
- CSharp
- C++
- jsharp
helpviewer_keywords:
- MSBuild, item metadata
- MSBuild, well-known item metadata
ms.assetid: b5e791b5-c68f-4978-ad8a-9247d03bb6c0
caps.latest.revision: 15
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.openlocfilehash: 1bb2e53102221194dc829df162c44bbf04378b28
ms.sourcegitcommit: 53aa5a413717a1b62ca56a5983b6a50f7f0663b3
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/17/2019
ms.locfileid: "59648945"
---
# <a name="msbuild-well-known-item-metadata"></a>MSBuild Tanınmış Öğe Meta Verisi
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Aşağıdaki tabloda, oluşturulduktan sonra her öğeye atanan meta veriler açıklanmaktadır. Her örnekte, aşağıdaki öğe bildirimi dosya eklemek için kullanılan `C:\MyProject\Source\Program.cs` projedeki.  
  
```  
<ItemGroup>  
    <MyItem Include="Source\Program.cs" />  
</ItemGroup>  
```  
  
|Öğe meta verileri|Açıklama|  
|-------------------|-----------------|  
|%(FullPath)|Öğenin tam yolunu içerir. Örneğin:<br /><br /> `C:\MyProject\Source\Program.cs`|  
|%(RootDir)|Öğenin kök dizinini içerir. Örneğin:<br /><br /> `C:\`|  
|%(Filename)|Uzantı olmadan öğenin dosya adını içerir. Örneğin:<br /><br /> `Program`|  
|%(Extension)|Öğesinin dosya adı uzantısını içerir. Örneğin:<br /><br /> `.cs`|  
|%(RelativeDir)|Belirtilen yolu içerir `Include` son eğik çizgiyi kadar bir öznitelik (\\). Örneğin:<br /><br /> `Source\`|  
|%(Directory)|Kök dizin olmadan öğenin dizinini içerir. Örneğin:<br /><br /> `MyProject\Source\`|  
|%(RecursiveDir)|Varsa `Include` öznitelik joker karakter içeren \* \*, bu meta veri joker karakterin yerini alan yolu parçası belirtir. Joker karakterler hakkında daha fazla bilgi için bkz. [nasıl yapılır: Derlenecek dosyaları seçme](../msbuild/how-to-select-the-files-to-build.md).<br /><br /> Varsa klasörü *C:\MySolution\MyProject\Source\\*  Program.cs dosyasını içeren ve proje dosyası bu öğe içeriyorsa:<br /><br /> `<ItemGroup>`<br /><br /> `<MyItem Include="C:\**\Program.cs" />`<br /><br /> `</ItemGroup>`<br /><br /> ardından değerini `%(MyItem.RecursiveDir)` olacaktır *MySolution\MyProject\Source\\* .|  
|%(Identity)|Belirtilen öğe `Include` özniteliği... Örneğin:<br /><br /> `Source\Program.cs`|  
|%(ModifiedTime)|Öğeye erişildiği son zamandan itibaren zaman damgası içerir. Örneğin:<br /><br /> `2004-07-01 00:21:31.5073316`|  
|%(CreatedTime)|Öğesi oluşturulduğu zaman damgası içerir. Örneğin:<br /><br /> `2004-06-25 09:26:45.8237425`|  
|%(AccessedTime)|Öğeye erişildiği son zamandan itibaren zaman damgası içerir.<br /><br /> `2004-08-14 16:52:36.3168743`|  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Öğeleri](../msbuild/msbuild-items.md)   
 [Toplu işleme](../msbuild/msbuild-batching.md)   
 [MSBuild Başvurusu](../msbuild/msbuild-reference.md)

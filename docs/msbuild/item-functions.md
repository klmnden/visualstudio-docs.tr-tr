---
title: Öğe işlevleri | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
helpviewer_keywords:
- msbuild, Item functions
ms.assetid: 5e6df3cc-2db8-4cbd-8fdd-3ffd03ac0876
author: mikejo5000
ms.author: mikejo
manager: douge
ms.workload:
- multiple
ms.openlocfilehash: 5d731cf14fca91920d5da6b6232f1a9bd4feb0b9
ms.sourcegitcommit: 37fb7075b0a65d2add3b137a5230767aa3266c74
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/02/2019
ms.locfileid: "53821299"
---
# <a name="item-functions"></a>Öğe işlevleri
MSBuild 4.0 ile başlayarak, görevleri ve hedefleri kod projesinde öğeleri hakkında bilgi almak için öğe işlevleri çağırabilir. Bu işlevler, başlangıç Distinct() öğeleri basitleştirin ve öğeler arasında döngü daha hızlıdır.  
  
## <a name="string-item-functions"></a>Dize öğe işlevleri  
 Herhangi bir öğeyi değer üzerinde çalışması için .NET Framework dize yöntemlerini ve özelliklerini kullanabilirsiniz. İçin <xref:System.String> yöntemleri, yöntem adını belirtin. İçin <xref:System.String> özellikleri "get_ sonra" özellik adı belirtin.  
  
 Birden çok dizeyi sahip öğeleri için her bir dizenin dize yöntemi veya özelliği çalıştırır.  
  
 Aşağıdaki örnek bu dize öğesi işlevlerinin nasıl kullanılacağı gösterilmektedir.  
  
```xml  
<ItemGroup>  
    <theItem Include="andromeda;tadpole;cartwheel" />  
</ItemGroup>  
  
<Target Name = "go">  
    <Message Text="IndexOf  @(theItem->IndexOf('r'))" />  
    <Message Text="Replace  @(theItem->Replace('tadpole', 'pinwheel'))" />  
    <Message Text="Length   @(theItem->get_Length())" />  
    <Message Text="Chars    @(theItem->get_Chars(2))" />  
</Target>  
  
  <!--  
  Output:  
    IndexOf  3;-1;2  
    Replace  andromeda;pinwheel;cartwheel  
    Length   9;7;9  
    Chars    d;d;r  
  -->  
```  
  
## <a name="intrinsic-item-functions"></a>İç öğe işlevleri  
 Aşağıdaki tabloda, öğeler için kullanılabilen iç işlevleri listeler.  
  
|İşlev|Örnek|Açıklama|  
|--------------|-------------|-----------------|  
|`Count`|`@(MyItem->Count())`|Öğelerin sayısını döndürür.|  
|`DirectoryName`|`@(MyItem->DirectoryName())`|Eşdeğerini döndürür `Path.DirectoryName` her öğe için.|  
|`Distinct`|`@(MyItem->Distinct())`|Farklı bir sahip öğeleri döndürür `Include` değerleri. Meta veri göz ardı edilir. Karşılaştırma büyük/küçük harfe duyarlıdır.|  
|`DistinctWithCase`|`@(MyItem->DistinctWithCase())`|Farklı bir sahip öğeleri döndürür `itemspec` değerleri. Meta veri göz ardı edilir. Karşılaştırma büyük/küçük harfe duyarlıdır.|  
|`Reverse`|`@(MyItem->Reverse())`|Öğeleri ters sırada döndürür.|  
|`AnyHaveMetadataValue`|`@(MyItem->AnyHaveMetadataValue("MetadataName", "MetadataValue"))`|Döndürür bir `boolean` herhangi bir öğeyi belirtilen meta veriler ada ve değere sahip olup olmadığını belirtmek için. Karşılaştırma büyük/küçük harfe duyarlıdır.|  
|`ClearMetadata`|`@(MyItem->ClearMetadata())`|Temizlenmiş meta verilerine öğeleri döndürür. Yalnızca `itemspec` korunur.|  
|`HasMetadata`|`@(MyItem->HasMetadata("MetadataName"))`|Belirtilen meta veri adı sahip öğeleri döndürür. Karşılaştırma büyük/küçük harfe duyarlıdır.|  
|`Metadata`|`@(MyItem->Metadata("MetadataName"))`|Meta veri adı olan meta verileri değerlerini döndürür.|  
|`WithMetadataValue`|`@(MyItem->WithMetadataValue("MetadataName", "MetadataValue"))`|Belirtilen meta veri adı ve değeri sahip öğeleri döndürür. Karşılaştırma büyük/küçük harfe duyarlıdır.|  
  
 Aşağıdaki örnekte, iç öğe işlevleri kullanma işlemini gösterir.  
  
```xml  
<ItemGroup>  
    <TheItem Include="first">  
        <Plant>geranium</Plant>  
    </TheItem>  
    <TheItem Include="second">  
        <Plant>algae</Plant>  
    </TheItem>  
    <TheItem Include="third">  
        <Plant>geranium</Plant>  
    </TheItem>  
</ItemGroup>  
  
<Target Name="go">  
    <Message Text="MetaData:    @(TheItem->Metadata('Plant'))" />  
    <Message Text="HasMetadata: @(theItem->HasMetadata('Plant'))" />  
    <Message Text="WithMetadataValue: @(TheItem->WithMetadataValue('Plant', 'geranium'))" />  
    <Message Text=" " />  
    <Message Text="Count:   @(theItem->Count())" />  
    <Message Text="Reverse: @(theItem->Reverse())" />  
</Target>  
  
  <!--   
  Output:  
    MetaData:    geranium;algae;geranium  
    HasMetadata: first;second;third  
    WithMetadataValue: first;third  
  
    Count:   3  
    Reverse: third;second;first  
  -->  
```  
  
## <a name="see-also"></a>Ayrıca bkz.  
 [Öğeler](../msbuild/msbuild-items.md)

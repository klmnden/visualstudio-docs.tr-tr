---
title: İş Akışı Tasarımcısı - ForEach&lt;T&gt; etkinlik Tasarımcısı
ms.date: 11/04/2016
ms.topic: reference
ms.prod: visual-studio-dev15
f1_keywords:
- System.Activities.Statements.ForEach`1.UI
ms.assetid: 67097b3a-fcf5-4a72-beb1-2c7784151a86
author: gewarren
ms.author: gewarren
manager: douge
ms.workload:
- multiple
ms.openlocfilehash: 681a89bd9c31cc4682e3ba7f5b9b0762f0ad8983
ms.sourcegitcommit: 37fb7075b0a65d2add3b137a5230767aa3266c74
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/02/2019
ms.locfileid: "53830316"
---
# <a name="foreachlttgt-activity-designer"></a>ForEach&lt;T&gt; etkinlik Tasarımcısı

<xref:System.Activities.Statements.ForEach%601> Etkinliği yürütür bulunan etkinlik kendi <xref:System.Activities.Statements.ForEach%601.Body%2A> belirtilen her öğe için <xref:System.Activities.Statements.ForEach%601.Values%2A> koleksiyonu.

## <a name="foreacht-properties-in-the-workflow-designer"></a>ForEach < T\> iş akışı Tasarımcısı özellikleri

Aşağıdaki tabloda en kullanışlı gösterilmektedir <xref:System.Activities.Statements.ForEach%601> etkinlik özellikleri ve tasarımcıda kullanmayı açıklar.

|Özellik Adı|Gerekli|Kullanım|
|-|--------------|-|
|<xref:System.Activities.Activity.DisplayName%2A>|False|Kolay adı <xref:System.Activities.Statements.ForEach%601> etkinlik. ForEach varsayılandır < Int32\>. Ancak <xref:System.Activities.Activity.DisplayName%2A> değeri kesinlikle gerekli değil, kullanmak için en iyi bir uygulamadır.|
|<xref:System.Activities.Statements.ForEach%601.Values%2A>|Doğru|Üzerinden yinelemek için öğeleri koleksiyonu. Ayarlanacak <xref:System.Activities.Statements.ForEach%601.Values%2A>, Visual Basic ifadesindeki türü **değerleri** kutusuna **ForEach < T\>**  etkinlik Tasarımcısı veya özellik kılavuzunda.|
|*TypeArgument*|Doğru|Öğelerin türünü <xref:System.Activities.Statements.ForEach%601.Values%2A> genel parametre tarafından belirtilen koleksiyon *T*. Varsayılan olarak, *TypeArgument* ayarlanır **Int32**. Türü değiştirmek için değerini değiştirmek *TypeArgument* özellik kılavuzunda birleşik giriş kutusu.|

Varsayılan olarak, döngü yineleyici adlı **öğesi**. Yineleyici değişkeni adını değiştirebilirsiniz <xref:System.Activities.Statements.ForEach%601> etkinlik Tasarımcısı. Döngü yineleyici alt ifadelerde kullanılabilir <xref:System.Activities.Statements.ForEach%601> etkinlik.

## <a name="see-also"></a>Ayrıca bkz.

- [ParallelForEach\<T >](../workflow-designer/parallelforeach-t-activity-designer.md)
- [Denetim Akışı](../workflow-designer/control-flow-activity-designers.md)
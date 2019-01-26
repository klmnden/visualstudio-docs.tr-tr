---
title: İş Akışı Tasarımcısı - Parallel etkinlik Tasarımcısı
ms.date: 11/04/2016
ms.topic: reference
ms.prod: visual-studio-dev15
f1_keywords:
- System.Activities.Statements.Parallel.UI
ms.assetid: 0306dc3b-075a-4091-ac3a-96486fbabed5
author: gewarren
ms.author: gewarren
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: adc84c10f703488357adcee7739c46183f8c2e85
ms.sourcegitcommit: 2193323efc608118e0ce6f6b2ff532f158245d56
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/25/2019
ms.locfileid: "54925805"
---
# <a name="parallel-activity-designer"></a>Parallel Etkinlik Tasarımcısı

<xref:System.Activities.Statements.Parallel> Etkinliği çocuk etkinliklerinin bir koleksiyonu aynı anda yürütür.

## <a name="the-parallel-activity"></a>Paralel etkinlik

<xref:System.Activities.Statements.Parallel> Etkinlik alt etkinlikleriyle depolayan bir <xref:System.Activities.Statements.Parallel.Branches%2A> koleksiyonu. Kullanım <xref:System.Activities.Statements.Parallel> yerine etkinlik <xref:System.Activities.Statements.Sequence> çocuk etkinliklerinin bazıları boş giderseniz etkinlik.

<xref:System.Activities.Statements.Parallel> Etkinliğinde bir <xref:System.Activities.Statements.Parallel.CompletionCondition%2A> içeren bir kullanıcı özelliği belirtilen Visual Basic ifade. <xref:System.Activities.Statements.Parallel> Her dal tamamlandıktan sonra bu özellik etkinlik değerlendirir. Değerlendirilirse **True**, ardından <xref:System.Activities.Statements.Parallel> etkinliği tamamlandıktan diğer dalları çalıştırmadan. Varsa <xref:System.Activities.Statements.Parallel.CompletionCondition%2A> için değerlendirilmiyor **True**, ardından <xref:System.Activities.Statements.Parallel> etkinliği tamamlandıktan tüm alt etkinliklerinin tamamladıktan sonra.

### <a name="using-the-parallel-activity-designer"></a>Paralel etkinlik Tasarımcısını kullanma

Erişim **paralel** etkinlik Tasarımcısı'nda **akış denetimi** kategorisi **araç kutusu**.

**Paralel** etkinlik Tasarımcısı, gelen sürüklenebilir **araç kutusu** ve etkinlik tasarımcıları normalde, örneğin, bir içineyerleştirilenheryerdeişakışıTasarımcısıyüzeyineaçınbırakılan**Dizisi** etkinlik Tasarımcısı. İş akışı tasarımcıya bırakılırken sonra oluşturduğu bir <xref:System.Activities.Statements.Parallel> içeren varsayılan olarak, etkinlik bir <xref:System.Activities.Activity.DisplayName%2A> , **paralel**

Bir etkinlik eklemek için <xref:System.Activities.Statements.Parallel.Branches%2A> paralel etkinlik koleksiyonunu sürükleyin bazı diğer etkinlik Tasarımcısı'ndan **araç kutusu** ve bu üçgen bırak **paralel** etkinlik Tasarımcısı. Bu üçgen dalları etkinlikleri flank. Bu yordamı tekrarlayarak ek etkinlikler eklenebilir. Etkinlikler, bunların içinde sürükleyip bırakarak sıralanabilir **paralel** etkinlik Tasarımcısı.

### <a name="parallel-activity-properties-in-the-workflow-designer"></a>İş akışı tasarımcısında paralel etkinlik özellikleri

Aşağıdaki tabloda, paralel etkinlik özelliklerini gösterir ve Tasarımcısı'nda nasıl kullanıldığını açıklar.

|Özellik Adı|Gerekli|Kullanım|
|-|--------------|-|
|<xref:System.Activities.Activity.DisplayName%2A>|False|Üst bilgide etkinlik Tasarımcısı kolay görünen adını belirtir. Varsayılan değer **paralel**. Değer, isteğe bağlı olarak düzenlenebilir **özellikleri** kılavuz veya doğrudan etkinlik Tasarımcısı başlığı.|
|<xref:System.Activities.Statements.Parallel.Branches%2A>|Doğru|Yürütülecek çocuk etkinliklerinin koleksiyonunu içerir.|
|<xref:System.Activities.Statements.Parallel.CompletionCondition%2A>|False|Bir dal tamamlandıktan sonra değerlendirilir. Değerlendirilirse **True**, ardından zamanlanmış dalları iptal edilir. Bu özelliği ayarlı değil veya değerlendiren **False**, tüm alt etkinliklerinin tamamladığında etkinliği tamamlar. Varsayılan değer **null**.|

## <a name="see-also"></a>Ayrıca bkz.

- [Sequence](../workflow-designer/sequence-activity-designer.md)
- [ParallelForEach\<T >](../workflow-designer/parallelforeach-t-activity-designer.md)
- [Denetim Akışı](../workflow-designer/control-flow-activity-designers.md)
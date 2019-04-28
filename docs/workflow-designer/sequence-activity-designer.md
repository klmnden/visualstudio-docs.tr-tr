---
title: İş Akışı Tasarımcısı - Sequence etkinlik Tasarımcısı
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- System.Activities.Statements.Sequence.UI
ms.assetid: 51c8d3cb-4d43-458f-9631-b63755f9ac94
author: gewarren
ms.author: gewarren
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: abbffa44ee7fa4db2a03e5f46820f707cae8d4fb
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62434091"
---
# <a name="sequence-activity-designer"></a>Sequence Etkinlik Tasarımcısı

<xref:System.Activities.Statements.Sequence> Etkinlik sırayla yürütülen bir alt etkinlik sıralı bir koleksiyonunu içerir.

Sırayla bir dizi etkinliği yürütmek için başka bir yolu bir <xref:System.Activities.Statements.Flowchart> etkinlik. Kullanmayı [akış](../workflow-designer/flowchart-activity-designer.md) basit dallanma veya diagrammatically modellemek için istediğiniz program akışı döngü olduğunda.

## <a name="using-the-sequence-activity-designer"></a>Sıralı etkinlik Tasarımcısını kullanma

Eklemek için bir <xref:System.Activities.Statements.Sequence> etkinliğini sürükleyip **dizisi** etkinlik Tasarımcısı'ndan **araç kutusu** açın iş akışı Tasarımcısı yüzeyine bırakın. Bunun için bir alt etkinlik eklemek için <xref:System.Activities.Statements.Sequence> etkinlik, diğer bazı etkinliğinden sürükleyin **araç kutusu** ve bu üçgen İpucu metin kutusunda "etkinliği buraya bırakın" bırakın.

### <a name="sequence-activity-properties-in-the-workflow-designer"></a>Sıralı iş akışı tasarımcısında etkinlik özellikleri

Aşağıdaki tabloda <xref:System.Activities.Statements.Sequence> özellikleri Tasarımcısı'nda nasıl kullanıldığı açıklanmaktadır. Bu özellikler, özellik kılavuzu veya tasarımcı yüzeyine düzenlenebilir.

|Özellik Adı|Gerekli|Kullanım|
|-|--------------|-|
|<xref:System.Activities.Activity.DisplayName%2A>|False|Kolay adı belirtir <xref:System.Activities.Statements.Sequence> üst bilgisindeki etkinlik Tasarımcısı. Varsayılan değer sırasıdır. Değer özellik kılavuzunda veya etkinlik Tasarımcısı başlığındaki doğrudan düzenleyebilirsiniz.<br /><br /> Ancak <xref:System.Activities.Activity.DisplayName%2A> kati şekilde gerekli değil kullanmak için en iyi bir uygulamadır.|

## <a name="see-also"></a>Ayrıca bkz.

- [Akış Çizelgesi](../workflow-designer/flowchart-activity-designer.md)
- [Denetim Akışı](../workflow-designer/control-flow-activity-designers.md)
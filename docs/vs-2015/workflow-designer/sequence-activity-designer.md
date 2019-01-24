---
title: Sequence etkinlik Tasarımcısı | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-workflow-designer
ms.topic: reference
f1_keywords:
- System.Activities.Statements.Sequence.UI
ms.assetid: 51c8d3cb-4d43-458f-9631-b63755f9ac94
caps.latest.revision: 5
author: gewarren
ms.author: gewarren
manager: jillfra
ms.openlocfilehash: 47743feae8c256aa0ddb4e3270aca32b108aa5d1
ms.sourcegitcommit: 8b538eea125241e9d6d8b7297b72a66faa9a4a47
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54799120"
---
# <a name="sequence-activity-designer"></a>Sequence Etkinlik Tasarımcısı
<xref:System.Activities.Statements.Sequence> Etkinlik sırayla yürütülen bir alt etkinlik sıralı bir koleksiyonunu içerir.  
  
 Sırayla bir dizi etkinliği yürütmek için başka bir yolu bir <xref:System.Activities.Statements.Flowchart> etkinlik. Kullanmayı [akış](../workflow-designer/flowchart-activity-designer.md) basit dallanma veya diagrammatically modellemek için istediğiniz program akışı döngü olduğunda.  
  
## <a name="using-the-sequence-activity-designer"></a>Sıralı etkinlik Tasarımcısını kullanma  
 Eklemek için bir <xref:System.Activities.Statements.Sequence> etkinliğini sürükleyip **dizisi** etkinlik Tasarımcısı'ndan **araç kutusu** oturum bırakın [!INCLUDE[wfd1](../includes/wfd1-md.md)] yüzeyi. Bunun için bir alt etkinlik eklemek için <xref:System.Activities.Statements.Sequence> etkinlik, diğer bazı etkinliğinden sürükleyin **araç kutusu** ve bu üçgen İpucu metin kutusunda "etkinliği buraya bırakın" bırakın.  
  
### <a name="sequence-activity-properties-in-the-workflow-designer"></a>Sıralı iş akışı tasarımcısında etkinlik özellikleri  
 Aşağıdaki tabloda <xref:System.Activities.Statements.Sequence> özellikleri Tasarımcısı'nda nasıl kullanıldığı açıklanmaktadır. Bu özellikler, özellik kılavuzu veya tasarımcı yüzeyine düzenlenebilir.  
  
|Özellik Adı|Gerekli|Kullanım|  
|-------------------|--------------|-----------|  
|<xref:System.Activities.Activity.DisplayName%2A>|False|Kolay adı belirtir <xref:System.Activities.Statements.Sequence> üst bilgisindeki etkinlik Tasarımcısı. Varsayılan değer sırasıdır. Değer özellik kılavuzunda veya etkinlik Tasarımcısı başlığındaki doğrudan düzenleyebilirsiniz.<br /><br /> Ancak <xref:System.Activities.Activity.DisplayName%2A> kati şekilde gerekli değil kullanmak için en iyi bir uygulamadır.|  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Akış Çizelgesi](../workflow-designer/flowchart-activity-designer.md)   
 [Denetim Akışı](../workflow-designer/control-flow-activity-designers.md)
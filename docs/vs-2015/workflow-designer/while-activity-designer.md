---
title: While etkinlik Tasarımcısı | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-workflow-designer
ms.topic: reference
f1_keywords:
- System.Activities.Statements.While.UI
ms.assetid: ea008091-2e4c-4f64-bfa5-afb919552446
caps.latest.revision: 5
author: gewarren
ms.author: gewarren
manager: jillfra
ms.openlocfilehash: 36752df3d8ffbf33b8ea95570d6a4efe8c8cd3be
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62855405"
---
# <a name="while-activity-designer"></a>While Etkinlik Tasarımcısı

<xref:System.Activities.Statements.While> Etkinliği yürütür bulunan etkinlik kendi <xref:System.Activities.Statements.While.Body%2A> değerlendiren belirtilen koşulu sırada **true**. Hiçbir zaman, içerilen bir etkinliği yürütür. İçerilen bir etkinliği en az bir kez yürütülmesini istediğiniz kullanırsanız <xref:System.Activities.Statements.DoWhile> etkinliği bunun yerine.

## <a name="while-properties-in-workflow-designer"></a>Çalışırken iş akışı Tasarımcısı özellikleri

Aşağıdaki tabloda en kullanışlı gösterilmektedir <xref:System.Activities.Statements.While> etkinlik özellikleri Tasarımcısı'nda nasıl kullanıldığı açıklanmaktadır.

|Özellik Adı|Gerekli|Kullanım|
|-------------------|--------------|-----------|
|<xref:System.Activities.Activity.DisplayName%2A>|False|Kolay adı belirtir <xref:System.Activities.Statements.While> üst bilgisindeki etkinlik Tasarımcısı. Varsayılan değer sırada. Değer içinde düzenlenebilir **özellikleri** penceresi veya doğrudan etkinlik Tasarımcısı başlığı.<br /><br /> Ancak <xref:System.Activities.Activity.DisplayName%2A> kati şekilde gerekli değil kullanmak için en iyi bir uygulamadır.|
|<xref:System.Activities.Statements.While.Body%2A>|False|Yürütülecek etkinliği içeren sırada <xref:System.Activities.Statements.While.Condition%2A> değerlendiren **true**.|
|<xref:System.Activities.Statements.While.Condition%2A>|Doğru|İçeren [!INCLUDE[vbprvb](../includes/vbprvb-md.md)] belirlemek için değerlendirilen bir ifade olup olmadığını etkinliğinde <xref:System.Activities.Statements.While.Body%2A> yürütülür.|

## <a name="see-also"></a>Ayrıca bkz.

- [Denetim Akışı](../workflow-designer/control-flow-activity-designers.md)
- [DoWhile](../workflow-designer/dowhile-activity-designer.md)
---
title: DoWhile etkinlik Tasarımcısı | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-workflow-designer
ms.topic: reference
f1_keywords:
- System.Activities.Statements.DoWhile.UI
ms.assetid: 948deb35-d72f-462b-bea6-4b119c10a148
caps.latest.revision: 7
author: gewarren
ms.author: gewarren
manager: jillfra
ms.openlocfilehash: d09954409baccfdc5d9eb083a15bd02f5d16cb85
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62785268"
---
# <a name="dowhile-activity-designer"></a>DoWhile Etkinlik Tasarımcısı
<xref:System.Activities.Statements.DoWhile> Etkinliği yürütür bulunan etkinlik kendi <xref:System.Activities.Statements.DoWhile.Body%2A> en az bir kez, belirtilen bir koşulu olana kadar **false**. Sıfır veya daha fazla kez kullanım yürütülecek bir döngü gövdesinde yer alan etkinlik gerekiyorsa <xref:System.Activities.Statements.While> etkinliği bunun yerine.  
  
## <a name="dowhile-properties-in-the-workflow-designer"></a>İş akışı tasarımcısında DoWhile özellikleri  
 Aşağıdaki tabloda en kullanışlı gösterilmektedir <xref:System.Activities.Statements.DoWhile> etkinlik özellikleri ve tasarımcıda kullanmayı açıklar.  
  
|Özellik Adı|Gerekli|Kullanım|  
|-------------------|--------------|-----------|  
|<xref:System.Activities.Statements.DoWhile.Body%2A>|False|Koşulu sırada yürütmek için etkinlik **true**. Eklemek için <xref:System.Activities.Statements.DoWhile.Body%2A> etkinlik, etkinlik araç kutusundan bir bırakma **gövdesi** kutusuna **DoWhile** etkinlik Tasarımcısı ile "Etkinliği buraya bırakın" İpucu metni.|  
|<xref:System.Activities.Statements.DoWhile.Condition%2A>|Doğru|Döngünün her yinelemesinden sonra değerlendirilecek koşul. Ayarlanacak <xref:System.Activities.Statements.DoWhile.Condition%2A>, tür a [!INCLUDE[vbprvb](../includes/vbprvb-md.md)] ifadesinde **koşul** kutusuna **DoWhile** etkinlik Tasarımcısı veya özellik kılavuzunda.|  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [while](../workflow-designer/while-activity-designer.md)   
 [Denetim Akışı](../workflow-designer/control-flow-activity-designers.md)
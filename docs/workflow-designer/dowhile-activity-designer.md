---
title: İş Akışı Tasarımcısı - DoWhile etkinlik Tasarımcısı
ms.date: 11/04/2016
ms.topic: reference
ms.prod: visual-studio-dev15
f1_keywords:
- System.Activities.Statements.DoWhile.UI
ms.assetid: 948deb35-d72f-462b-bea6-4b119c10a148
author: gewarren
ms.author: gewarren
manager: douge
ms.workload:
- multiple
ms.openlocfilehash: bc96d44a38a0cf8a1865de236b9f7ef473c960a7
ms.sourcegitcommit: 37fb7075b0a65d2add3b137a5230767aa3266c74
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/02/2019
ms.locfileid: "53960436"
---
# <a name="dowhile-activity-designer"></a>DoWhile Etkinlik Tasarımcısı

<xref:System.Activities.Statements.DoWhile> Etkinliği yürütür bulunan etkinlik kendi <xref:System.Activities.Statements.DoWhile.Body%2A> en az bir kez, belirtilen bir koşulu olana kadar **false**. Sıfır veya daha fazla kez kullanım yürütülecek bir döngü gövdesinde yer alan etkinlik gerekiyorsa <xref:System.Activities.Statements.While> etkinliği bunun yerine.

## <a name="dowhile-properties-in-the-workflow-designer"></a>İş akışı tasarımcısında DoWhile özellikleri

Aşağıdaki tabloda en kullanışlı gösterilmektedir <xref:System.Activities.Statements.DoWhile> etkinlik özellikleri ve tasarımcıda kullanmayı açıklar:

|Özellik Adı|Gerekli|Kullanım|
|-|--------------|-|
|<xref:System.Activities.Statements.DoWhile.Body%2A>|False|Koşulu sırada yürütmek için etkinlik **true**. Eklemek için <xref:System.Activities.Statements.DoWhile.Body%2A> etkinlik, etkinlik araç kutusundan bir bırakma **gövdesi** kutusuna **DoWhile** etkinlik Tasarımcısı ile "Etkinliği buraya bırakın" İpucu metni.|
|<xref:System.Activities.Statements.DoWhile.Condition%2A>|Doğru|Döngünün her yinelemesinden sonra değerlendirilecek koşul. Ayarlanacak <xref:System.Activities.Statements.DoWhile.Condition%2A>, Visual Basic ifadesindeki türü **koşul** kutusuna **DoWhile** etkinlik Tasarımcısı veya özellik kılavuzunda.|

## <a name="see-also"></a>Ayrıca bkz.

- [While](../workflow-designer/while-activity-designer.md)
- [Denetim Akışı](../workflow-designer/control-flow-activity-designers.md)
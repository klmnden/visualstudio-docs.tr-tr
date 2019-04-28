---
title: İş Akışı Tasarımcısı - StateMachine etkinlik Tasarımcısı
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- StateMachine Designer
- System.Activities.Statements.StateMachine.UI
ms.assetid: 474d5fb3-1049-4b3f-bc6b-7524dbbe1672
ms.author: gewarren
manager: jillfra
ms.workload:
- multiple
author: gewarren
ms.openlocfilehash: 59b1a194f4f301bd3080820b56c89044315c66e7
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62809399"
---
# <a name="statemachine-activity-designer"></a>StateMachine Etkinlik Tasarımcısı

<xref:System.Activities.Statements.StateMachine> Etkinliği durumları koleksiyonunu içeren ve tanıdık durum makine paradigma kullanarak iş akışları modeller.

## <a name="using-the-statemachine-activity-designer"></a>StateMachine etkinlik Tasarımcısı kullanma

Eklemek için bir <xref:System.Activities.Statements.StateMachine> etkinliğini sürükleyip **StateMachine** etkinlik Tasarımcısı'ndan **Durum makinesi** bölümünü **araç kutusu** ve iş akışı tasarımcısını açın bırakın Surface. Bunun için bir alt durum eklemek için <xref:System.Activities.Statements.StateMachine> etkinliğini sürükleyip bir <xref:System.Activities.Statements.State> veya <xref:System.Activities.Core.Presentation.FinalState> gelen **araç kutusu** üzerine bırakın **StateMachine**.

### <a name="statemachine-activity-properties-in-the-workflow-designer"></a>Durum makinesi iş akışı tasarımcısında etkinlik özellikleri

Aşağıdaki tabloda <xref:System.Activities.Statements.StateMachine> iş akışı Tasarımcısı'nı kullanarak ayarlanabilir ve Tasarımcısı'nda nasıl kullanıldığını açıklar. Bu özellikler, özellik kılavuzunda düzenlenebilir ve bazı Tasarımcı yüzeyinde düzenlenebilir.

|Özellik Adı|Gerekli|Kullanım|
|-|--------------|-|
|<xref:System.Activities.Activity.DisplayName%2A>|False|Kolay adı belirtir <xref:System.Activities.Statements.StateMachine> üst bilgisindeki etkinlik Tasarımcısı. Varsayılan değer **StateMachine**. Değer özellik kılavuzunda veya etkinlik Tasarımcısı başlığındaki doğrudan düzenleyebilirsiniz. <xref:System.Activities.Activity.DisplayName%2A> İş akışı Tasarımcısı üst kısmında görüntülenen içerik haritalı gezinme kullanılır.<br /><br /> Ancak <xref:System.Activities.Activity.DisplayName%2A> kati şekilde gerekli değil kullanmak için en iyi bir uygulamadır.|

## <a name="see-also"></a>Ayrıca bkz.

- [Akış Çizelgesi](../workflow-designer/flowchart-activity-designer.md)
- [Denetim Akışı](../workflow-designer/control-flow-activity-designers.md)
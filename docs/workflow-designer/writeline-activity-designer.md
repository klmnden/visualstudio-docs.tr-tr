---
title: İş Akışı Tasarımcısı - WriteLine etkinlik Tasarımcısı
ms.date: 11/04/2016
ms.topic: reference
ms.prod: visual-studio-dev15
f1_keywords:
- System.Activities.Statements.WriteLine.UI
ms.assetid: 1b5f29a8-b7fd-477e-949e-2f689cae3c96
author: gewarren
ms.author: gewarren
manager: douge
ms.workload:
- multiple
ms.openlocfilehash: baea87d2ab750da3ee0cfef2450ec0ad04d231cc
ms.sourcegitcommit: 37fb7075b0a65d2add3b137a5230767aa3266c74
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/02/2019
ms.locfileid: "53857549"
---
# <a name="writeline-activity-designer"></a>WriteLine Etkinlik Tasarımcısı

**WriteLine** etkinlik Tasarımcısı oluşturmak ve yapılandırmak için kullanılan bir <xref:System.Activities.Statements.WriteLine> etkinlik.

## <a name="the-writeline-activity"></a>WriteLine etkinlik

<xref:System.Activities.Statements.WriteLine> Etkinlik metni belirtilen bir yazar <xref:System.IO.TextWriter> nesne. Hayır ise <xref:System.IO.TextWriter> belirtilen <xref:System.Activities.Statements.WriteLine> metin konsola yazar.

### <a name="using-the-writeline-activity-designer"></a>WriteLine etkinlik Tasarımcısı kullanma

Erişim **WriteLine** etkinlik Tasarımcısı'nda **Temelleri** kategorisi **araç kutusu**. **WriteLine** etkinlik Tasarımcısı, gelen sürüklenebilir **araç kutusu** ve etkinlikleri genellikle yerleştirilen her yerde, gibi olarak içinde iş akışı Tasarımcısı yüzeyine açın bırakılan bir <xref:System.Activities.Statements.Sequence>. Bu, oluşturur bir <xref:System.Activities.Statements.WriteLine> etkinliği ile bir varsayılan <xref:System.Activities.Activity.DisplayName%2A> WriteLine biri. <xref:System.Activities.Activity.DisplayName%2A> Üst bilgisinde düzenlenebilir **WriteLine** etkinlik Tasarımcısı veya **DisplayName** özellik kılavuzunda kutusu.

### <a name="the-writeline-properties"></a>WriteLine özellikleri

Aşağıdaki tabloda <xref:System.Activities.Statements.WriteLine> özellikleri Tasarımcısı'nda nasıl kullanıldığı açıklanmaktadır. Bu özellikler, özellik kılavuzunda düzenlenebilir ve bunlardan bazıları iş akışı Tasarımcısı yüzeyine düzenlenebilir.

|Özellik Adı|Gerekli|Kullanım|
|-|--------------|-|
|<xref:System.Activities.Activity.DisplayName%2A>|False|Kolay adı <xref:System.Activities.Statements.WriteLine> etkinlik. WriteLine varsayılandır. Ancak <xref:System.Activities.Activity.DisplayName%2A> kati şekilde gerekli değil bir kullanmak için en iyi bir uygulamadır.|
|<xref:System.Activities.Statements.WriteLine.Text%2A>|False|Yazılacak metin. Özellik ayarlamak için bir Visual Basic ifadesinin türü **metin** kutusuna **WriteLine** etkinlik Tasarımcısı veya özellik kılavuzunda.|
|<xref:System.Activities.Statements.WriteLine.TextWriter%2A>|False|<xref:System.IO.TextWriter> Hangi <xref:System.Activities.Statements.WriteLine> Yazar <xref:System.Activities.Statements.WriteLine.Text%2A>. Konsol varsayılandır.|

## <a name="see-also"></a>Ayrıca bkz.

- [Temel Türler](../workflow-designer/primitives-activity-designers.md)
- [Assign](../workflow-designer/assign-activity-designer.md)
- [Delay](../workflow-designer/delay-activity-designer.md)
- [InvokeMethod](../workflow-designer/invokemethod-activity-designer.md)
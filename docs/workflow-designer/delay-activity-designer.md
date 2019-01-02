---
title: İş Akışı Tasarımcısı - Delay etkinlik Tasarımcısı
ms.date: 11/04/2016
ms.topic: reference
ms.prod: visual-studio-dev15
f1_keywords:
- System.Activities.Statements.Delay.UI
ms.assetid: f51742a8-2c9a-47d1-8a23-18459d03ae19
author: gewarren
ms.author: gewarren
manager: douge
ms.workload:
- multiple
ms.openlocfilehash: 6c793456cd32d6d5749bcda8c8d266f6cd939601
ms.sourcegitcommit: 37fb7075b0a65d2add3b137a5230767aa3266c74
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/02/2019
ms.locfileid: "53823668"
---
# <a name="delay-activity-designer"></a>Delay Etkinlik Tasarımcısı

**Gecikme** etkinlik Tasarımcısı oluşturmak ve yapılandırmak için kullanılan bir <xref:System.Activities.Statements.Delay> etkinlik.

## <a name="the-delay-activity"></a>Delay etkinlik

<xref:System.Activities.Statements.Delay> Etkinlik belirtilen bir süre için bir iş akışı yürütülmesini geciktirir.

### <a name="use-the-delay-activity-designer"></a>Delay etkinlik Tasarımcısı kullanma

**Gecikme** etkinlik Tasarımcısı bulunabilir **Temelleri** kategorisi **araç kutusu**, hangi erişilen tıklayarak **araç kutusu**iş akışı Tasarımcısı için sekmesinde. Alternatif olarak, seçin **araç kutusu** gelen **görünümü** tuşuna basın veya menü **Ctrl**+**Alt** + **X**.

**Gecikme** etkinlik Tasarımcısı, gelen sürüklenebilir **araç kutusu** ve etkinlikleri genellikle yerleştirilen her yerde, gibi olarak içinde iş akışı Tasarımcısı yüzeyine açın bırakılan bir <xref:System.Activities.Statements.Sequence>. Etkinlik Tasarımcısı bırakarak oluşturur bir <xref:System.Activities.Statements.Delay> etkinliği ile bir varsayılan <xref:System.Activities.Activity.DisplayName%2A> gecikme. <xref:System.Activities.Activity.DisplayName%2A> Üst bilgisinde düzenlenebilir **gecikme** etkinlik Tasarımcısı veya **DisplayName** özellik kılavuzunda kutusu.

### <a name="the-delay-properties"></a>Gecikmeli Özellikler

Aşağıdaki tabloda <xref:System.Activities.Statements.Delay> özelliklerini ve bunların Tasarımcısı'nda nasıl kullanıldığı açıklanmaktadır. Bu özellikler, özellik kılavuzunda düzenlenebilir ve bunlardan bazıları iş akışı Tasarımcısı yüzeyine düzenlenebilir.

|Özellik Adı|Gerekli|Kullanım|
|-|--------------|-|
|<xref:System.Activities.Activity.DisplayName%2A>|False|Kolay adı <xref:System.Activities.Statements.Delay> etkinlik. Gecikme varsayılandır. Ancak <xref:System.Activities.Activity.DisplayName%2A> değeri kesinlikle gerekli değildir, kullanmak için en iyi bir uygulamadır.|
|<xref:System.Activities.Statements.Delay.Duration%2A>|Doğru|İş akışı gecikme süre miktarı. Bu özellik, özellik kılavuzunda ayarlanır. Bir sabit değer yazın ya da <xref:System.TimeSpan> 00:00:00 biçimi veya süreyi belirtmek için bir Visual Basic ifade.|

## <a name="see-also"></a>Ayrıca bkz.

- [Temel Türler](../workflow-designer/primitives-activity-designers.md)
- [Assign](../workflow-designer/assign-activity-designer.md)
- [Delay Etkinlik Tasarımcısı](../workflow-designer/delay-activity-designer.md)
- [InvokeMethod](../workflow-designer/invokemethod-activity-designer.md)
- [WriteLine](../workflow-designer/writeline-activity-designer.md)
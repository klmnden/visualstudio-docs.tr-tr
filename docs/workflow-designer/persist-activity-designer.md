---
title: İş Akışı Tasarımcısı-kalıcı etkinlik Tasarımcısı
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- System.Activities.Statements.Persist.UI
ms.assetid: be8648dd-3eb9-4a50-8ec1-57a8be804692
author: gewarren
ms.author: gewarren
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 7be70d18b1fc8ff12e2d1fb177b41775954334ed
ms.sourcegitcommit: e98db44f3a33529b0ba188d24390efd09e548191
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/25/2019
ms.locfileid: "71254843"
---
# <a name="persist-activity-designer"></a>Persist Etkinlik Tasarımcısı

**Kalıcı** etkinlik Tasarımcısı, <xref:System.Activities.Statements.Persist> etkinlik oluşturmak ve yapılandırmak için kullanılır.

## <a name="the-persist-activity"></a>Kalıcı etkinlik

<xref:System.Activities.Statements.Persist> Etkinlik, mümkünse bir iş akışını diske kaydeder. Etkinlik, örneğin bir <xref:System.Activities.Statements.TransactionScope> etkinlik içinde, kalıcılık olmayan bir bölgede yürütülemez. <xref:System.Activities.Statements.Persist> Kalıcı olmayan bir kapsamda <xref:System.Activities.Statements.Persist> etkinlik kullanıyorsanız, çalışma zamanında bir özel durum oluşturulur.

### <a name="using-the-persist-activity-designer"></a>Kalıcı etkinlik tasarımcısını kullanma

**Kalıcı** etkinlik **Tasarımcısı araç kutusu sekmesine** tıklanarak erişilen (alternatif olarak, **Görünüm** menüsünden **araç kutusu** ' nu veya Ctrl + Alt + X ' i seçerek **),** **çalışma alanının çalışma zamanı** kategorisinde bulunabilir.

**Kalıcı** etkinlik Tasarımcısı **araç kutusundan** sürüklenip, örneğin içinde <xref:System.Activities.Statements.Sequence>olduğu gibi etkinliklerin genellikle yerleştirildiği iş akışı Tasarımcısı yüzeyine bırakılabilir. Bu, varsayılan <xref:System.Activities.Statements.Persist> olarak **görünmeyen** bir etkinlik oluşturur. , <xref:System.Activities.Activity.DisplayName%2A> **Kalıcı** etkinlik tasarımcısının üst bilgisinde veya özellik kılavuzunun **DisplayName** kutusunda düzenlenebilir.

### <a name="the-persist-properties"></a>Devam eden özellikler

Aşağıdaki tabloda <xref:System.Activities.Statements.Persist> özellikler gösterilmektedir ve bunların tasarımcıda nasıl kullanıldığı açıklanmaktadır. Bu özellikler özellik kılavuzunda düzenlenebilir ve bazıları İş Akışı Tasarımcısı yüzeyinde düzenlenebilirler.

|Özellik Adı|Gerekli|Kullanım|
|-|--------------|-|
|<xref:System.Activities.Activity.DisplayName%2A>|False|<xref:System.Activities.Statements.Persist> Etkinliğin kolay adı. Varsayılan değer korunur. Görünen ad kesinlikle gerekli olmasa da, bir görünen ad kullanmak en iyi uygulamadır.|

## <a name="see-also"></a>Ayrıca bkz.

- [Çalışma Zamanı](../workflow-designer/runtime-activity-designers.md)
- [TerminateWorkflow](../workflow-designer/terminateworkflow-activity-designer.md)
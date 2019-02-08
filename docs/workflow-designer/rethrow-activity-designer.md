---
title: İş Akışı Tasarımcısı - Rethrow etkinlik Tasarımcısı
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- System.Activities.Statements.Rethrow.UI
ms.assetid: 9cfa2eda-395f-4cf3-9154-83fadd4f7452
author: gewarren
ms.author: gewarren
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 558ff5a36d172b8cd1fef0b811d1eaa920b90c6d
ms.sourcegitcommit: 21d667104199c2493accec20c2388cf674b195c3
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/08/2019
ms.locfileid: "55913882"
---
# <a name="rethrow-activity-designer"></a>Rethrow Etkinlik Tasarımcısı

**Rethrow** etkinlik Tasarımcısı oluşturmak ve yapılandırmak için kullanılan bir <xref:System.Activities.Statements.Rethrow> etkinlik.

## <a name="the-rethrow-activity"></a>Rethrow etkinlik

<xref:System.Activities.Statements.Rethrow> Etkinlik, daha önce oluşturulan bir özel durum oluşturur. Bu etkinlik yalnızca kullanılabilir bir <xref:System.Activities.Statements.Catch> işleyicisinde <xref:System.Activities.Statements.TryCatch> etkinlik.

### <a name="use-the-rethrow-activity-designer"></a>ReThrow etkinlik Tasarımcısı kullanma

Erişim **Rethrow** etkinlik Tasarımcısı'nda **hata işleme** kategorisi **araç kutusu**. **Rethrow** etkinlik Tasarımcısı, gelen sürüklenebilir **araç kutusu** ve etkinlikleri genellikle yerleştirilen her yerde, gibi olarak içinde iş akışı Tasarımcısı yüzeyine açın bırakılan bir <xref:System.Activities.Statements.Sequence>. Etkinlik Tasarımcısı bırakarak oluşturur bir <xref:System.Activities.Statements.Rethrow> etkinliği ile bir varsayılan **DisplayName** Throw biri. <xref:System.Activities.Activity.DisplayName%2A> Değeri üst bilgisinde düzenlenebilir **Rethrow** etkinlik Tasarımcısı veya **DisplayName** özellik kılavuzunda kutusu.

### <a name="the-rethrow-properties"></a>Rethrow özellikleri

Aşağıdaki tabloda <xref:System.Activities.Statements.Rethrow> özelliklerini ve bunların Tasarımcısı'nda nasıl kullanıldığı açıklanmaktadır:

|Özellik Adı|Gerekli|Kullanım|
|-|--------------|-|
|<xref:System.Activities.Activity.DisplayName%2A>|False|İsteğe bağlı kolay adı belirtir <xref:System.Activities.Statements.Rethrow> etkinlik. Rethrow varsayılandır.|

## <a name="see-also"></a>Ayrıca bkz.

- [Koleksiyon](../workflow-designer/collection-activity-designers.md)
- [Throw](../workflow-designer/throw-activity-designer.md)
- [TryCatch](../workflow-designer/trycatch-activity-designer.md)
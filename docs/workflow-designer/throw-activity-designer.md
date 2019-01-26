---
title: İş Akışı Tasarımcısı - Throw etkinlik Tasarımcısı
ms.date: 11/04/2016
ms.topic: reference
ms.prod: visual-studio-dev15
f1_keywords:
- System.Activities.Statements.Throw.UI
ms.assetid: 5e97c947-be39-4a1f-af04-000e2e09528a
author: gewarren
ms.author: gewarren
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 60b7396c8a57b6ddcf9ea48c04a17f070194ccdc
ms.sourcegitcommit: 2193323efc608118e0ce6f6b2ff532f158245d56
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/25/2019
ms.locfileid: "54940524"
---
# <a name="throw-activity-designer"></a>Throw Etkinlik Tasarımcısı

**Throw** etkinlik Tasarımcısı oluşturmak ve yapılandırmak için kullanılan bir <xref:System.Activities.Statements.Throw> etkinlik.

## <a name="the-throw-activity"></a>Throw etkinlik

<xref:System.Activities.Statements.Throw> Etkinlik bir özel durum oluşturur.

### <a name="using-the-throw-activity-designer"></a>Throw etkinlik Tasarımcısı kullanma

Erişim **Throw** etkinlik Tasarımcısı'nda **hata işleme** kategorisi **araç kutusu**.

**Throw** etkinlik Tasarımcısı, gelen sürüklenebilir **araç kutusu** ve etkinlikleri genellikle yerleştirilen her yerde, gibi olarak içinde iş akışı Tasarımcısı yüzeyine açın bırakılan bir <xref:System.Activities.Statements.Sequence>. Bu, oluşturur bir <xref:System.Activities.Statements.Throw> etkinliği ile bir varsayılan **DisplayName** Throw biri. <xref:System.Activities.Activity.DisplayName%2A> Değeri üst bilgisinde düzenlenebilir **Throw** etkinlik Tasarımcısı veya **DisplayName** özellik kılavuzunda kutusu. <xref:System.Activities.Statements.Throw.Exception%2A> Özellik Kılavuzu'nun özellik düzenlenemez.

### <a name="the-throw-properties"></a>Throw özellikleri

Aşağıdaki tabloda <xref:System.Activities.Statements.Throw> özellikleri Tasarımcısı'nda nasıl kullanıldığı açıklanmaktadır.

|Özellik Adı|Gerekli|Kullanım|
|-|--------------|-|
|<xref:System.Activities.Activity.DisplayName%2A>|False|İsteğe bağlı kolay adı belirtir <xref:System.Activities.Statements.Throw> etkinlik. Throw varsayılandır.|
|<xref:System.Activities.Statements.Throw.Exception%2A>|Doğru|Oluşturulacak özel durum. Bu özel durumun öğesinden türetilmelidir <xref:System.Exception>. Özel durumu belirtmek için bir Visual Basic ifadesinin özellik kılavuzunda yazın.|

## <a name="see-also"></a>Ayrıca bkz.

- [Koleksiyon](../workflow-designer/collection-activity-designers.md)
- [Rethrow](../workflow-designer/rethrow-activity-designer.md)
- [Throw Etkinlik Tasarımcısı](../workflow-designer/throw-activity-designer.md)
- [TryCatch](../workflow-designer/trycatch-activity-designer.md)
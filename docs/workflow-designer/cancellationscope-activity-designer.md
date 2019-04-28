---
title: İş Akışı Tasarımcısı - CancellationScope etkinlik Tasarımcısı
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- System.Activities.Statements.CancellationScope.UI
ms.assetid: 2c85d663-b219-4142-9866-7693ffd46379
author: gewarren
ms.author: gewarren
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 43a818be208c7e07ef74a8f35923f3042bb8fad5
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "63009796"
---
# <a name="cancellationscope-activity-designer"></a>CancellationScope Etkinlik Tasarımcısı

**CancellationScope** etkinlik Tasarımcısı oluşturmak ve yapılandırmak için kullanılan bir <xref:System.Activities.Statements.CancellationScope> etkinlik.

## <a name="the-cancellationscope-activity"></a>CancellationScope etkinlik

<xref:System.Activities.Statements.CancellationScope> Etkinlik, Etkinlik yürütme ve iptal etme mantığı Bu etkinliğin belirtmenize olanak sağlar.

### <a name="using-the-cancellationscope-activity-designer"></a>CancellationScope etkinlik Tasarımcısı kullanma

**CancellationScope** etkinlik Tasarımcısı bulunabilir **işlem** kategorisi **araç kutusu**. Açmak için **araç kutusu**seçin **araç kutusu** iş akışı Tasarımcısı için sekmesinde. Alternatif olarak, seçin **araç kutusu** gelen **görünümü** tuşuna basın veya menü **Ctrl**+**Alt** + **X**.

**CancellationScope** etkinlik Tasarımcısı, gelen sürüklenebilir **araç kutusu** ve etkinlikleri yerleştirilir her yerde, örneğin olarak içinde iş akışı Tasarımcısı yüzeyine açın bırakılan bir <xref:System.Activities.Statements.Sequence>. Bırakarak **CancellationScope** etkinlik Tasarımcısı oluşturur bir <xref:System.Activities.Statements.CancellationScope> etkinliği ile bir varsayılan <xref:System.Activities.Activity.DisplayName%2A> CancellationScope biri. Düzen <xref:System.Activities.Activity.DisplayName%2A> üstbilgisinin değerini **CancellationScope** etkinlik Tasarımcısı. İçinde de düzenleyebilirsiniz **DisplayName** özellik kılavuzunda kutusu.

### <a name="the-cancellationscope-properties"></a>CancellationScope özellikleri

Aşağıdaki tabloda <xref:System.Activities.Statements.CancellationScope> özellikleri Tasarımcısı'nda nasıl kullanıldığı açıklanmaktadır. <xref:System.Activities.Activity.DisplayName%2A> Özelliği özellik kılavuzunda düzenlenebilir ancak iş akışı Tasarımcısı yüzeyine diğer özellikleri düzenlenmesi gerekir.

|Özellik Adı|Gerekli|Kullanım|
|-|--------------|-|
|<xref:System.Activities.Activity.DisplayName%2A>|False|İsteğe bağlı kolay adı <xref:System.Activities.Statements.CancellationScope> etkinlik. CancellationScope varsayılandır. Ancak <xref:System.Activities.Activity.DisplayName%2A> değeri kesinlikle gerekli değil, kullanmak için en iyi bir uygulamadır.|
|<xref:System.Activities.Statements.CancellationScope.Body%2A>|Doğru|Hangi iptal için sağlanan mantıksal etkinlik belirtir. Eklemek için <xref:System.Activities.Statements.CancellationScope.Body%2A> etkinlik, açılan bir etkinlikten **araç kutusu** içine **gövdesi** kutusuna **CancellationScope** etkinlik Tasarımcısı. İpucu metnini "Etkinliği buraya bırakın" ekleyin.|
|<xref:System.Activities.Statements.CancellationScope.CancellationHandler%2A>|Doğru|İptal durumunda ise çalıştırılan etkinlik belirtir. Eklenecek <xref:System.Activities.Statements.CancellationScope.CancellationHandler%2A> etkinlik, açılan bir etkinlikten **araç kutusu** içine **CancellationHandler** kutusuna **CancellationScope** etkinlik Tasarımcısı. İpucu metnini "Etkinliği buraya bırakın" ekleyin.|

## <a name="see-also"></a>Ayrıca bkz.

- [İşlem](../workflow-designer/transaction-activity-designers.md)
- [CompensableActivity](../workflow-designer/compensableactivity-activity-designer.md)
- [Compensate](../workflow-designer/compensate-activity-designer.md)
- [Confirm](../workflow-designer/confirm-activity-designer.md)
- [TransactionScope](../workflow-designer/transactionscope-activity-designer.md)
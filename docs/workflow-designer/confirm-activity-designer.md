---
title: İş Akışı Tasarımcısı - onaylayın etkinlik Tasarımcısı
ms.date: 11/04/2016
ms.topic: reference
ms.prod: visual-studio-dev15
f1_keywords:
- System.Activities.Statements.Confirm.UI
ms.assetid: c753b67b-b0e7-462a-bb4e-ba8db04a078d
author: gewarren
ms.author: gewarren
manager: douge
ms.workload:
- multiple
ms.openlocfilehash: 34f59bc8ad3040c6077d5feeb4f725f367b8dcdc
ms.sourcegitcommit: 37fb7075b0a65d2add3b137a5230767aa3266c74
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/02/2019
ms.locfileid: "53956483"
---
# <a name="confirm-activity-designer"></a>Confirm Etkinlik Tasarımcısı

**Onayla** etkinlik Tasarımcısı oluşturmak ve yapılandırmak için kullanılan bir <xref:System.Activities.Statements.Confirm> etkinlik.

## <a name="the-confirm-activity"></a>Etkinlik onaylayın
 <xref:System.Activities.Statements.Confirm> Etkinlik açıkça çağıran <xref:System.Activities.Statements.CompensableActivity.ConfirmationHandler%2A> bulunan bir etkinlik için bir <xref:System.Activities.Statements.CompensableActivity>. Varsa <xref:System.Activities.Statements.Confirm> etkinliği içinde kullanılmaz <xref:System.Activities.Statements.CompensableActivity.CancellationHandler%2A>, <xref:System.Activities.Statements.CompensableActivity.CompensationHandler%2A>, veya <xref:System.Activities.Statements.CompensableActivity.ConfirmationHandler%2A> , bir <xref:System.Activities.Statements.CompensableActivity>, sonra da belirtmeniz gerekir <xref:System.Activities.Statements.Confirm.Target%2A> özelliği.

 <xref:System.Activities.Statements.CompensationToken> Tarafından belirtilen <xref:System.Activities.Statements.Compensate.Target%2A> açıkça onaylayın veya dengelemek için bir yöntem sunan bir <xref:System.Activities.Statements.CompensableActivity> sonra <xref:System.Activities.Statements.CompensableActivity.Body%2A> , <xref:System.Activities.Statements.CompensableActivity> başarıyla tamamlandı.

### <a name="using-the-confirm-activity-designer"></a>Kullanarak Confirm etkinlik Tasarımcısı
 **Onayla** etkinlik Tasarımcısı bulunabilir **işlem** kategorisi **araç kutusu**, hangi erişilen tıklayarak **araç kutusu**iş akışı Tasarımcısı'nın sol tarafındaki sekmesi. Alternatif olarak, seçin **araç kutusu** gelen **görünümü** tuşuna basın veya menü **Ctrl**+**Alt** + **X**.

 **Onayla** etkinlik Tasarımcısı, gelen sürüklenebilir **araç kutusu** ve etkinlikleri genellikle yerleştirilen her yerde, gibi olarak içinde iş akışı Tasarımcısı yüzeyine açın bırakılan bir <xref:System.Activities.Statements.Sequence>. Bu oluşturur bir <xref:System.Activities.Statements.Confirm> etkinliği ile bir varsayılan <xref:System.Activities.Activity.DisplayName%2A> , onaylayın. <xref:System.Activities.Activity.DisplayName%2A> Değeri olabilir ya da üstbilgisindeki özelliklerin düzenlenmiş **Onayla** etkinlik Tasarımcısı veya **DisplayName** özellik kılavuzunda kutusu.

### <a name="the-confirm-properties"></a>Özellikleri onaylayın
 Aşağıdaki tabloda <xref:System.Activities.Statements.Confirm> özellikleri Tasarımcısı'nda nasıl kullanıldığı açıklanmaktadır. <xref:System.Activities.Activity.DisplayName%2A> Özelliği, özellik kılavuzu veya iş akışı Tasarımcısı yüzeyine düzenlenebilir ancak <xref:System.Activities.Statements.Confirm.Target%2A> özellik kılavuzunda özellik düzenlenemez.

|Özellik Adı|Gerekli|Kullanım|
|-|--------------|-|
|<xref:System.Activities.Activity.DisplayName%2A>|False|İsteğe bağlı kolay adı belirtir <xref:System.Activities.Statements.CancellationScope> etkinlik. Onayla varsayılandır.|
|<xref:System.Activities.Statements.Confirm.Target%2A>|Doğru|Belirtir <xref:System.Activities.InArgument%601> içeren <xref:System.Activities.Statements.CompensationToken> bu <xref:System.Activities.Statements.Confirm> etkinlik.|

## <a name="see-also"></a>Ayrıca bkz.

- [İşlem](../workflow-designer/transaction-activity-designers.md)
- [CancellationScope](../workflow-designer/cancellationscope-activity-designer.md)
- [CompensableActivity](../workflow-designer/compensableactivity-activity-designer.md)
- [Compensate](../workflow-designer/compensate-activity-designer.md)
- [TransactionScope](../workflow-designer/transactionscope-activity-designer.md)
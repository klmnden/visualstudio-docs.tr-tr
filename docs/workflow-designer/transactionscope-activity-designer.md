---
title: İş Akışı Tasarımcısı - TransactionScope etkinlik Tasarımcısı
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- System.Activities.Statements.TransactionScope.UI
ms.assetid: 8d7ebfc6-7478-4888-b3b0-b14f296096af
author: gewarren
ms.author: gewarren
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: e84312518c19ef2a041091c5e2439dd7fb312c69
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62433974"
---
# <a name="transactionscope-activity-designer"></a>TransactionScope Etkinlik Tasarımcısı

**TransactionScope** etkinlik Tasarımcısı oluşturmak ve yapılandırmak için kullanılan bir <xref:System.Activities.Statements.TransactionScope> etkinlik.

## <a name="the-transactionscope-activity"></a>TransactionScope etkinlik

<xref:System.Activities.Statements.TransactionScope> Etkinliği tek bir işlemde içerilen bir etkinliği yürütür. Ne zaman işlem yürütmeleri <xref:System.Activities.Statements.TransactionScope.Body%2A> etkinliği ve diğer tüm katılımcıları işlem başarıyla tamamlandı.

### <a name="using-the-transactionscope-activity-designer"></a>TransactionScope etkinlik Tasarımcısı kullanma

Erişim **TransactionScope** etkinlik Tasarımcısı'nda **işlem** kategorisi **araç kutusu**. **TransactionScope** etkinlik Tasarımcısı, gelen sürüklenebilir **araç kutusu** ve etkinlikleri genellikle yerleştirilen her yerde, gibi olarak içinde iş akışı Tasarımcısı yüzeyine açın bırakılan bir <xref:System.Activities.Statements.Sequence>. Bu, oluşturur bir <xref:System.Activities.Statements.TransactionScope> etkinliği ile bir varsayılan <xref:System.Activities.Activity.DisplayName%2A> TransactionScope biri. <xref:System.Activities.Activity.DisplayName%2A> Değeri üst bilgisinde düzenlenebilir **TransactionScope** etkinlik Tasarımcısı veya **DisplayName** özellik kılavuzunda kutusu.

### <a name="the-transactionscope-properties"></a>TransactionScope özellikleri

Aşağıdaki tabloda <xref:System.Activities.Statements.TransactionScope> özellikleri Tasarımcısı'nda nasıl kullanıldığı açıklanmaktadır. <xref:System.Activities.Activity.DisplayName%2A> Ve <xref:System.Activities.Statements.TransactionScope.Body%2A> özelliklerinin iş akışı Tasarımcısı yüzeyine düzenlenebilir. Ancak, özellik Kılavuzu'nun diğer özellikleri düzenlenmesi gerekir.

|Özellik Adı|Gerekli|Kullanım|
|-|--------------|-|
|<xref:System.Activities.Activity.DisplayName%2A>|False|İsteğe bağlı kolay adı <xref:System.Activities.Statements.TransactionScope> etkinlik. TransactionScope varsayılandır. Ancak <xref:System.Activities.Activity.DisplayName%2A> değeri kesinlikle gerekli değil, kullanmak için en iyi bir uygulamadır.|
|<xref:System.Activities.Statements.TransactionScope.Body%2A>|Doğru|Tek bir işlem içinde çalıştırmak için etkinlik belirtir. Eklemek için <xref:System.Activities.Statements.TransactionScope.Body%2A> etkinlik, açılan bir etkinlikten **araç kutusu** içine **gövdesi** kutusuna **TransactionScope** ipucu metnini "bırakma etkinlik ile etkinlik Tasarımcısı Burada".|
|<xref:System.Activities.Statements.TransactionScope.IsolationLevel%2A>|Doğru|Belirtir <xref:System.Transactions.IsolationLevel> bu <xref:System.Activities.Statements.TransactionScope>.|
|<xref:System.Activities.Statements.TransactionScope.Timeout%2A>|False|(00:00: saat: dakika: saniye gösteren 00 biçimlendirilmiş) zaman aralığını belirtir. işlemin tamamlanması sahip. Varsayılan değer 1 dakikadır (00: 01:00).|
|[System.Activities.Statements.TransactionScope.AbortInstanceOnTransactionFailure](https://msdn.microsoft.com/library/system.activities.statements.transactionscope.abortinstanceontransactionfailure.aspx)|Doğru|İşlem durdurur, iş akışı durduruldu olup olmadığını belirten değeri belirtir.|

## <a name="see-also"></a>Ayrıca bkz.

- [İşlem](../workflow-designer/transaction-activity-designers.md)
- [TerminateWorkflow](../workflow-designer/terminateworkflow-activity-designer.md)
- [CompensableActivity](../workflow-designer/compensableactivity-activity-designer.md)
- [Compensate](../workflow-designer/compensate-activity-designer.md)
- [Confirm](../workflow-designer/confirm-activity-designer.md)
---
title: Confirm etkinlik Tasarımcısı | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-workflow-designer
ms.topic: reference
f1_keywords:
- System.Activities.Statements.Confirm.UI
ms.assetid: c753b67b-b0e7-462a-bb4e-ba8db04a078d
caps.latest.revision: 5
author: gewarren
ms.author: gewarren
manager: jillfra
ms.openlocfilehash: 29635044eb4cca558d631ab959b1b4f5480dbdbe
ms.sourcegitcommit: 8b538eea125241e9d6d8b7297b72a66faa9a4a47
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54782589"
---
# <a name="confirm-activity-designer"></a>Confirm Etkinlik Tasarımcısı
**Onayla** etkinlik Tasarımcısı oluşturmak ve yapılandırmak için kullanılan bir <xref:System.Activities.Statements.Confirm> etkinlik.  
  
## <a name="the-confirm-activity"></a>Etkinlik onaylayın  
 <xref:System.Activities.Statements.Confirm> Etkinlik açıkça çağıran <xref:System.Activities.Statements.CompensableActivity.ConfirmationHandler%2A> bulunan bir etkinlik için bir <xref:System.Activities.Statements.CompensableActivity>. Varsa <xref:System.Activities.Statements.Confirm> etkinliği içinde kullanılmaz <xref:System.Activities.Statements.CompensableActivity.CancellationHandler%2A>, <xref:System.Activities.Statements.CompensableActivity.CompensationHandler%2A>, veya <xref:System.Activities.Statements.CompensableActivity.ConfirmationHandler%2A> , bir <xref:System.Activities.Statements.CompensableActivity>, sonra da belirtmeniz gerekir <xref:System.Activities.Statements.Confirm.Target%2A> özelliği.  
  
 <xref:System.Activities.Statements.CompensationToken> Tarafından belirtilen <xref:System.Activities.Statements.Compensate.Target%2A> açıkça onaylayın veya dengelemek için bir yöntem sunan bir <xref:System.Activities.Statements.CompensableActivity> sonra <xref:System.Activities.Statements.CompensableActivity.Body%2A> , <xref:System.Activities.Statements.CompensableActivity> başarıyla tamamlandı.  
  
### <a name="using-the-confirm-activity-designer"></a>Kullanarak Confirm etkinlik Tasarımcısı  
 **Onayla** etkinlik Tasarımcısı bulunabilir **işlem** kategorisi **araç kutusu**, hangi erişilen tıklayarak **araç kutusu**sol tarafındaki sekmesinde [!INCLUDE[wfd2](../includes/wfd2-md.md)] (Alternatif olarak, seçin **araç** gelen **görünümü** menüsünden veya CTRL + ALT + X.)  
  
 **Onayla** etkinlik Tasarımcısı, gelen sürüklenebilir **araç kutusu** ve oturum bırakılan [!INCLUDE[wfd2](../includes/wfd2-md.md)] yüzey yerde etkinlikleri genellikle yerleştirilir, örneğin olarak içinde bir <xref:System.Activities.Statements.Sequence>. Bu oluşturur bir <xref:System.Activities.Statements.Confirm> etkinliği ile bir varsayılan <xref:System.Activities.Activity.DisplayName%2A> , onaylayın. <xref:System.Activities.Activity.DisplayName%2A> Değeri olabilir ya da üstbilgisindeki özelliklerin düzenlenmiş **Onayla** etkinlik Tasarımcısı veya **DisplayName** özellik kılavuzunda kutusu.  
  
### <a name="the-confirm-properties"></a>Özellikleri onaylayın  
 Aşağıdaki tabloda <xref:System.Activities.Statements.Confirm> özellikleri Tasarımcısı'nda nasıl kullanıldığı açıklanmaktadır. <xref:System.Activities.Activity.DisplayName%2A> Özelliği, özellik kılavuzu veya Cihazınızda düzenlenebilir [!INCLUDE[wfd2](../includes/wfd2-md.md)] surface, ancak <xref:System.Activities.Statements.Confirm.Target%2A> özellik kılavuzunda özellik düzenlenemez.  
  
|Özellik Adı|Gerekli|Kullanım|  
|-------------------|--------------|-----------|  
|<xref:System.Activities.Activity.DisplayName%2A>|False|İsteğe bağlı kolay adı belirtir <xref:System.Activities.Statements.CancellationScope> etkinlik. Onayla varsayılandır.|  
|<xref:System.Activities.Statements.Confirm.Target%2A>|Doğru|Belirtir <xref:System.Activities.InArgument%601> içeren <xref:System.Activities.Statements.CompensationToken> bu <xref:System.Activities.Statements.Confirm> etkinlik.|  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [İşlem](../workflow-designer/transaction-activity-designers.md)   
 [CancellationScope](../workflow-designer/cancellationscope-activity-designer.md)   
 [CompensableActivity](../workflow-designer/compensableactivity-activity-designer.md)   
 [Telafi](../workflow-designer/compensate-activity-designer.md)   
 [TransactionScope](../workflow-designer/transactionscope-activity-designer.md)
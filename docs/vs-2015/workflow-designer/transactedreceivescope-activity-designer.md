---
title: TransactedReceiveScope etkinlik Tasarımcısı | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-workflow-designer
ms.topic: reference
f1_keywords:
- System.ServiceModel.Activities.TransactedReceiveScope.UI
ms.assetid: 7ca93aad-4e83-4d81-90f4-998ee114d9b6
caps.latest.revision: 4
author: gewarren
ms.author: gewarren
manager: jillfra
ms.openlocfilehash: f4864a19cf48b468abed90e120e4924237653cec
ms.sourcegitcommit: 8b538eea125241e9d6d8b7297b72a66faa9a4a47
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54799331"
---
# <a name="transactedreceivescope-activity-designer"></a>TransactedReceiveScope Etkinlik Tasarımcısı
**TransactedReceiveScope** Tasarımcısı oluşturmak ve yapılandırmak için kullanılan bir <xref:System.ServiceModel.Activities.TransactedReceiveScope> etkinlik.  
  
## <a name="the-transactedreceivescope-activity"></a>TransactedReceiveScope etkinlik  
 <xref:System.ServiceModel.Activities.TransactedReceiveScope> Etkinliğini bir iş akışı veya dağıtıcı tarafından oluşturulan sunucu işlemleri harekete akış olanak sağlar.  
  
### <a name="using-the-transactedreceivescope-activity-designer"></a>TransactedReceiveScope etkinlik Tasarımcısı kullanma  
 **TransactedReceiveScope** etkinlik Tasarımcısı bulunabilir **Mesajlaşma** kategorisi **araç kutusu**, hangi erişilen tıklayarak **araç kutusu**  sekmesinde [!INCLUDE[wfd2](../includes/wfd2-md.md)] (Alternatif olarak, seçin **araç** gelen **görünümü** menüsünü veya CTRL + ALT + X.)  
  
 **TransactedReceiveScope** etkinlik Tasarımcısı, gelen sürüklenebilir **araç kutusu** ve oturum bırakılan [!INCLUDE[wfd2](../includes/wfd2-md.md)] yüzey yerde etkinlikleri genellikle yerleştirilir. Bu, oluşturur bir <xref:System.ServiceModel.Activities.TransactedReceiveScope> etkinliği ile bir varsayılan **DisplayName** TransactedReceiveScope kullanımı. <xref:System.Activities.Activity.DisplayName%2A> Üst bilgisinde düzenlenebilir **TransactedReceiveScope** etkinlik Tasarımcısı veya **DisplayName** özellik kılavuzunda kutusu.  
  
 **TransactedReceiveScope** Tasarımcısı içerir **istek** ve **gövdesi** kutuları. Bu yapılandırma için kullanılan <xref:System.ServiceModel.Activities.TransactedReceiveScope.Request%2A> belirten özellik bir <xref:System.ServiceModel.Activities.Receive> etkinlik ve <xref:System.ServiceModel.Activities.TransactedReceiveScope.Body%2A> başka belirten özellik <xref:System.Activities.Activity>. <xref:System.ServiceModel.Activities.TransactedReceiveScope.Request%2A> Bir işlem oluşturur. Daha sonra işlem kapsamı için ortam yapılan <xref:System.ServiceModel.Activities.TransactedReceiveScope.Body%2A> böylece bu işlem içinde bu kapsam içinde herhangi bir etkinliği yürütür.  
  
### <a name="the-transactedreceivescope-properties"></a>TransactedReceiveScope özellikleri  
 Aşağıdaki tabloda <xref:System.ServiceModel.Activities.TransactedReceiveScope> özellikleri Tasarımcısı'nda nasıl kullanıldığı açıklanmaktadır. Bunlar <xref:System.Activities.Activity.DisplayName%2A> özelliği, özellik kılavuzu veya Cihazınızda düzenlenebilir [!INCLUDE[wfd2](../includes/wfd2-md.md)] surface, ama sıklıkla başkalarını gerekir düzenlenmesi tasarım yüzeyinde.  
  
|Özellik Adı|Gerekli|Kullanım|  
|-------------------|--------------|-----------|  
|<xref:System.Activities.Activity.DisplayName%2A>|False|İsteğe bağlı kolay adı <xref:System.ServiceModel.Activities.TransactedReceiveScope> etkinlik. TransactedReceiveScope varsayılandır.<br /><br /> Ancak <xref:System.Activities.Activity.DisplayName%2A> adı kesinlikle gerekli değil, görünen adı kullanmak için en iyi bir uygulamadır.|  
|<xref:System.ServiceModel.Activities.TransactedReceiveScope.Request%2A>|Doğru|Bırakılanlar bir <xref:System.ServiceModel.Activities.Receive> etkinliğini **istek** etkinlik tasarımcısının yüzeyine blok.|  
|<xref:System.ServiceModel.Activities.TransactedReceiveScope.Body%2A>|False|Bırakılanlar bir <xref:System.Activities.Activity> içine **gövdesi** etkinlik tasarımcısının yüzeyine blok.|  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [CorrelationScope](../workflow-designer/correlationscope-activity-designer.md)   
 [Initializecorrelation](../workflow-designer/initializecorrelation-activity-designer.md)   
 [Alma](../workflow-designer/receive-activity-designer.md)   
 [ReceiveAndSendReply](../workflow-designer/receiveandsendreply-template-designer.md)   
 [Gönder](../workflow-designer/send-activity-designer.md)   
 [SendAndReceiveReply](../workflow-designer/sendandreceivereply-template-designer.md)
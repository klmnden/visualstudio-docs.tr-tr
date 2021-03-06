---
title: Mesajlaşma etkinlik tasarımcıları | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-workflow-designer
ms.topic: reference
ms.assetid: 897e63cf-a42f-4edd-876f-c4ccfffaf6d6
caps.latest.revision: 7
author: gewarren
ms.author: gewarren
manager: jillfra
ms.openlocfilehash: 250b213fc3bc54d67f55d41c5eb3aba7e3488cd4
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62420229"
---
# <a name="messaging-activity-designers"></a>Mesajlaşma Etkinlik Tasarımcıları
Mesajlaşma etkinlik tasarımcıları oluşturmak ve göndermek ve almak Mesajlaşma etkinlikleri yapılandırmak için kullanılan [!INCLUDE[indigo1](../includes/indigo1-md.md)] iletileri içinden bir [!INCLUDE[wf](../includes/wf-md.md)] uygulama. [!INCLUDE[netfx40_long](../includes/netfx40-long-md.md)] Beş Mesajlaşma etkinlikleri tanıtır ve [!INCLUDE[wfd1](../includes/wfd1-md.md)] bir iş akışı içinde Mesajlaşma yönetmenizi sağlayan iki yeni Şablon tasarımcıları sağlar. Bu bölümde yer alan ve aşağıdaki tabloda listelenen konular Kılavuzu nasıl kullanılacağı hakkında sağlamaya [!INCLUDE[wfd2](../includes/wfd2-md.md)] etkinliği ve Şablon tasarımcıları.  
  
## <a name="in-this-section"></a>Bu Bölümde  
  
|İleti etkinliği|Açıklama|  
|----------------------|-----------------|  
|[CorrelationScope](../workflow-designer/correlationscope-activity-designer.md)|Oluşturur ve yapılandırır bir <xref:System.ServiceModel.Activities.CorrelationScope> etkinliklerle Mesajlaşma alt örtük yönetimini sağlayan etkinlik bir <xref:System.ServiceModel.Activities.CorrelationHandle> nesne.|  
|[InitializeCorrelation](../workflow-designer/initializecorrelation-activity-designer.md)|Oluşturur ve yapılandırır bir <xref:System.ServiceModel.Activities.InitializeCorrelation> ınicializace korelace gönderme veya bir ileti almak için kullanılan etkinlik.|  
|[Receive](../workflow-designer/receive-activity-designer.md)|Oluşturur ve yapılandırır bir <xref:System.ServiceModel.Activities.Receive> etkinliği bir hizmetten bir ileti alır.|  
|[ReceiveAndSendReply](../workflow-designer/receiveandsendreply-template-designer.md)|Önceden yapılandırılmış bir çift oluşturur <xref:System.ServiceModel.Activities.Send> ve <xref:System.ServiceModel.Activities.ReceiveReply> içindeki etkinlikleri bir <xref:System.Activities.Statements.Sequence> etkinlik.|  
|[Send](../workflow-designer/send-activity-designer.md)|Oluşturur ve yapılandırır bir <xref:System.ServiceModel.Activities.Send> etkinliği bir hizmete ileti gönderir.|  
|[SendAndReceiveReply](../workflow-designer/sendandreceivereply-template-designer.md)|Önceden yapılandırılmış bir çift oluşturur <xref:System.ServiceModel.Activities.Receive> ve <xref:System.ServiceModel.Activities.SendReply> içindeki etkinlikleri bir <xref:System.Activities.Statements.Sequence> etkinlik.|  
|[TransactedReceiveScope](../workflow-designer/transactedreceivescope-activity-designer.md)|Oluşturur ve yapılandırır bir <xref:System.ServiceModel.Activities.TransactedReceiveScope> işlemleri bir iş akışını sağlayan etkinlik.|  
  
## <a name="reference"></a>Başvuru  
 <xref:System.Activities.Activity>  
  
 <xref:System.ServiceModel.Activities.CorrelationScope>  
  
 <xref:System.ServiceModel.Activities.Receive>  
  
 <xref:System.ServiceModel.Activities.Send>  
  
 <xref:System.ServiceModel.Activities.ReceiveReply>  
  
 <xref:System.ServiceModel.Activities.SendReply>  
  
 <xref:System.ServiceModel.Activities.TransactedReceiveScope>  
  
## <a name="related-sections"></a>İlgili Bölümler  
 Etkinlik tasarımcıları diğer türleri için aşağıdaki konulara bakın.  
  
 [Denetim Akışı](../workflow-designer/control-flow-activity-designers.md)  
  
 [Etkinlik Tasarımcılarını kullanma](../workflow-designer/using-the-activity-designers.md)  
  
 [Akış Çizelgesi](../workflow-designer/flowchart-activity-designers.md)  
  
 [Çalışma Zamanı](../workflow-designer/runtime-activity-designers.md)  
  
 [Temel Türler](../workflow-designer/primitives-activity-designers.md)  
  
 [İşlem](../workflow-designer/transaction-activity-designers.md)  
  
 [Koleksiyon](../workflow-designer/collection-activity-designers.md)  
  
 [Hata İşleme](../workflow-designer/error-handling-activity-designers.md)  
  
## <a name="external-resources"></a>Dış Kaynaklar  
 [Etkinlik Tasarımcılarını kullanma](../workflow-designer/using-the-activity-designers.md)
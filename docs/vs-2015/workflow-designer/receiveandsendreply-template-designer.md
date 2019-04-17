---
title: ReceiveAndSendReply şablon Tasarımcısı | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-workflow-designer
ms.topic: reference
f1_keywords:
- System.ServiceModel.Activities.ReceiveAndSendReply.UI
- System.ServiceModel.Activities.SendReply.UI
ms.assetid: d1d9a058-df7e-48f5-a2e7-3caeeba7eaa6
caps.latest.revision: 5
author: gewarren
ms.author: gewarren
manager: jillfra
ms.openlocfilehash: 74b3559849fe69da998f59c3caa6e38ff23b238b
ms.sourcegitcommit: 53aa5a413717a1b62ca56a5983b6a50f7f0663b3
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/17/2019
ms.locfileid: "59657525"
---
# <a name="receiveandsendreply-template-designer"></a>ReceiveAndSendReply Şablon Tasarımcısı
**ReceiveAndSendReply** şablon çifti oluşturmak için kullanılan önceden yapılandırılmış <xref:System.ServiceModel.Activities.Receive> ve <xref:System.ServiceModel.Activities.SendReply> içindeki etkinlikleri bir <xref:System.Activities.Statements.Sequence> istek/yanıt iletisi exchange bir parçası olarak bağıntılı olan etkinliği sunucuda deseni.  

## <a name="the-receiveandsendreply-template"></a>ReceiveAndSendReply şablon  
 Ekleme **ReceiveAndSendReply** şablon oluşturma yanı sıra üç şeyi yapar <xref:System.ServiceModel.Activities.Receive> ve <xref:System.ServiceModel.Activities.SendReply> etkinliklerle bir <xref:System.Activities.Statements.Sequence> etkinlik:  

1.  Yapılandırır <xref:System.ServiceModel.Activities.Receive.OperationName%2A>, <xref:System.ServiceModel.Activities.Receive.ServiceContractName%2A> özelliklerini <xref:System.ServiceModel.Activities.Receive> etkinlik.  

2.  Bağlar <xref:System.ServiceModel.Activities.SendReply.Request%2A> özelliği <xref:System.ServiceModel.Activities.Receive> etkinliğini <xref:System.ServiceModel.Activities.Send> etkinlik.  

3.  Oluşturur bir <xref:System.ServiceModel.Activities.CorrelationHandle> üst etkinliği bir değişken olarak.  

### <a name="using-the-receiveandsendreply-template-designer"></a>Kullanma ReceiveAndSendReply şablon Tasarımcısı  
 **ReceiveAndSendReply** etkinlik Tasarımcısı bulunabilir **Mesajlaşma** kategorisi **araç kutusu**, hangi erişilen tıklayarak **araç kutusu**  sekmesinde [!INCLUDE[wfd2](../includes/wfd2-md.md)] (Alternatif olarak, seçin **araç** gelen **görünümü** menüsünü veya CTRL + ALT + X.)  

 **ReceiveAndSendReply** etkinlik Tasarımcısı, gelen sürüklenebilir **araç kutusu** ve oturum bırakılan [!INCLUDE[wfd2](../includes/wfd2-md.md)] yüzey yerde etkinlikleri genellikle yerleştirilir. Bu, oluşturur bir <xref:System.ServiceModel.Activities.Receive> ile yapılandırılmış etkinlik **Gönder** etkinlik Tasarımcısı ve ilişkili bir <xref:System.ServiceModel.Activities.SendReply> SendReplyToReceive tasarımcı ile yapılandırılabilir.  

 [!INCLUDE[crabout](../includes/crabout-md.md)] kullanarak **alma** yapılandırmak için tasarımcı <xref:System.ServiceModel.Activities.Receive> etkinliğine bakın [alma](../workflow-designer/receive-activity-designer.md) konu.  

 [!INCLUDE[crabout](../includes/crabout-md.md)] kullanarak **SendReplyToReceive** yapılandırmak için tasarımcı <xref:System.ServiceModel.Activities.SendReply> etkinlik, aşağıdaki bölüme bakın.  

### <a name="properties-of-sendreply"></a>SendReply özellikleri  
 Aşağıdaki tabloda <xref:System.ServiceModel.Activities.SendReply> özellikleri Tasarımcısı'nda nasıl kullanıldığı açıklanmaktadır. Bu özellikleri Özellikler Kılavuzu ' düzenlenebilir ve bazı şirket düzenlenebilir [!INCLUDE[wfd2](../includes/wfd2-md.md)] Tasarımcı yüzeyine bırakın.  

|                               Özellik Adı                                | Gerekli |                                                                                                                                                                                                                                                                                                                                                      Kullanım                                                                                                                                                                                                                                                                                                                                                       |
|----------------------------------------------------------------------------|----------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|              <xref:System.Activities.Activity.DisplayName%2A>              |  False   |                                                                                                                                                                                            İsteğe bağlı kolay adı <xref:System.ServiceModel.Activities.SendReply> etkinlik. SendReplyToReceive varsayılandır.<br /><br /> Ancak kolay için varsayılan olmayan bir değeri kullanımını <xref:System.Activities.Activity.DisplayName%2A> kati şekilde gerekli değil gibi bir değer kullanmak için en iyi bir uygulamadır.                                                                                                                                                                                             |
|         <xref:System.ServiceModel.Activities.SendReply.Request%2A>         |   Doğru   | Başvuru <xref:System.ServiceModel.Activities.Receive> etkinlik ile eşleştirilmiş <xref:System.ServiceModel.Activities.SendReply> etkinlik. Bu özellik olmamalıdır **null**. <xref:System.ServiceModel.Activities.Receive> ve <xref:System.ServiceModel.Activities.SendReply> etkinlikler birlikte sunucu üzerinde bir istek/yanıt Mesajlaşma modeli model için kullanılır. Bu özellik belirten <xref:System.ServiceModel.Activities.Send> etkinlik eşleştirilmiştir. Tasarımcıda için otomatik olarak bağlı olduğundan bu özellik düzenlenemiyor <xref:System.ServiceModel.Activities.Send> oluşturduğunuz etkinlik <xref:System.ServiceModel.Activities.SendReply> etkinlik. |
|         <xref:System.ServiceModel.Activities.SendReply.Content%2A>         |  False   |                       İleti veya parametre içeriği almak için belirtir. Ya da olabilir bir <xref:System.ServiceModel.Activities.ReceiveMessageContent> etkinlik veya <xref:System.ServiceModel.Activities.ReceiveParametersContent> etkinlik. Yanındaki üç nokta düğmesine tıklayarak bu özellik düzenleme **içerik** özellik kılavuzu veya tıklayarak alanındaki **tanımla...** yanında düğmesini **içerik** üzerinde etiket **alma** etkinlik Tasarımcı yüzeyine bırakın. Her ikisini de görüntüle **içerik tanımı** iletişim. [!INCLUDE[crabout](../includes/crabout-md.md)] Bu kutuyu kullanmak üzere nasıl [içerik tanımı iletişim kutusunun](../workflow-designer/content-definition-dialog-box.md) konu.                       |
| <xref:System.ServiceModel.Activities.SendReply.CorrelationInitializers%2A> |  False   |            Koleksiyonunu belirtir <xref:System.ServiceModel.Activities.CorrelationInitializer> birden çok başlatmak nesneleri <xref:System.ServiceModel.Activities.CorrelationHandle> bu yapılandırma nesneleri <xref:System.ServiceModel.Activities.Receive> etkinlik iş akışı içinde. Yanındaki üç nokta düğmesini tıklayın <xref:System.ServiceModel.Activities.SendReply.CorrelationInitializers%2A> özelliği açmak için özellikler kılavuzundaki **bağıntı başlatıcılar Ekle** iletişim kutusu. [!INCLUDE[crabout](../includes/crabout-md.md)] Bu kutuyu bkz [Correlationınitializer iletişim kutusunu](../workflow-designer/add-correlationinitializers-dialog-box.md) konu.            |
|         <xref:System.ServiceModel.Activities.SendReply.Action%2A>          |  False   |                                                                                                                                                                                                                                              İletinin eylem üstbilgisini belirtir. Açıkça ayarlanmazsa, değeri varsayılan olarak:<br /><br /> <strong>https://tempuri.org/{service ad alanı sözleşme} / {hizmet sözleşmesi adı} / {işlem adı}</strong>                                                                                                                                                                                                                                              |
|    <xref:System.ServiceModel.Activities.SendReply.PersistBeforeSend%2A>    |  False   |                                                                                                                                                                                                                                                                                          Yanıt iletisi gönderilmeden önce iş akışı örneği kalıcı olup olmadığını belirtir. Varsayılan değer **false**.                                                                                                                                                                                                                                                                                           |

## <a name="see-also"></a>Ayrıca Bkz.  
 [CorrelationScope](../workflow-designer/correlationscope-activity-designer.md)   
 [Initializecorrelation](../workflow-designer/initializecorrelation-activity-designer.md)   
 [Alma](../workflow-designer/receive-activity-designer.md)   
 [Gönder](../workflow-designer/send-activity-designer.md)   
 [SendAndReceiveReply](../workflow-designer/sendandreceivereply-template-designer.md)   
 [TransactedReceiveScope](../workflow-designer/transactedreceivescope-activity-designer.md)
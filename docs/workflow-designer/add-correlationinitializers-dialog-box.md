---
title: İş Akışı Tasarımcısı - Correlationınitializer iletişim kutusu Ekle
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- AddCorrelationInitializers.UI
ms.assetid: c0517467-d54a-4ee6-aef0-c19b96b6f395
author: gewarren
ms.author: gewarren
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 21c030295d325ea1ee4d546356f8cda5ef6ffd3f
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62946657"
---
# <a name="add-correlationinitializers-dialog-box"></a>CorrelationInitializer Ekle İletişim Kutusu

**Bağıntı başlatıcılar Ekle** iletişim kutusunda iş akışı Tasarımcısı'nda yapılandırmak için kullanılan **Correlationınitializer** özelliklerini <xref:System.ServiceModel.Activities.Send>, <xref:System.ServiceModel.Activities.Receive>, <xref:System.ServiceModel.Activities.SendReply>, ve <xref:System.ServiceModel.Activities.ReceiveReply> etkinlikler. Bu kutuyu kullanan etkinlik tasarımcıları hakkında daha fazla bilgi için bkz. [Gönder](../workflow-designer/send-activity-designer.md), [alma](../workflow-designer/receive-activity-designer.md), [ReceiveAndSendReply](../workflow-designer/receiveandsendreply-template-designer.md), ve [SendAndReceiveReply ](../workflow-designer/sendandreceivereply-template-designer.md) konuları.

Bu iletişim kutusu ile belirtilen koleksiyondaki bağıntı başlatıcılar Mesajlaşma etkinlikler arasında aşağıdaki bağıntılar başlatabilirsiniz:

- Sorgu tabanlı
- bağlam
- geri çağırma bağlamı
- İstek-yanıt

Aşağıdaki tabloda kullanıcı arabirimi (UI) öğelerini açıklar **bağıntı başlatıcılar Ekle** iletişim kutusunda:

|Arabirim Öğesi|Açıklama|
|-|-----------------|
|**Başlatıcı Ekle**|Tıklayın **Ekle başlatma** kutusunu ek bir başlatıcı koleksiyona ekleyin.|
|**Typ korelace**|Bağıntı başlatıcı türünü belirtir. Aralarından seçim yapabileceğiniz dört tür vardır:<br /><br /> 1. Belirtmek için bir geri çağırma bağıntı başlatıcı bir <xref:System.ServiceModel.Activities.CallbackCorrelationInitializer>.<br />2. Belirtmek için bir bağlam bağıntı başlatıcı bir <xref:System.ServiceModel.Activities.CorrelationInitializer>.<br />3. Belirtmek için bir istek-yanıt bağıntısı Başlatıcı bir <xref:System.ServiceModel.Activities.RequestReplyCorrelationInitializer>.<br />4. Belirtmek için bir sorgu bağıntı başlatıcı bir <xref:System.ServiceModel.Activities.QueryCorrelationInitializer>.<br /><br /> Düzenlenecek **CorrelationType**<br /><br /> 1. Belirli bir satırda için sekmesinde **ekleme Başlatıcı** DataGrid.<br />2. Odağı ayarlamak için **CorrelationTypeComboBox**, basın **Ctrl**+**sekmesini**.<br />3. Açılır kutu için alt + aşağı ok tuşlarına basın **ComboBox** ve düzenleyin.|
|**XPath sorguları**|Gelen ve giden iletilerden bağıntı verileri ayıklamak için kullanılan sorguları içeren bir anahtar/değer çifti. Bu liste yalnızca geçerli kullanıldığında <xref:System.ServiceModel.Activities.QueryCorrelationInitializer> türleri.|

## <a name="to-launch-the-add-correlation-initializers-dialog-box"></a>Bağıntı başlatıcılar Ekle iletişim kutusunu başlatmak için

 **Bağıntı başlatıcılar Ekle** iletişim kutusu tarafından kullanılan **Gönder**, **alma**, **ReceiveAndSendReply**, ve  **SendAndReceiveReply** tasarımcıları. Bunlara erişmek her durumda ve içerir durumda benzer **alma** Tasarımcısı burada yordamı göstermek için kullanılır.

 **Alma** etkinlik Tasarımcısı, gelen sürüklenebilir **araç kutusu** ve etkinlikleri yerleştirilen her yerde iş akışı Tasarımcısı yüzeyine açın. Bırakarak **alma** etkinlik Tasarımcısı oluşturur bir <xref:System.ServiceModel.Activities.Receive> etkinliği ile bir varsayılan <xref:System.Activities.Activity.DisplayName%2A> alma. Seçin **alma** etkinlik Tasarımcısı ve üç nokta düğmesini (koleksiyon) metnin yanında tıklatın **Correlationınitializer** özelliği için özellik kılavuzunda **Ekle Bağıntı başlatıcılar** iletişim kutusu görünür.

## <a name="see-also"></a>Ayrıca bkz.

- [Bağıntıyı Başlat İletişim Kutusu](../workflow-designer/initialize-correlation-dialog-box.md)
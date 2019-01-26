---
title: İş Akışı Tasarımcısı - içerik tanımı iletişim kutusu
ms.date: 11/04/2016
ms.topic: reference
ms.prod: visual-studio-dev15
f1_keywords:
- MessageContent.UI
ms.assetid: 7e4237c3-90a1-4149-bd8a-3643d1dde0df
author: gewarren
ms.author: gewarren
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 49d789e3cbf1a005462e4b23db698bc81c65164a
ms.sourcegitcommit: 2193323efc608118e0ce6f6b2ff532f158245d56
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/25/2019
ms.locfileid: "54999944"
---
# <a name="content-definition-dialog-box"></a>İçerik Tanımı İletişim Kutusu

**İçerik tanımı** iletişim kutusunda iş akışı Tasarımcısı'nda yapılandırmak için kullanılan **içerik** özelliklerini <xref:System.ServiceModel.Activities.Send>, <xref:System.ServiceModel.Activities.Receive>, <xref:System.ServiceModel.Activities.SendReply>, ve <xref:System.ServiceModel.Activities.ReceiveReply> etkinlikler. Bu kutuyu kullanan etkinlik tasarımcıları hakkında daha fazla bilgi için bkz. [Gönder](../workflow-designer/send-activity-designer.md), [alma](../workflow-designer/receive-activity-designer.md), [ReceiveAndSendReply](../workflow-designer/receiveandsendreply-template-designer.md), ve [SendAndReceiveReply ](../workflow-designer/sendandreceivereply-template-designer.md) konuları.

Aşağıdaki tabloda kullanıcı arabirimi (UI) öğelerini açıklar **başlatmak bağıntı** iletişim kutusunda:

|Arabirim Öğesi|Açıklama|
|-|-----------------|
|**İleti**|İleti içeriği belirtir **ileti veri** ifade metin kutusu ve türünü kullanarak **ileti türü** aşağı açılan liste kutusu. Varsayılan olarak, **içerik tanımı** kullanan <xref:System.ServiceModel.Activities.ReceiveMessageContent>, hangi bekliyor bir <xref:System.ServiceModel.Channels.Message> veya sözleşme türü iş akışı hizmet tanımı içinde bir ileti.|
|**Parametreler**|Tıklayın **parametreleri** kullanmak için bir radyo düğmesi <xref:System.ServiceModel.Activities.ReceiveParametersContent>, bir veri anlaşması bekliyor. Veri Kılavuzu Genel koleksiyonu ayarlamak için kullanın <xref:System.Activities.OutArgument> anahtar/değer çiftleri değerleri geçerli iş akışında değişken parametreleri atanır.|

**İçerik tanımı** iletişim kutusu tarafından kullanılan **Gönder**, **alma**, **ReceiveAndSendReply**, ve  **SendAndReceiveReply** tasarımcıları. Her durumda bunları erişme benzer ve alma durum burada yordamı göstermek için kullanılır.

**Alma** etkinlik Tasarımcısı, gelen sürüklenebilir **araç kutusu** ve etkinlikleri genellikle yerleştirilen her yerde iş akışı Tasarımcısı yüzeyine açın. Bu, oluşturur bir <xref:System.ServiceModel.Activities.Receive> etkinliği ile bir varsayılan <xref:System.Activities.Activity.DisplayName%2A> alma. Seçin **alma** etkinlik Tasarımcısı ve üç nokta düğmesini (içerik) metnin yanında tıklatın **içerik** özelliği için özellik kılavuzunda **içerik tanımı**iletişim kutusu görünür.

İçerik içinde belirtilen **ileti** bölümü bir <xref:System.ServiceModel.Activities.ReceiveMessageContent> etkinlik veya içinde **parametre** bölümü bir <xref:System.ServiceModel.Activities.ReceiveParametersContent> etkinlik.

## <a name="see-also"></a>Ayrıca bkz.

- [İş Akışı Tasarımcısı Kullanıcı Arabirimi Yardımı](../workflow-designer/workflow-designer-ui-help.md)
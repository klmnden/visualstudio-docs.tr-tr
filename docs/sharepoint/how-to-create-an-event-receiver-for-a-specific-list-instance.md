---
title: 'Nasıl Yapılır: Belirli bir liste örneği için olay alıcı oluşturma | Microsoft Docs'
ms.date: 02/02/2017
ms.topic: conceptual
dev_langs:
- VB
- CSharp
helpviewer_keywords:
- SharePoint development in Visual Studio, event receivers
- event receivers [SharePoint development in Visual Studio]
author: TerryGLee
ms.author: tglee
manager: douge
ms.workload:
- office
ms.openlocfilehash: a92b86d7e02487ff333fb8517086f9c6221d35ec
ms.sourcegitcommit: 37fb7075b0a65d2add3b137a5230767aa3266c74
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/02/2019
ms.locfileid: "53818868"
---
# <a name="how-to-create-an-event-receiver-for-a-specific-list-instance"></a>Nasıl Yapılır: Belirli bir liste örneği için olay alıcı oluşturma
  Bir liste örneği olay alıcısı, herhangi bir örneğini liste tanımı gerçekleşen olaylara yanıt verir. Olay alıcısı şablonu belirli bir liste örneğini hedefleme etkinleştirmez olsa da, belirli bir liste örneği olaylara yanıt vermek için bir liste tanımı için kapsamlı bir olay alıcısı değiştirebilirsiniz.  
  
 Belirli bir liste örneği, hedeflemek için *Elements.xml* değiştirmek için olay alıcı `ListTemplateId` ile `ListUrl` ve liste örneği URL'sini ekleyin.  
  
## <a name="create-a-list-instance-event-receiver"></a>Bir liste örneği olay alıcısı oluşturma  
 Aşağıdaki adımlarda, bir özel Duyurular listesi örneğinde gerçekleşen olayları yanıtlamanıza izin listesi öğesi olay alıcısı değiştirmek gösterilmektedir.  
  
#### <a name="to-modify-an-event-receiver-to-respond-to-a-specific-list-instance"></a>Belirli bir liste örneği için yanıt vermek için bir olay alıcısı değiştirmek için  
  
1.  Bir tarayıcıda SharePoint sitesini açın.  
  
2.  Gezinti bölmesinde **listeler** bağlantı.  
  
3.  İçinde **tüm Site içeriğini** sayfasında **Oluştur** bağlantı.  
  
4.  İçinde **Oluştur** iletişim kutusunda **duyuruları** yazın, duyuru ad **TestAnnouncements**ve ardından **Oluştur**düğmesi.  
  
5.  İçinde [!INCLUDE[vsprvs](../sharepoint/includes/vsprvs-md.md)], bir olay alıcısı projesi oluşturun.  
  
6.  İçinde **ne tür bir olay alıcısı istiyor musunuz?** listesinde **liste öğesi etkinlikleri**.  
  
    > [!NOTE]  
    >  Başka bir tür için bir liste tanımı, örneğin, kapsamları olay alıcısının belirleyebilirsiniz **listesi e-posta olayları** veya **liste iş akışı etkinlikleri**.  
  
7.  İçinde **olay kaynağı hangi öğe olmalıdır?** listesinde **duyuruları**.  
  
8.  İçinde **aşağıdaki olayları işlemek** listesinden **bir öğe eklendiğinde** onay kutusunu işaretleyin ve ardından **son** düğmesi.  
  
9. İçinde **Çözüm Gezgini**, EventReceiver1 altında açın *Elements.xml*.  
  
     Olay alıcısı şu anda aşağıdaki satırı kullanarak duyuruları liste tanımı başvuruyor:  
  
    ```xml  
    <Receivers ListTemplateId="104">  
    ```  
  
     Aşağıdaki metni şu satırı değiştirin:  
  
    ```xml  
    <Receivers ListUrl="Lists/TestAnnouncements">  
    ```  
  
     Bu yeni gerçekleşen olaylara yanıt vermek için olay alıcı yönlendirir **TestAnnouncements** oluşturduğunuz Duyurular listesi. Değiştirebileceğiniz `ListURL` SharePoint sunucusundaki herhangi bir liste örneği başvurmak için özniteliği.  
  
10. Olay alıcısı için kod dosyasını açın ve ItemAdding yöntemde bir kesme noktası koyun.  
  
11. Seçin **F5** anahtarı oluşturun ve çözümü çalıştırın.  
  
12. SharePoint'te seçin **TestAnnouncements** Gezinti bölmesindeki bağlantı.  
  
13. Seçin **Yeni duyuru Ekle** bağlantı.  
  
14. Duyuru için bir başlık girin ve ardından **Kaydet** düğmesi.  
  
     Özel Duyuru listesine yeni öğe eklendiğinde, kesme noktasına isabet dikkat edin.  
  
15. Seçin **F5** sürdürmek için anahtar.  
  
16. Gezinti bölmesinde **listeler** bağlantısını ve ardından **duyuruları** bağlantı.  
  
17. Yeni bir duyuru ekleyin.  
  
     Alıcı yalnızca özel duyuru liste örneği olayları yanıtlamak için yapılandırıldığından olay alıcısı'te yeni duyurudan tetiklemez dikkat edin **TestAnnouncements**.  
  
## <a name="see-also"></a>Ayrıca bkz.
 [Nasıl yapılır: Olay alıcısı oluşturma](../sharepoint/how-to-create-an-event-receiver.md)   
 [SharePoint çözümleri geliştirme](../sharepoint/developing-sharepoint-solutions.md)  

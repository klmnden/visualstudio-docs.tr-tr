---
title: 'Nasıl yapılır: Olay alıcısı oluşturma | Microsoft Docs'
ms.date: 02/02/2017
ms.topic: conceptual
f1_keywords:
- VS.SharePointTools.SPE.EventReceiver
dev_langs:
- VB
- CSharp
- VB
- CSharp
helpviewer_keywords:
- SharePoint development in Visual Studio, event receivers
- event receivers [SharePoint development in Visual Studio]
author: John-Hart
ms.author: johnhart
manager: jillfra
ms.workload:
- office
ms.openlocfilehash: bc42a92e1d7dcc73bb6bc0433da4e6a31d7fefb2
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62966763"
---
# <a name="how-to-create-an-event-receiver"></a>Nasıl yapılır: Olay alıcısı oluşturma
  Oluşturarak *Olay alıcıları*, bir kullanıcı SharePoint öğeleri listeleri gibi veya liste öğesi ile etkileşim kurduğunda, yanıt verebilirsiniz. Örneğin, bir kullanıcı takvimi değiştirir veya bir ad kişiler listeden silmesi olay alıcısı kodda tetiklenebilir. Bu konuyu takip ederek, bir liste örneği için bir olay alıcısı ekleme konusunda bilgi edinebilirsiniz.

 Bu adımları tamamlamak için yüklü olmalıdır [!INCLUDE[vsprvs](../sharepoint/includes/vsprvs-md.md)] ve Windows ve SharePoint sürümleri desteklenir. Bu örnek bir SharePoint projesine gerektirdiğinden, ayrıca konudaki yordama tamamlamış olmanız gerekir [izlenecek yol: SharePoint için site sütunu, içerik türü ve liste oluşturma](../sharepoint/walkthrough-create-a-site-column-content-type-and-list-for-sharepoint.md).

## <a name="adding-an-event-receiver"></a>Bir olay alıcısı ekleme
 Oluşturduğunuz proje [izlenecek yol: SharePoint için site sütunu, içerik türü ve liste oluşturma](../sharepoint/walkthrough-create-a-site-column-content-type-and-list-for-sharepoint.md) özel site sütunları, özel bir liste ve içerik türünü içerir. Aşağıdaki yordamda, bu proje bir basit olay işleyicisi (bir olay alıcısı) ekleyerek listeleri gibi SharePoint öğeleri gerçekleşen olayları işlemek nasıl gösteren bir liste örneği için genişletin.

#### <a name="to-add-an-event-receiver-to-the-list-instance"></a>Liste örneği için olay alıcı eklemek için

1. Oluşturduğunuz proje açmak [izlenecek yol: SharePoint için site sütunu, içerik türü ve liste oluşturma](../sharepoint/walkthrough-create-a-site-column-content-type-and-list-for-sharepoint.md).

2. İçinde **Çözüm Gezgini**, adlı SharePoint proje düğümünü seçin **Clinic**.

3. Menü çubuğunda, **proje** > **Yeni Öğe Ekle**.

4. Ya da altında **Visual C#** veya **Visual Basic**, genişletme **SharePoint** düğümünü seçip **2010** öğesi.

5. İçinde **şablonları** bölmesinde seçin **olay alıcısı**, adlandırın **TestEventReceiver1**ve ardından **Tamam** düğmesi.

     **SharePoint Özelleştirme Sihirbazı** görünür.

6. İçinde **ne tür bir olay alıcısı istiyor musunuz?** listesinde **liste öğesi etkinlikleri**.

7. İçinde **olay kaynağı hangi öğe olmalıdır?** listesinde **Hastalara (Clinic\Patients)**.

8. İçinde **aşağıdaki olayları işlemek** yanındaki onay kutusunu işaretleyin, listesi **bir öğe eklendikten sonra**ve ardından **son** düğmesi.

     Adlı tek bir yöntem yeni bir olay alıcısı için kod dosyasını içeren `ItemAdded`. Sonraki adımda, böylece her kişi Scott Brown varsayılan olarak adlandırılacak bu yöntem için kod ekleyeceksiniz.

9. Varolan `ItemAdded` yöntemine aşağıdaki kodu ve ardından **F5** anahtarı:

     [!code-csharp[SP_EventReceiver#1](../sharepoint/codesnippet/CSharp/CustomField1/TestEventReceiver1/TestEventReceiver1.cs#1)]
     [!code-vb[SP_EventReceiver#1](../sharepoint/codesnippet/VisualBasic/CustomField1_VB/EventReceiver1/EventReceiver1.vb#1)]

     Kodu çalıştırır ve SharePoint sitesi web tarayıcısında görüntülenir.

10. Hızlı Başlat çubuğunda **Hastalara** bağlantısını ve ardından **Yeni Öğe Ekle** bağlantı.

     Yeni öğeler için giriş formunu açar.

11. Alanlara veri girin ve ardından **Kaydet** düğmesi.

     Seçtiğiniz sonra **Kaydet** düğmesi **hasta adı** sütun Scott Brown adına otomatik olarak güncelleştirir.

## <a name="see-also"></a>Ayrıca bkz.

- [SharePoint çözümleri geliştirme](../sharepoint/developing-sharepoint-solutions.md)
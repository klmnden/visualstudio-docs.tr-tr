---
title: 'Nasıl yapılır: Araç kutusuna etkinlik ekleme | Microsoft Docs'
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-workflow-designer
ms.topic: reference
ms.assetid: b3a8a785-5928-457a-8a50-30267e29503d
caps.latest.revision: 16
author: gewarren
ms.author: gewarren
manager: jillfra
ms.openlocfilehash: 0aa6a76555a18c142acb8759b1bc71d56e9d7dcd
ms.sourcegitcommit: 08fc78516f1107b83f46e2401888df4868bb1e40
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/15/2019
ms.locfileid: "65690935"
---
# <a name="how-to-add-activities-to-the-toolbox"></a>Nasıl yapılır: Araç Kutusuna Etkinlik Ekleme
Etkinlikleri eklenebilir **araç kutusu** çözümünüzdeki birkaç farklı yolla. Bunları içinde geçerli projenize ekleyin, bunları farklı bir proje başvurusu veya bunları farklı bir derlemeden başvurulacak.  
  
### <a name="to-add-an-activity-from-within-your-current-project"></a>Geçerli projeyi içinde etkinliği eklemek için  
  
1. Yeni bir özel etkinlik, geçerli iş akışı projenize ekleyin. [!INCLUDE[crabout](../includes/crabout-md.md)] projeniz için yeni bir özel etkinlik ekleme [nasıl yapılır: Bir iş akışı projesine yeni öğe ekleme](../workflow-designer/how-to-add-a-new-item-to-a-workflow-project.md).  
  
2. Özel mantığı etkinlik ekleyin.  
  
3. Projeyi oluşturun. Derleme başarılı olursa yeni bir kategoride **araç kutusu** adlı "\<*proje adı*>", kategorisindeki özel etkinlik ile görüntülenir.  
  
    > [!NOTE]
    > Araç kutusu sıfırlarsanız, çözümü yeniden oluşturulmuş olsa bile özel etkinlikler kaldırılacak. Özel etkinlikler araç kutusu sıfırlandı sonra yeniden için yeniden [!INCLUDE[vs2010](../includes/vs2010-md.md)].  
  
    > [!NOTE]
    > Araç yalnızca belirli bir ada bir etkinlik gösterebilirsiniz. İki etkinliği farklı derlemelerden aynı sınıf adı varsa, yalnızca biri görüntülenir.  
  
    > [!NOTE]
    > Uygulama etki alanı Düzenleyicisi örnekleri arasında paylaşılan; statik değişken kullanılması durumunda da Düzenleyicisi örnekleri arasında paylaşılır. Bu, istenen davranışı değilse, bir hizmet değişken örneklerini izlemek için kullanılmalıdır. Bkz: [ModelItem düzenleme bağlamını kullanarak](https://msdn.microsoft.com/library/7f9f1ea5-0147-4079-8eca-be94f00d3aa1) tasarımcısı içindeki Hizmetleri kullanımı hakkında bilgi.  
  
### <a name="to-add-an-activity-from-within-a-different-project"></a>Etkinliği içinde farklı bir projeye eklemek için  
  
1. En az bir iş akışı projesi ve özel etkinlik kitaplığı projesi veya özel bir etkinlik tanımlayan başka bir iş akışı projesi içeren bir çözüm açın.  
  
2. Her iki proje oluşturun. Yapılar başarılı olursa yeni bir kategoride **araç kutusu** adlı "\<*proje adı*>" Bu kategorisindeki özel etkinlik ile görüntülenir.  
  
### <a name="to-add-an-activity-to-the-toolbox-from-an-assembly"></a>Bir derlemeye ait Araç Kutusu'na bir etkinlik eklemek için  
  
1. Bir iş akışı çözümü açın.  
  
2. Gelen **Araçları** menüsünde **araç kutusu öğelerini Seç...** .  
  
3. İçinde **araç kutusu öğelerini Seç** iletişim kutusunda, **System.Activities bileşenleri** sekmesine, ardından tıklayın **Gözat...** eklemek istediğiniz özel etkinlik içeren derlemeye gidin.  
  
4. Derlemeyi seçin ve tıklayın **Tamam**. Özel Etkinlik bileşen bileşenleri listesine eklenir ve otomatik olarak seçilir.  
  
    1. Tıklayın **Tamam** iletişim kutusunu kapatmak için.  
  
5. Araç kutusu görüntülemek için seçin **araç kutusu** gelen **görünümü** menüsü.  
  
6. Özel Etkinlik görünür **araç kutusu** odaktaki öğeyi eklenmeden önce olan kategorisi altında. Örneğin, varsa **genel** kategori seçilmedi **araç kutusu** görünür altında etkinlik araç kutusu öğesi eklemeden önce **genel** kategorisi.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [İş Akışı Tasarımcısını Kullanma](../workflow-designer/using-the-workflow-designer.md)
---
title: 'İş Akışı Tasarımcısı - nasıl yapılır: Araç Kutusuna Etkinlik Ekleme'
ms.date: 11/04/2016
ms.topic: conceptual
ms.assetid: b3a8a785-5928-457a-8a50-30267e29503d
author: gewarren
ms.author: gewarren
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: b9e50736e5d9bc55eadf0aab7e7f00d26eb03249
ms.sourcegitcommit: 1fc6ee928733e61a1f42782f832ead9f7946d00c
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/22/2019
ms.locfileid: "60117245"
---
# <a name="how-to-add-activities-to-the-toolbox"></a>Nasıl yapılır: Araç Kutusuna Etkinlik Ekleme

Etkinlikleri eklenebilir **araç kutusu** çözümünüzdeki birkaç farklı yolla. Bunları içinde geçerli projenize ekleyin, bunları farklı bir proje başvurusu veya bunları farklı bir derlemeden başvurulacak.

## <a name="to-add-an-activity-from-within-your-current-project"></a>Geçerli projeyi içinde etkinliği eklemek için

1. Yeni bir özel etkinlik, geçerli iş akışı projenize ekleyin. Projenize yeni bir özel etkinlik ekleme hakkında daha fazla bilgi için bkz. [nasıl yapılır: Bir iş akışı projesine yeni öğe ekleme](../workflow-designer/how-to-add-a-new-item-to-a-workflow-project.md).

2. Özel mantığı etkinlik ekleyin.

3. Projeyi oluşturun. Derleme başarılı olursa yeni bir kategoride **araç kutusu** adlı "\<*proje adı*>", kategorisindeki özel etkinlik ile görüntülenir.

    > [!NOTE]
    > Araç kutusu sıfırlarsanız, çözümü yeniden oluşturulmuş olsa bile özel etkinlikler kaldırılacak. Özel etkinlikler araç kutusu sıfırlandı sonra yeniden doldurmak için Visual Studio'yu yeniden başlatın.

    > [!NOTE]
    > Araç yalnızca belirli bir ada bir etkinlik gösterebilirsiniz. İki etkinliği farklı derlemelerden aynı sınıf adı varsa, yalnızca biri görüntülenir.

    > [!NOTE]
    > Uygulama etki alanı Düzenleyicisi örnekleri arasında paylaşılan; statik değişken kullanılması durumunda da Düzenleyicisi örnekleri arasında paylaşılır. Bu, istenen davranışı değilse, bir hizmet değişken örneklerini izlemek için kullanılmalıdır. Bkz: [ModelItem düzenleme bağlamını kullanarak](/dotnet/framework/windows-workflow-foundation/using-the-modelitem-editing-context) tasarımcısı içindeki Hizmetleri kullanımı hakkında bilgi.

## <a name="to-add-an-activity-from-within-a-different-project"></a>Etkinliği içinde farklı bir projeye eklemek için

1. En az bir iş akışı projesi ve özel etkinlik kitaplığı projesi veya özel bir etkinlik tanımlayan başka bir iş akışı projesi içeren bir çözüm açın.

2. Her iki proje oluşturun. Yapılar başarılı olursa yeni bir kategoride **araç kutusu** adlı "\<*proje adı*>" Bu kategorisindeki özel etkinlik ile görüntülenir.

## <a name="to-add-an-activity-to-the-toolbox-from-an-assembly"></a>Bir derlemeye ait Araç Kutusu'na bir etkinlik eklemek için

1. Bir iş akışı çözümü açın.

2. Gelen **Araçları** menüsünde **araç kutusu öğelerini Seç**.

3. İçinde **araç kutusu öğelerini Seç** iletişim kutusunda **System.Activities bileşenleri** sekmesinde'e tıklayın **Gözat** özel içeren derlemeye gidin eklemek istediğiniz etkinliği.

4. Derlemeyi seçin ve tıklayın **Tamam**. Özel Etkinlik bileşen bileşenleri listesine eklenir ve otomatik olarak seçilir.

    1. Tıklayın **Tamam** iletişim kutusunu kapatmak için.

5. Araç kutusu görüntülemek için seçin **araç kutusu** gelen **görünümü** menüsü.

6. Özel Etkinlik görünür **araç kutusu** odaktaki öğeyi eklenmeden önce olan kategorisi altında. Örneğin, varsa **genel** kategori seçilmedi **araç kutusu** görünür altında etkinlik araç kutusu öğesi eklemeden önce **genel** kategorisi.

## <a name="see-also"></a>Ayrıca bkz.

- [İş Akışı Tasarımcısını Kullanma](developing-applications-with-the-workflow-designer.md)
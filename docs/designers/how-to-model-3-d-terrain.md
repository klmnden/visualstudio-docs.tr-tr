---
title: 'Nasıl yapılır: Model 3B Arazi'
ms.date: 11/04/2016
ms.topic: conceptual
ms.assetid: f779b1fd-82a9-4a11-8ab7-c1c9caabc883
author: gewarren
ms.author: gewarren
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 41974aee19cf1e4919028d5ef0f0e9b53c6b369e
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62844466"
---
# <a name="how-to-model-3d-terrain"></a>Nasıl yapılır: 3B arazi modeli oluşturma

Bu makalede, 3B Arazi modeli oluşturmak için Model Düzenleyicisi'ni kullanma gösterilmektedir.

## <a name="create-a-3d-terrain-model"></a>Bir 3B Arazi modeli oluşturma

Ek yüzleri yapmak için bir düz kümelere ve ardından ilginç Arazi özellikleri oluşturmak için kendi köşeler işleme, 3B Arazi oluşturabilirsiniz.

İşlemi tamamladığınızda, model şu şekilde görünmelidir:

![3&#45;Arazi modeli gösteren D Sahne](../designers/media/digit-terrain-model.png)

Başlamadan önce emin **özellikleri** penceresi ve **araç kutusu** görüntülenir.

1. Bir 3B modeli ile çalışmak için oluşturun. Başlarken bölümünde projenize bir model ekleme hakkında daha fazla bilgi için bkz. [Model Düzenleyicisi](../designers/model-editor.md).

2. Düzlem sahneye ekleyin. İçinde **araç kutusu**altında **şekiller**seçin **düzlemi** ve tasarım yüzeyine taşıyın.

    > [!TIP]
    > Düzlem nesne çalışmak kolaylaştırmak için tasarım yüzeyini çerçevesi. İçinde **seçin** modu düzlemi nesneyi seçin ve ardından Model Düzenleyicisi araç çubuğunda **çerçeve nesnesi** düğmesi.

3. Yüz seçim moduyla girin. Model Düzenleyicisi araç çubuğunda **seçin yüz**.

4. Düzlem alt bölümlere ayırır. Yüz seçimi modunda, seçimi için etkinleştirmek için bir kez düzlemi seçin ve yeniden yalnızca kendi yüz seçmek için bunu seçin. Model Düzenleyicisi araç çubuğunda **yüzü alt bölümlere ayırır**. Bu dört eşit boyutlu bölümlere bölme düzlemine yeni köşeler ekler.

5. Daha fazla alt bölümleri oluşturun. Yeni yüzler seçili durumdayken seçin **yüzü alt bölümlere ayırır** iki kez. Bu, 64 yüzleri toplam oluşturur. Daha fazla alt bölümleri oluşturarak Arazi daha da fazla ayrıntı verebilir.

6. Nokta seçim moduna girin. Model Düzenleyicisi araç çubuğunda **noktası seç**.

7. Arazi özelliği oluşturmak için bir noktayı değiştirin. Nokta seçim moduyla noktalarından birini seçin ve ardından Model Düzenleyicisi araç çubuğunda **çevir** aracı. Bir noktayı temsil eden bir kutu tasarım yüzeyinde görünür. Yeşil ok kutusuna gidin ve böylece noktası yüksekliğini değiştirmek için kullanın. İlginç Arazi özellikleri oluşturmak farklı noktaları için bu adımı yineleyin.

    > [!TIP]
    > Tek seferde bir tutum değiştirmek üzere birkaç noktası seçebilirsiniz.

Arazi modeli tamamlanmıştır. İşte son modelin yeniden uygulanan Phong gölgelendirme ile:

![3&#45;Arazi modeli gösteren D Sahne](../designers/media/digit-terrain-model.png)

Bu Arazi modeli açıklanan gradyan gölgelendirici etkisini göstermek için kullanabileceğiniz [nasıl yapılır: Geometri tabanlı gradyan gölgelendirici oluşturma](../designers/how-to-create-a-geometry-based-gradient-shader.md).

## <a name="see-also"></a>Ayrıca bkz.

- [Model düzenleyicisi](../designers/model-editor.md)
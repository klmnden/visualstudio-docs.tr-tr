---
title: 'Nasıl yapılır: 3B Arazi modeli oluşturma | Microsoft Docs'
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-designers
ms.topic: conceptual
ms.assetid: f779b1fd-82a9-4a11-8ab7-c1c9caabc883
caps.latest.revision: 19
author: gewarren
ms.author: gewarren
manager: jillfra
ms.openlocfilehash: 90a24ef7b5bff321d460834a8fdde24e3e6cfd75
ms.sourcegitcommit: 47eeeeadd84c879636e9d48747b615de69384356
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "63434450"
---
# <a name="how-to-model-3-d-terrain"></a>Nasıl yapılır: Model 3B Arazi
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Bu belge, 3B Arazi modeli oluşturmak için Model Düzenleyicisi nasıl yapılacağı açıklanır.  
  
 Bu belgede şu faaliyetler gösterilmiştir:  
  
- Nesneler bir Sahne ekleme  
  
- Yüzleri ve noktalarını seçme  
  
- Seçimleri çevirme  
  
- Kullanarak **yüzü alt bölümlere ayırır** aracı  
  
- Çerçeve tasarım yüzeyine bir nesne  
  
## <a name="creating-a-3-d-terrain-model"></a>Bir 3B Arazi modeli oluşturma  
 Ek yüzleri yapmak için bir düz kümelere ve ardından ilginç Arazi özellikleri oluşturmak için kendi köşeler işleme, 3B Arazi oluşturabilirsiniz.  
  
 İşlemi tamamladığınızda, model şu şekilde görünmelidir:  
  
 ![3&#45;Arazi modeli gösteren D Sahne](../designers/media/digit-terrain-model.png "basamak Arazi modeli")  
  
 Başlamadan önce emin **özellikleri** penceresi ve **araç kutusu** görüntülenir.  
  
#### <a name="to-create-a-3-d-terrain-model"></a>Bir 3B Arazi modeli oluşturma  
  
1. Çalışmak için bir 3B modeli oluşturun. Başlarken bölümünde projenize bir model ekleme hakkında daha fazla bilgi için bkz. [Model Düzenleyicisi](../designers/model-editor.md).  
  
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
  
   ![3&#45;Arazi modeli gösteren D Sahne](../designers/media/digit-terrain-model.png "basamak Arazi modeli")  
  
   Bu Arazi modeli açıklanan gradyan gölgelendirici etkisini göstermek için kullanabileceğiniz [nasıl yapılır: Geometri tabanlı gradyan gölgelendirici oluşturma](../designers/how-to-create-a-geometry-based-gradient-shader.md).  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Model Düzenleyicisi](../designers/model-editor.md)

---
title: 'Nasıl yapılır: Temel doku gölgelendiricisi oluşturma | Microsoft Docs'
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-designers
ms.topic: conceptual
ms.assetid: 5af113fb-6415-4be0-8b23-10fddb10e80a
caps.latest.revision: 25
author: gewarren
ms.author: gewarren
manager: jillfra
ms.openlocfilehash: dce20d3e1833659ebfec2e84e6bff7f86dff844e
ms.sourcegitcommit: 47eeeeadd84c879636e9d48747b615de69384356
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "63438439"
---
# <a name="how-to-create-a-basic-texture-shader"></a>Nasıl yapılır: Temel doku gölgelendiricisi oluşturma
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Bu belge, gölgelendirici Tasarımcısı ve yönlendirilmiş grafik gölgelendirici dili (DGSL) bir tek doku gölgelendiricisi oluşturmak için nasıl kullanılacağını gösterir. Bu gölgelendiriciyi RGB ve dokudan örneklenen alfa değerleri için doğrudan son rengini ayarlar.  
  
 Bu belgede şu faaliyetler gösterilmiştir:  
  
- Bir gölgelendirici grafiği düğümleri kaldırma  
  
- Grafiğe düğüm ekleme  
  
- Gölgelendirici parametrelerini ayarlama  
  
- Parametre görünürlüğünü ayarlama  
  
- Düğümleri bağlanma  
  
## <a name="creating-a-basic-texture-shader"></a>Temel doku gölgelendiricisi oluşturma  
 Temel, tek bir doku gölgelendirici doğrudan son çıkış rengi renk ve alfa değerleri bir doku örneğinin yazarak uygulayabilirsiniz.  
  
 Başlamadan önce emin **özellikleri** penceresi ve **araç kutusu** görüntülenir.  
  
#### <a name="to-create-a-basic-texture-shader"></a>Temel doku gölgelendiricisi oluşturma  
  
1. Çalışmak için bir DGSL gölgelendirici oluşturun. Projenize DGSL gölgelendirici ekleme hakkında daha fazla bilgi için bkz. Başlarken bölümünde [gölgelendirici Tasarımcısı](../designers/shader-designer.md).  
  
2. Silme **nokta rengi** düğümü. İçinde **seçin** modunu Seç **nokta rengi** düğümünü ve ardından menü çubuğunda, **Düzenle**, **Sil**. Bu, sonraki adımda eklenen düğümü için yer sağlar.  
  
3. Ekleme bir **doku örneğinin** grafiğe düğüm. İçinde **araç kutusu**altında **doku**seçin **doku örneğinin** ve tasarım yüzeyine taşıyın.  
  
4. Ekleme bir **doku koordinatı** grafiğe düğüm. İçinde **araç kutusu**altında **doku**seçin **doku koordinatı** ve tasarım yüzeyine taşıyın.  
  
5. Bir doku uygulamak için seçin. İçinde **seçin** modunu seçin **doku örneğinin** düğümünü ve ardından **özellikleri** penceresinde kullanarak kullanmak istediğiniz dokuyu belirtin **dosya adı**  özelliği.  
  
6. Doku genel olarak erişilebilir hale getirir. Seçin **doku örneğinin** düğümünü ve ardından **özellikleri** penceresinde **erişim** özelliğini **genel**. Gibi başka bir aracı, doku ayarlayabilirsiniz artık **Model Düzenleyicisi**.  
  
7. Doku koordinatlarını doku örneğine bağlanın. İçinde **seçin** modu, taşıma **çıkış** , terminal **doku koordinatı** düğüme **UV** , terminal **doku Örnek** düğümü. Bu bağlantıyı belirtilen koordinatlarda dokuyu örnekler.  
  
8. Doku örneğinin son rengi bağlanın. Taşıma **RGB** , terminal **doku örneğinin** düğüme **RGB** , terminal **son rengini** düğümünü ve ardından taşıyın **Alfa** , terminal **doku örneğinin** düğüme **alfa** , terminal **son rengini** düğümü.  
  
   Aşağıdaki resimde tamamlanmış gölgelendirici grafiği ve bir küpe uygulanan gölgelendiricinin önizlemesini gösterir.  
  
> [!NOTE]
> Bu çizimde, bir önizleme şeklinde kullanılır ve bir doku gölgelendirici etkisini daha iyi göstermek için belirtilen.  
  
 ![Gölgelendirici grafiği ve etkisini önizlemesini](../designers/media/digit-texture-effect.png "basamak doku etkisi")  
  
 Belirli şekiller daha iyi önizlemeleri için bazı gölgelendiricileri sağlayabilir. Gölgelendirici Tasarımcısı'nda gölgelendiricileri önizleme hakkında daha fazla bilgi için bkz. [gölgelendirici Tasarımcısı](../designers/shader-designer.md)  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Nasıl yapılır: 3B modele gölgelendirici uygulama](../designers/how-to-apply-a-shader-to-a-3-d-model.md)   
 [Görüntü Düzenleyicisi](../designers/image-editor.md)   
 [Gölgelendirici Tasarımcısı](../designers/shader-designer.md)   
 [Gölgelendirici Tasarımcısı Düğümleri](../designers/shader-designer-nodes.md)

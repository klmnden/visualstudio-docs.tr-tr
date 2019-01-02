---
title: 'Nasıl Yapılır: Temel doku gölgelendiricisi oluşturma'
ms.date: 11/04/2016
ms.prod: visual-studio-dev15
ms.topic: conceptual
ms.assetid: 5af113fb-6415-4be0-8b23-10fddb10e80a
author: gewarren
ms.author: gewarren
manager: douge
ms.workload:
- multiple
ms.openlocfilehash: 85de6bcaa4b3b62c9a3ad03464d9b95cb0134a6e
ms.sourcegitcommit: 37fb7075b0a65d2add3b137a5230767aa3266c74
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/02/2019
ms.locfileid: "53946074"
---
# <a name="how-to-create-a-basic-texture-shader"></a>Nasıl Yapılır: Temel doku gölgelendiricisi oluşturma

Bu makalede, gölgelendirici Tasarımcısı ve yönlendirilmiş grafik gölgelendirici dili (DGSL) bir tek doku gölgelendiricisi oluşturmak için nasıl kullanılacağını gösterir. Bu gölgelendiriciyi RGB ve dokudan örneklenen alfa değerleri için doğrudan son rengini ayarlar.

## <a name="create-a-basic-texture-shader"></a>Temel doku gölgelendiricisi oluşturma

Temel, tek bir doku gölgelendirici doğrudan son çıkış rengi renk ve alfa değerleri bir doku örneğinin yazarak uygulayabilirsiniz.

Başlamadan önce emin **özellikleri** penceresi ve **araç kutusu** görüntülenir.

1.  Çalışmak için bir DGSL gölgelendirici oluşturun. Projenize DGSL gölgelendirici ekleme hakkında daha fazla bilgi için bkz. Başlarken bölümünde [gölgelendirici Tasarımcısı](../designers/shader-designer.md).

2.  Silme **nokta rengi** düğümü. İçinde **seçin** modunu Seç **nokta rengi** düğümünü ve ardından menü çubuğunda, **Düzenle** > **Sil**. Bu, sonraki adımda eklenen düğümü için yer sağlar.

3.  Ekleme bir **doku örneğinin** grafiğe düğüm. İçinde **araç kutusu**altında **doku**seçin **doku örneğinin** ve tasarım yüzeyine taşıyın.

4.  Ekleme bir **doku koordinatı** grafiğe düğüm. İçinde **araç kutusu**altında **doku**seçin **doku koordinatı** ve tasarım yüzeyine taşıyın.

5.  Bir doku uygulamak için seçin. İçinde **seçin** modunu seçin **doku örneğinin** düğümünü ve ardından **özellikleri** penceresinde kullanarak kullanmak istediğiniz dokuyu belirtin **dosya adı**  özelliği.

6.  Doku genel olarak erişilebilir hale getirir. Seçin **doku örneğinin** düğümünü ve ardından **özellikleri** penceresinde **erişim** özelliğini **genel**. Gibi başka bir aracı, doku ayarlayabilirsiniz artık **Model Düzenleyicisi**.

7.  Doku koordinatlarını doku örneğine bağlanın. İçinde **seçin** modu, taşıma **çıkış** , terminal **doku koordinatı** düğüme **UV** , terminal **doku Örnek** düğümü. Bu bağlantıyı belirtilen koordinatlarda dokuyu örnekler.

8.  Doku örneğinin son rengi bağlanın. Taşıma **RGB** , terminal **doku örneğinin** düğüme **RGB** , terminal **son rengini** düğümünü ve ardından taşıyın **Alfa** , terminal **doku örneğinin** düğüme **alfa** , terminal **son rengini** düğümü.

Aşağıdaki resimde tamamlanmış gölgelendirici grafiği ve bir küpe uygulanan gölgelendiricinin önizlemesini gösterir.

> [!NOTE]
> Bu çizimde, bir önizleme şeklinde kullanılır ve bir doku gölgelendirici etkisini daha iyi göstermek için belirtilen.

![Gölgelendirici grafiği ve etkisini önizlemesi](../designers/media/digit-texture-effect.png)

Belirli şekiller daha iyi önizlemeleri için bazı gölgelendiricileri sağlayabilir. Gölgelendirici Tasarımcısı'nda gölgelendiricileri önizleme hakkında daha fazla bilgi için bkz. [gölgelendirici Tasarımcısı](../designers/shader-designer.md)

## <a name="see-also"></a>Ayrıca bkz.

- [Nasıl yapılır: 3B modele gölgelendirici uygulama](../designers/how-to-apply-a-shader-to-a-3-d-model.md)
- [Görüntü Düzenleyicisi](../designers/image-editor.md)
- [Gölgelendirici Tasarımcısı](../designers/shader-designer.md)
- [Gölgelendirici Tasarımcısı düğümleri](../designers/shader-designer-nodes.md)
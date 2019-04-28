---
title: 'Nasıl yapılır: Temel doku oluşturma | Microsoft Docs'
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-designers
ms.topic: conceptual
ms.assetid: 0222e8bf-d29f-421b-9b1f-123d500fa179
caps.latest.revision: 17
author: gewarren
ms.author: gewarren
manager: jillfra
ms.openlocfilehash: bd1a9a2a269c173ef9dcb47b39921073802fe1ee
ms.sourcegitcommit: 47eeeeadd84c879636e9d48747b615de69384356
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "63438407"
---
# <a name="how-to-create-a-basic-texture"></a>Nasıl yapılır: Temel doku oluşturma
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Bu belge temel bir doku oluşturmak için görüntü Düzenleyicisi nasıl yapılacağı açıklanır.  
  
 Bu belgede şu faaliyetler gösterilmiştir:  
  
- Doku boyutunu ayarlama  
  
- Ön ve arka plan renkleri ayarlama  
  
- Alfa kanalını (saydam) kullanma  
  
- Kullanarak **dolgu** ve **elipsin** araçları  
  
- Aracı özelliklerini ayarlama  
  
## <a name="creating-a-basic-texture"></a>Temel doku oluşturma  
 Görüntüleri ve oyunlarda veya uygulamalarda ilişkin dokular oluşturmak ve değiştirmek için görüntü Düzenleyicisi'ni kullanabilirsiniz.  
  
 Aşağıdaki adımlar, bir "hedef merkezi" hedefi temsil eden bir doku oluşturmayı gösterir. İşlemi tamamladığınızda, doku aşağıdaki resimdeki gibi görünmelidir. Daha iyi dokudaki saydamlık göstermek için görüntü Düzenleyicisi göstermek için yeşil, Damalı düzeni kullanmak için yapılandırıldı.  
  
 ![Saydamlık yeşil renkte gösterilir "hedef merkezi" hedefle](../designers/media/digit-bullseye-texture-in-editor.png "basamak-hedef merkezi-doku-Düzenleyici")  
  
 Başlamadan önce emin **özellikleri** penceresi görüntülenir. Kullandığınız **özellikleri** penceresi görüntüyü boyutunu ayarlayın, aracı özelliklerini değiştirmek ve çalışırken renkleri belirtin.  
  
#### <a name="to-create-a-bullseye-target-texture"></a>Bir "hedef merkezi" hedef dokusu oluşturmak için  
  
1. Çalışmak için bir doku oluşturun. Projenize doku ekleme hakkında daha fazla bilgi için bkz. Başlarken bölümünde [Resim Düzenleyicisi](../designers/image-editor.md).  
  
2. Görüntü boyutu 512 x 512 piksel olarak ayarlayın. İçinde **özellikleri** penceresinde değerlerini ayarlayın **genişliği** ve **yükseklik** özelliklerine `512`.  
  
3. Görüntü Düzenleyicisi araç çubuğunda **dolgu** aracı. **Özellikleri** penceresi özelliklerini görüntüler **dolgu** aracından görüntü özelliklerini birlikte.  
  
4. Ön plan rengini tamamen saydam siyah olarak ayarlar. İçinde **özellikleri** penceresi içinde **renkleri** özellik grubu, select **ön plan**. Değerlerini ayarlayın **R**, **G**, **B**, ve **A** yanındaki Renk Seçici için Özellikler `0`.  
  
5. Görüntü Düzenleyicisi araç çubuğunda **dolgu** aracı tuşuna basın ve Shift tuşunu basılı tutun ve herhangi bir noktaya görüntüyü seçin. Shift tuşunu kullanarak görüntüde rengini değiştirmek için dolgu rengi alfa değeri neden olur; Aksi takdirde, alfa değeri dolgu rengi renk görüntünün birlikte karıştırmak için kullanılır.  
  
   > [!IMPORTANT]
   > Bu adımda, önceki adımda, renk seçimi ile birlikte, temel görüntü için çizim "hedef merkezi" hedef dokuyu hazırlanır sağlar. Resmin saydam siyah doldurulur olduğunda — ve hedef kenarlığını siyah olduğundan — yumuşatma yapıt hedefi geçici bir çözüm olacaktır.  
  
6. Görüntü Düzenleyicisi araç çubuğunda **elipsin** aracı.  
  
7. Ön plan rengini tamamen opak siyah olarak ayarlar. Değerlerini ayarlayın **R**, **G**, ve **B** özelliklerine `0` değeri **A** özelliğini `255`.  
  
8. Arka plan rengi tamamen opak beyaz olarak ayarlar. İçinde **özellikleri** penceresi içinde **renkleri** özellik grubu, select **arka plan**. Değerlerini ayarlayın **R**, **G**, **B**, ve **A** özelliklerine `255`.  
  
9. Elipsin ana hattın genişliği ayarlayın. İçinde **özellikleri** penceresi içinde **Görünüm** özellik grubu ayarlayın **genişliği** özelliğini `8`.  
  
10. Bu düzgünleştirme etkin olduğundan emin olun. İçinde **özellikleri** penceresi, **Görünüm** özelliği emin olun, grup **yumuşatma** özelliği ayarlanmış.  
  
11. Kullanarak **elipsin** aracı, piksel Koordinattan bir daire çizin `(3, 3)` piksel koordinat için `(508, 508)`. Daha fazla daire çizmek için kolay, basın ve çizerken Shift tuşunu basılı tutun.  
  
    > [!NOTE]
    > Geçerli işaretçisi konumunu piksel koordinatlarını görüntülenir [!INCLUDE[vsprvs](../includes/vsprvs-md.md)] durum çubuğu.  
  
12. Arka plan rengini değiştirin. Ayarlama **R** için `44`, **G** için `165`, **B** için `211`, ve **A** için `255`.  
  
13. Piksel koordinat başka bir daire çizin `(64, 64)` piksel koordinat için `(448, 448)`.  
  
14. Tamamen opak beyaz arka plan rengini değiştirin. Ayarlama **R**, **G**, **B**, ve **A** için `255`.  
  
15. Piksel koordinat başka bir daire çizin `(128, 128)` piksel koordinat için `(384, 384)`.  
  
16. Arka plan rengini değiştirin. Ayarlama **R** için `255`, **G** ve **B** için `64`, ve **A** için `255`.  
  
17. Piksel koordinat başka bir daire çizin `(192, 192)` piksel koordinat için `(320, 320)`.  
  
    "Hedef merkezi" hedef dokuyu tamamlanmıştır. Saydamlık ile gösterilen son görüntü aşağıda verilmiştir.  
  
    ![Tam "hedef"merkezi hedef doku](../designers/media/gfx-image-demo-bullseye.png "gfx_image_demo_bullseye")  
  
    Bir sonraki adım, bu dokunun MIP düzeyleri oluşturabilirsiniz. Bilgi için [nasıl yapılır: MIP düzeyleri oluşturma ve değiştirme](../designers/how-to-create-and-modify-mip-levels.md).  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Görüntü Düzenleyicisi](../designers/image-editor.md)

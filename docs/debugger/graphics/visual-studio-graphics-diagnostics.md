---
title: Grafik tanılama | Microsoft Docs
ms.custom: seodec18
ms.date: 11/04/2016
ms.topic: conceptual
f1_keywords:
- vs.graphics
ms.assetid: fa69c550-62a7-41b5-bb1f-7eb04af1a6e8
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: cbc3edfabe041804a632b919eff4e565be9cc5e3
ms.sourcegitcommit: b0d8e61745f67bd1f7ecf7fe080a0fe73ac6a181
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/22/2019
ms.locfileid: "56703038"
---
# <a name="visual-studio-graphics-diagnostics"></a>Visual Studio Grafik Tanılama
Visual Studio*grafik tanılama* kaydetme ve ardından Direct3D uygulamalar oluşturma ve performans sorunları çözümleme araçları kümesidir. Grafik Tanılama, Windows PC, bir Windows cihaz öykünücüsü veya bir uzak bilgisayar veya cihaz üzerinde yerel olarak çalışan uygulamalarda kullanılabilir.

 Grafik tanılama iş akışının nasıl Direct3D uygulamanızın kullandığı kaydını yakalayarak başlar — Canlı çalıştığı gibi — davranışını hemen çözümlenebilir böylece paylaşılan ya da daha sonra kullanmak üzere kaydedildi. Yakalama oturumu başlattı ve Visual Studio'dan veya komut satırı Yakalama aracı ile el ile denetlenen **dxcap.exe**. Yakalama oturumu da başlatılan ve grafik tanılama yakalama API'leri kullanarak programlı olarak denetlenir.

 Yakalama oturumu kaydettikten sonra içeriğini Visual Studio tarafından çalınabilecek *grafik Çözümleyicisi* tam aynı kaynakları kullanarak ve işleme komutları kullanılan uygulaması herhangi bir zamanda, yakalanan kareleri yeniden. Ardından, grafik Çözümleyicisi penceresi sağlanan araçları kullanarak, yakalanan kareleri birini ayrıntılı olarak çözümlenebilir. Bu araçlar, her Direct3D API çağrısı, kaynak, işlem hattı durum nesnesi, ardışık düzen aşamasını veya yakalanan çerçevede bir piksel bile tam geçmişini incelemek için kullanılabilir. Bu araçları birlikte kullanarak, bir işleme sorunuyla sezgisel, yakalanan çerçevede görüntülenme şeklini öğesinden başlayarak ve aşağı uygulamanın kaynak kodu, gölgelendiriciler veya grafik varlıklar, sorunun kök nedenini araştırıp bulma notebook'ta incelenebilir.

 Performans sorunlarını tanılamak için yakalanan çerçeve kullanılarak çözümlenebilecek *çerçeve analizi* aracı. Bu araç, olası performans iyileştirmeleri otomatik olarak uygulama Direct3D nasıl kullanacağını değiştirip sizin için tüm çeşitlemeleri değerlendirmesi keşfediyor. Daha önce yapmış olabilirsiniz ve bu tür değişiklikler yalnızca el ile bulmak için benchmarked hangilerinin yapılan bir fark giden. Çerçeve Analizi ile yalnızca faydalı olur bildiğiniz değişiklikler yapmanız gerekir.

 Grafik Tanılama'yı arayın ve en iyi şekilde çalıştırın, grafik açısından zengin Direct3D uygulaması yardımcı olur.

 Devam [genel bakış](overview-of-visual-studio-graphics-diagnostics.md) ne sunan Visual Studio grafik Tanılama hakkında daha fazla bilgi edinmek için.

## <a name="in-this-section"></a>Bu Bölümde
 [Genel Bakış](overview-of-visual-studio-graphics-diagnostics.md) araçları ve grafik tanılama iş akışı sunar.

 [Başlarken](getting-started-with-visual-studio-graphics-diagnostics.md) Bu bölümde, grafik tanılama Direct3D uygulamanızla kullanmaya başlamak Visual Studio grafik Tanılama'yı yükleme ve öğreneceksiniz.

 [Grafik bilgilerini yakalama](capturing-graphics-information.md) uygulamanızda bir işleme sorunuyla incelemek için grafik tanılama kullanmak için önce uygulamayı DirectX nasıl kullandığı hakkında bilgi kaydedin. Kayıt oturumu sırasında uygulamanız çalışırken normalde, *yakalama* (diğer bir deyişle, seçin), ilgilendiğiniz çerçeveleri. Yakalamalar çerçeveleri nasıl işlendiğini hakkında ayrıntılı bilgi içerir. Yakalanan bilgiler grafik olarak kaydedebilirsiniz daha sonra incelemek veya takımınızın diğer üyeleriyle paylaşmak için günlük belgesi.

 [GPU kullanımı](gpu-usage.md) uygulamanızın profilini çıkarmak için grafik tanılama kullanmak için GPU kullanımı aracı kullanın. GPU kullanımı, CPU kullanımı gibi diğer profil oluşturma araçları ile uyumlu bir şekilde uygulamanızdaki performans sorunlarını katkıda bulunabilir CPU ve GPU etkinliği ilişkilendirmek için kullanılabilir.

 [Grafik günlük belgesi](graphics-log-document.md) kaydedilmiş grafik günlüğü incelenmesi başlatmak için grafik günlüğü belge penceresinde bir yakalanan çerçeve seçmek için kullandığınız — ve hatta belirli bir pikseli — böylece ayrıntılı olarak inceleyebilir *olayları* (yani olan DirectX API çağrıları), etkisi.

 [Çerçeve analizi](graphics-frame-analysis.md) bir çerçeveyi seçtikten sonra grafik çerçevesi analizi inceleyin ve işleme performansınızı ayarlamak için kullanın.

 [Olay listesi](graphics-event-list.md) bir çerçeveyi seçtikten sonra kullandığınız **grafik olay listesi** işleme sorunuyla ilgili olup olmadığını belirlemek için olaylarını incelemek için.

 [Durum](graphics-state.md) durum penceresi, geçerli olay sırasında etkin olan grafik durumu anlamanıza yardımcı olur.

 [Ardışık Düzen aşamaları](graphics-pipeline-stages.md) içinde **grafik ardışık düzen aşamaları** penceresinde yeri belirleyebilir seçili olan olay grafik ardışık düzeninin her aşamasında tarafından nasıl işlendiğini araştırmak işleme sorunuyla ilk görünür. Ardışık Düzen aşamaları İnceleme nesneyi nedeniyle yanlış bir dönüştürme görünmez yaklaştığında veya aşamalar birini ne sonraki aşamasına bekliyor eşleşmeyen bir çıktı üretir özellikle yararlı olur.

 [Olay çağrı yığını](graphics-event-call-stack.md) kullandığınız **grafik olay çağrı yığını** , işleme sorunuyla ilişkili uygulama koduna gidebilmeniz şu anda seçili olayın çağrı yığınını incelemek için.

 [Piksel geçmişi](graphics-pixel-history.md) kullanarak **grafik piksel geçmişi** penceresi şu anda seçilen piksel, etkileyen olaylar tarafından nasıl etkilendiğini analiz etmek için olay veya belirli neden olan olaylar birleşimi tanımlayabilirsiniz işleme sorunlarını türleri. Piksel gölgelendirici çıkışı olduğundan nesne yanlış işlendiğinde piksel geçmişi özellikle yararlıdır hatalı veya yanlış çerçeve arabelleği veya piksellerinin atıldı çünkü nesne bile görünmediği zaman birleştirilmiştir çerçeve arabelleği ulaşmadan önce.

 [Nesne tablosu](graphics-object-table.md) kullandığınız **Graphics Object Table** özelliklerini ve belirli Direct3D nesneleri ve şu anda seçili olayı için geçerli olan kaynakların içeriğini incelemek için. Nesne tablosu, bir olayı sırasında etkin olan grafik cihaz bağlamı belirlemek ve sabit arabellekler köşe arabellekleri ve dokular gibi grafik kaynakları içeriğini incelemek yardımcı olabilir.

 [HLSL hata ayıklayıcısı](hlsl-shader-debugger.md) aşama şu anda seçilen olay ve grafik ardışık düzen için gölgelendirici kodu nasıl davranacağını incelemek için kullandığınız **HLSL hata ayıklayıcısı** kodda adım adım için değişkenlerin içeriğini inceleyebilir ve diğer gerçekleştirin Tipik hata ayıklama görevlerini. HLSL hata ayıklayıcısı, compute gölgelendirici kodu sonuçlarını grafik ardışık düzen tarafından daha fazla işlenebilir veya yalnızca, uygulamanız tarafından okunur bağımsız olarak incelemek için de kullanabilirsiniz.

 [Komut satırı Yakalama aracı](command-line-capture-tool.md) hızlı bir şekilde yakalayın ve Visual Studio ya da programlı yakalama kullanmadan grafik bilgilerini kayıttan yürütmek için komut satırı Yakalama aracı kullanın. Özellikle, bir test ortamında veya, otomasyon için komut satırı Yakalama aracı kullanabilirsiniz.

 [Örnekler](graphics-diagnostics-examples.md) birkaç örnek grafik tanılama araçları birlikte farklı türde işleme sorunlarını tanılamak için nasıl kullanılacağını gösterir.

## <a name="related-sections"></a>İlgili Bölümler

| Başlık | Açıklama |
| - | - |
| [Hata ayıklayıcısı özellik turu](/visualstudio/debugger/debugger-feature-tour) | Hata ayıklama işlevleri tanıtır [!INCLUDE[vsprvs](../../code-quality/includes/vsprvs_md.md)]. |
| [DirectX grafik ve oyun](http://go.microsoft.com/fwlink/?LinkId=256498) | DirectX grafik teknolojilerini açıklayan makaleleri sağlar. |

---
title: '1. Adım: Bir Windows Forms uygulaması projesi oluşturma'
ms.date: 11/04/2016
ms.prod: visual-studio-dev15
ms.topic: conceptual
ms.assetid: 16ac2422-e720-4e3a-b511-bc2a54201a86
author: TerryGLee
ms.author: tglee
manager: douge
ms.workload:
- multiple
ms.openlocfilehash: 86942dda1990fe8a681ec2832b2474d42d418a63
ms.sourcegitcommit: 37fb7075b0a65d2add3b137a5230767aa3266c74
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/02/2019
ms.locfileid: "53842063"
---
# <a name="step-1-create-a-windows-forms-application-project"></a>1. Adım: Bir Windows Forms uygulaması projesi oluşturma
Resim Görüntüleyici oluşturduğunuzda ilk adım bir Windows Forms Application projesi oluşturmaktır.

 ![video bağlantısı](../data-tools/media/playvideo.gif)bu konunun video sürümü için bkz: [öğretici 1: Visual Basic'te - Video 1 resim görüntüleyici oluşturma](http://go.microsoft.com/fwlink/?LinkId=205209) veya [öğretici 1: İçinde resim görüntüleyici oluşturma C# -Video 1](http://go.microsoft.com/fwlink/?LinkId=205199). Bazı menü komutlarında ve diğer kullanıcı arabirimi öğelerinde küçük farklılıklar olduğundan bu videolarda Visual Studio'nun önceki bir sürümü kullanın. Ancak, kavramlar ve yordamlar benzer şekilde Visual Studio'nun geçerli sürümünde çalışır.

## <a name="to-create-a-windows-forms-application-project"></a>Bir Windows Forms uygulaması projesi oluşturmak için

1.  Menü çubuğunda, **dosya** > **yeni** > **proje**. İletişim kutusu şu şekilde görünmelidir.

     ![Yeni Proje iletişim kutusu](../ide/media/newprojectdialogcallouts.png)
**yeni proje** iletişim kutusu

2.  Seçin ya da **Visual C#** veya **Visual Basic** içinde **yüklü şablonlar** listesi.

3.  Şablonlar listesinde **Windows Forms uygulaması** simgesi. Yeni form adı **pictureviewer olarak**ve ardından **Tamam** düğmesi.

     Visual Studio, programınız için bir çözüm oluşturur. Bir çözüm için tüm projeleri ve dosyaları, programınızın gerek duyduğu bir kapsayıcı görevi görür. Bu kullanım koşullarını, bu öğreticinin ilerleyen bölümlerinde daha ayrıntılı olarak açıklanacaktır.

4.  Artık Visual Studio arabiriminde görmeniz gereken aşağıda gösterilmiştir.

    > [!NOTE]
    >  Pencere düzeniniz tam olarak bu çizim gibi görünmeyebilir. Kesin pencere düzeni, Visual Studio, kullandığınız programlama diline ve diğer etkenlere sürümüne bağlıdır. Ancak, tüm üç pencerenin de görüntülendiğini doğrulamanız gerekir.

     ![IDE penceresi](../ide/media/express_ideoverview_visio.png)
**IDE** penceresi

     Arabirim üç pencere içerir: ana pencere, **Çözüm Gezgini**ve **özellikleri** penceresi.

     Bu pencerelerden biri eksikse, menü çubuğundan seçerek varsayılan pencere düzenini geri **penceresi** > **pencere düzenini Sıfırla**. Windows, menü komutlarını kullanarak da görüntüleyebilirsiniz. Menü çubuğunda, **görünümü** > **Özellikler penceresi** veya **Çözüm Gezgini**. Başka bir pencere açıksa seçerek bunları kapatın **kapatmak** (x), sağ üst köşesinde düğmesini.

5.  Çizim aşağıdaki pencereleri (sol üst köşeden saat yönünde Giden) göstermektedir:

    -   **Ana pencere** Bu pencerede formlarla çalışma ve kod düzenleme gibi işin çoğunu gerçekleştirirsiniz. Çizimde, bir formda pencere gösterir **Form Düzenleyicisi**. Pencerenin üst kısmındaki **başlangıç sayfası** sekmesi ve **Form1.cs [Design]** sekmesi görüntülenir. (Visual Basic içinde sekme adı ile biter. *.vb* yerine *.cs*.)

    -   **Çözüm Gezgini penceresinde** Bu pencerede, görüntüleyebilir ve çözümünüzdeki tüm öğelerine gidin. Bir dosyanın içeriğini seçerseniz **özellikleri** penceresi değişiklikler. Bir kod dosyası açarsanız (sona erdiği içinde *.cs* görselde C# ve *.vb* Visual Basic'te), kod dosyası veya kod dosyası için bir tasarımcı görünür. Bir tasarımcı, düğmeler ve listeler gibi denetimler ileride ekleyebileceğiniz görsel bir yüzeydir. Visual Studio formları için tasarımcı adı verilir **Windows Form Tasarımcısı**.

    -   **Özellikler penceresi** Bu pencerede diğer pencerelerde seçtiğiniz öğelerin özelliklerini değiştirebilirsiniz. Form1 seçerseniz, örneğin, alt başlık ayarlayarak değiştirebileceğiniz **metin** özelliğini değiştirebilirsiniz arka plan rengi ayarlayarak **Backcolor** özelliği.

    > [!NOTE]
    >  Üst satırı **Çözüm Gezgini** gösterir **çözüm 'Pictureviewer olarak' (1 proje)**, Visual Studio çözüm için oluşturduğunuz anlamına gelir. Bir çözüm birden fazla proje içerebilir ancak şu an için yalnızca bir proje içeren çözümlerle çalışacaksınız.

6.  Menü çubuğunda, **dosya** > **Tümünü Kaydet**.

     Alternatif, **Tümünü Kaydet** aşağıdaki çizimin gösterdiği araç çubuğunda düğme.

     ![Tüm araç çubuğu düğmesi Kaydet](../ide/media/express_iconsaveall.png)
**Tümünü Kaydet** araç çubuğu düğmesi

     Visual Studio klasör adını ve proje adını otomatik olarak doldurur ve daha sonra projeyi projeler klasörünüze kaydeder.

## <a name="to-continue-or-review"></a>Devam etmek veya gözden geçirmek için

-   Sonraki öğretici adımına gitmek için bkz: [2. adım: Programınızı çalıştırmak](../ide/step-2-run-your-program.md).

-   Genel Bakış konusuna dönmek için bkz: [öğretici 1: Resim Görüntüleyici oluşturma](../ide/tutorial-1-create-a-picture-viewer.md).

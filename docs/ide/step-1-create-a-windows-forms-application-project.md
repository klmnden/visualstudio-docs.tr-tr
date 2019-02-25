---
title: '1. Adım: Bir Windows Forms uygulaması projesi oluşturma'
ms.date: 01/26/2019
ms.topic: conceptual
ms.assetid: 16ac2422-e720-4e3a-b511-bc2a54201a86
author: TerryGLee
ms.author: tglee
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 2b8552adfd4a7f94c58bcb32a60fbe8cd4c9323b
ms.sourcegitcommit: 1c8e07b98fc0a44b5ab90bcef77d9fac7b3eb452
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/25/2019
ms.locfileid: "56796536"
---
# <a name="step-1-create-a-windows-forms-application-project"></a>1. Adım: Bir Windows Forms uygulaması projesi oluşturma

Resim Görüntüleyici oluşturduğunuzda ilk adım bir Windows Forms Application projesi oluşturmaktır.

 ![video bağlantısı](../data-tools/media/playvideo.gif)bu konunun video sürümü için bkz: [öğretici 1: Visual Basic'te - Video 1 resim görüntüleyici oluşturma](http://go.microsoft.com/fwlink/?LinkId=205209) veya [öğretici 1: İçinde resim görüntüleyici oluşturma C# -Video 1](http://go.microsoft.com/fwlink/?LinkId=205199). Bazı menü komutlarında ve diğer kullanıcı arabirimi öğelerinde küçük farklılıklar olduğundan bu videolarda Visual Studio'nun önceki bir sürümü kullanın. Ancak, kavramlar ve yordamlar benzer şekilde Visual Studio'nun geçerli sürümünde çalışır.

## <a name="to-create-a-windows-forms-application-project"></a>Bir Windows Forms uygulaması projesi oluşturmak için

1. Menü çubuğunda, **dosya** > **yeni** > **proje**. İletişim kutusu şu şekilde görünmelidir.

     ![Yeni Proje iletişim kutusu](../ide/media/newprojectdialogcallouts.png)<br/>
***Yeni proje** iletişim kutusu*

2. Seçin ya da **Visual C#**  veya **Visual Basic** sol tarafındaki **yeni proje** iletişim kutusu.

3. Şablonlar listesinde **Windows Forms uygulaması (.NET Framework)**. Yeni form adı **pictureviewer olarak**ve ardından **Tamam** düğmesi.

    >[!NOTE]
    >Görmüyorsanız **Windows Forms uygulaması (.NET Framework)** şablon, Visual Studio yükleyicisini kullanma **.NET Masaüstü geliştirmesinden** iş yükü.<br/><br/>![.NET masaüstü geliştirme iş yükünü Visual Studio yükleyicisi](../ide/media/dot-net-desktop-dev-workload.png)<br/><br/> Daha fazla bilgi için [Visual Studio 2017'yi yükleme](../install/install-visual-studio.md) sayfası.

     Visual Studio, programınız için bir çözüm oluşturur. Bir çözüm için tüm projeleri ve dosyaları, programınızın gerek duyduğu bir kapsayıcı görevi görür. Bu kullanım koşullarını, bu öğreticinin ilerleyen bölümlerinde daha ayrıntılı olarak açıklanacaktır.

4. Üç windows geliştirme ortamı içerir: ana pencere, **Çözüm Gezgini**ve **özellikleri** penceresi.

     Bu pencerelerden biri eksikse, menü çubuğundan seçerek varsayılan pencere düzenini geri **penceresi** > **pencere düzenini Sıfırla**. Windows, menü komutlarını kullanarak da görüntüleyebilirsiniz. Menü çubuğunda, **görünümü** > **Özellikler penceresi** veya **Çözüm Gezgini**. Başka bir pencere açıksa seçerek bunları kapatın **kapatmak** (x), sağ üst köşesinde düğmesini.

    ::: moniker range="vs-2017"

    - **Ana pencere** Bu pencerede formlarla çalışma ve kod düzenleme gibi işin çoğunu gerçekleştirirsiniz. Ndaki bir forma pencere gösterir **Form Düzenleyicisi**. Pencerenin üst kısmındaki **başlangıç sayfası** sekmesi ve **Form1.cs [Design]** sekmesi görüntülenir. (Visual Basic içinde sekme adı ile biter. *.vb* yerine *.cs*.)

    ::: moniker-end

    ::: moniker range=">=vs-2019"

    - **Ana pencere** Bu pencerede formlarla çalışma ve kod düzenleme gibi işin çoğunu gerçekleştirirsiniz. Ndaki bir forma pencere gösterir **Form Düzenleyicisi**.

    ::: moniker-end

    - **Çözüm Gezgini penceresinde** Bu pencerede, görüntüleyebilir ve çözümünüzdeki tüm öğelerine gidin. Bir dosyanın içeriğini seçerseniz **özellikleri** penceresi değişiklikler. Bir kod dosyası açarsanız (sona erdiği içinde *.cs* görselde C# ve *.vb* Visual Basic'te), kod dosyası veya kod dosyası için bir tasarımcı görünür. Bir tasarımcı, düğmeler ve listeler gibi denetimler ileride ekleyebileceğiniz görsel bir yüzeydir. Visual Studio formları için tasarımcı adı verilir **Windows Form Tasarımcısı**.

    - **Özellikler penceresi** Bu pencerede diğer pencerelerde seçtiğiniz öğelerin özelliklerini değiştirebilirsiniz. Form1 seçerseniz, örneğin, alt başlık ayarlayarak değiştirebileceğiniz **metin** özelliğini değiştirebilirsiniz arka plan rengi ayarlayarak **Backcolor** özelliği.

    > [!NOTE]
    > Üst satırı **Çözüm Gezgini** gösterir **çözüm 'Pictureviewer olarak' (1 proje)**, Visual Studio çözüm için oluşturduğunuz anlamına gelir. Bir çözüm birden fazla proje içerebilir ancak şu an için yalnızca bir proje içeren çözümlerle çalışacaksınız.

6. Menü çubuğunda, **dosya** > **Tümünü Kaydet**.

     Alternatif, **Tümünü Kaydet** aşağıdaki çizimin gösterdiği araç çubuğunda düğme.

     ![Tüm araç çubuğu düğmesi Kaydet](../ide/media/express_iconsaveall.png)<br/>
***Tümünü Kaydet** araç çubuğu düğmesi*

     Visual Studio klasör adını ve proje adını otomatik olarak doldurur ve daha sonra projeyi projeler klasörünüze kaydeder.

## <a name="to-continue-or-review"></a>Devam etmek veya gözden geçirmek için

- Sonraki öğretici adımına gitmek için bkz: [2. adım: Programınızı çalıştırmak](../ide/step-2-run-your-program.md).

- Genel Bakış konusuna dönmek için bkz: [öğretici 1: Resim Görüntüleyici oluşturma](../ide/tutorial-1-create-a-picture-viewer.md).

## <a name="see-also"></a>Ayrıca bkz.

- [Yeni bir Windows formu oluşturma](/dotnet/framework/winforms/creating-a-new-windows-form/)
---
title: '11. Adım: Programınızı çalıştırma ve diğer özellikleri deneme'
ms.date: 11/04/2016
ms.topic: conceptual
ms.assetid: 656614d0-4fe7-4a67-8edc-c10919377d09
author: TerryGLee
ms.author: tglee
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 43cb58c65131b5cc7e01b0f59306761a3b275dc7
ms.sourcegitcommit: 5216c15e9f24d1d5db9ebe204ee0e7ad08705347
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/09/2019
ms.locfileid: "68925921"
---
# <a name="step-11-run-your-program-and-try-other-features"></a>11. Adım: Programınızı çalıştırma ve diğer özellikleri deneme
Programınız tamamlandı ve çalıştırılmaya hazırlanıyor. Programınızı çalıştırabilir ve arka plan rengini <xref:System.Windows.Forms.PictureBox>ayarlayabilirsiniz. Daha fazla bilgi edinmek için, formun rengini değiştirerek, düğmeleri ve onay kutusunu özelleştirerek ve formun özelliklerini değiştirerek programı geliştirmeyi deneyin.

Örneğin tamamlanmış bir sürümünü indirmek için bkz. [tüm resim Görüntüleyici öğreticisi örneği](https://code.msdn.microsoft.com/Complete-Picture-Viewer-7d91d3a8).

![video](../data-tools/media/playvideo.gif)bağlantısı bu konunun video sürümü için bkz [. öğretici 1: Visual Basic-video 5](http://go.microsoft.com/fwlink/?LinkId=205216) veya [öğretici 1 ' de bir resim Görüntüleyicisi oluşturun: Video 5 C# ](http://go.microsoft.com/fwlink/?LinkId=205206)' te bir resim görüntüleyici oluşturun. Bu videolar, Visual Studio 'nun önceki bir sürümünü kullanır, bu nedenle bazı menü komutlarında ve diğer kullanıcı arabirimi öğelerinde küçük farklılıklar vardır. Ancak, kavramlar ve yordamlar Visual Studio 'nun geçerli sürümünde benzer şekilde çalışır.

## <a name="to-run-your-program-and-set-the-background-color"></a>Programınızı çalıştırmak ve arka plan rengini ayarlamak için

1. **F5**' i seçin veya menü çubuğunda Hata **Ayıkla** > **Başlat hata**Ayıkla ' yı seçin.

2. Bir resmi açmadan önce, **arka plan rengini ayarla** düğmesini seçin. **Renk** iletişim kutusu açılır.

     ![Renk iletişim kutusu](../ide/media/express_colordialog.png)
**rengi** iletişim kutusu

3. PictureBox arka plan rengini ayarlamak için bir renk seçin. Nasıl çalıştığını anlamak için `backgroundButton_Click()` yönteme yakından bakın.

    > [!NOTE]
    > URL 'sini **Dosya Aç** iletişim kutusuna yapıştırarak Internet 'ten bir resim yükleyebilirsiniz. Arka plan renginiz görünür olduğundan, saydam bir arka plana sahip bir görüntü bulmaya çalışın.

4. Temizlendiğinden emin olmak için **Resmi Temizle** düğmesini seçin. Sonra, **Kapat** düğmesini seçerek programdan çıkın.

## <a name="to-try-other-features"></a>Diğer özellikleri denemek için

- **BackColor** özelliğini kullanarak formun ve düğmelerin rengini değiştirin.

- **Yazı tipi** ve **ForeColor** özelliklerini kullanarak düğmelerinizi ve onay kutusunu özelleştirin.

- Formunuzun **FormBorderStyle** ve **ControlBox** özelliklerini değiştirin.

- Kullanıcı **ENTER** veya **ESC** tuşunu seçtiğinde düğmelerin otomatik olarak seçilmesi için formunuzun **AcceptButton** ve **CancelButton** özelliklerini kullanın. Kullanıcı **ENTER** ' a tıkladığında **dosyayı aç** iletişim kutusunu açar ve Kullanıcı **ESC**' i seçtiğinde kutuyu kapatır.

## <a name="to-continue-or-review"></a>Devam etmek veya gözden geçirmek için

- Visual Studio 'da programlama hakkında daha fazla bilgi edinmek için bkz. [programlama kavramları](https://msdn.microsoft.com/Library/65c12cca-af4f-4017-886e-2dbc00a189d6).

- Visual Basic hakkında daha fazla bilgi için bkz. [Visual Basic uygulamalar geliştirme](/dotnet/visual-basic/developing-apps/index).

- Görsel C#hakkında daha fazla bilgi edinmek için bkz. [ C# dile giriş ve .NET Framework](/dotnet/csharp/getting-started/introduction-to-the-csharp-language-and-the-net-framework).

- Sonraki öğreticiye gitmek için bkz [. öğretici 2: Süreli bir matematik testi](../ide/tutorial-2-create-a-timed-math-quiz.md)oluşturun.

- Önceki öğretici adımına dönmek için bkz [. adım 10: Ek düğmeler ve onay kutusu](../ide/step-10-write-code-for-additional-buttons-and-a-check-box.md)için kod yazın.

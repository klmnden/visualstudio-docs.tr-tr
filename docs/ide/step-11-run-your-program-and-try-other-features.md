---
title: '11. Adım: Resim görüntüleyici uygulamanızı çalıştırın ve diğer özellikleri deneyin'
ms.date: 09/11/2019
ms.assetid: 656614d0-4fe7-4a67-8edc-c10919377d09
ms.topic: tutorial
ms.prod: visual-studio-windows
ms.technology: vs-ide-general
ms.devlang:
- csharp
- vb
author: TerryGLee
ms.author: tglee
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 4d57852a356b2399a358f1636495e96a3dcec44f
ms.sourcegitcommit: 6993bcb0d2b0067b1b7b7899bfba52c31c70b7e7
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/18/2019
ms.locfileid: "71095326"
---
# <a name="step-11-run-your-picture-viewer-app-and-try-other-features"></a>11. Adım: Resim görüntüleyici uygulamanızı çalıştırın ve diğer özellikleri deneyin

Resim görüntüleyici uygulamanız tamamlandı ve çalıştırılmaya hazırlanıyor. Uygulamanızı çalıştırabilir ve arka plan rengini <xref:System.Windows.Forms.PictureBox>ayarlayabilirsiniz. Daha fazla bilgi edinmek için formun rengini değiştirerek, düğmeleri ve onay kutusunu özelleştirerek ve formun özelliklerini değiştirerek uygulamayı geliştirmeyi deneyin.

## <a name="how-to-run-your-app-and-set-the-background-color"></a>Uygulamanızı çalıştırma ve arka plan rengini ayarlama

1. **F5**' i seçin veya menü çubuğunda Hata **Ayıkla** > **Başlat hata**Ayıkla ' yı seçin.

1. Bir resmi açmadan önce, **arka plan rengini ayarla** düğmesini seçin. **Renk** iletişim kutusu açılır.

     ![Renk iletişim kutusu](../ide/media/express_colordialog.png)<br/>
***Renk*** *iletişim kutusu*

1. PictureBox arka plan rengini ayarlamak için bir renk seçin. Nasıl çalıştığını anlamak için `backgroundButton_Click()` (veya, `BackgroundButton_Click()`) yöntemine yakından bakın.

    > [!NOTE]
    > URL 'sini **Dosya Aç** iletişim kutusuna yapıştırarak Internet 'ten bir resim yükleyebilirsiniz. Arka plan renginiz görünür olduğundan, saydam bir arka plana sahip bir görüntü bulmaya çalışın.

1. Temizlendiğinden emin olmak için **Resmi Temizle** düğmesini seçin. Sonra, **Kapat** düğmesini seçerek uygulamadan çıkın.

## <a name="try-other-features"></a>Diğer özellikleri deneme

* **BackColor** özelliğini kullanarak formun ve düğmelerin rengini değiştirin.

* **Yazı tipi** ve **ForeColor** özelliklerini kullanarak düğmelerinizi ve onay kutusunu özelleştirin.

* Formunuzun **FormBorderStyle** ve **ControlBox** özelliklerini değiştirin.

* Kullanıcı **ENTER** veya **ESC** tuşunu seçtiğinde düğmelerin otomatik olarak seçilmesi için formunuzun **AcceptButton** ve **CancelButton** özelliklerini kullanın. Kullanıcı **ENTER** ' a tıkladığında ve Kullanıcı **ESC**' i seçtiğinde kutuyu kapatdığınızda, uygulamayı **Aç** iletişim kutusunu açın.

## <a name="next-steps"></a>Sonraki adımlar

Daha fazla bilgi edinmek için aşağıdaki öğreticiyle devam edin:

> [!div class="nextstepaction"]
> [Öğretici 2: Süreli matematik testi oluşturma](../ide/tutorial-2-create-a-timed-math-quiz.md)

Önceki öğretici adımına dönmek için bkz [. adım 10: Ek düğmeler ve onay kutusu](../ide/step-10-write-code-for-additional-buttons-and-a-check-box.md)için kod yazın.

## <a name="see-also"></a>Ayrıca bkz.

* [Diğer C# öğreticiler](/visualstudio/get-started/csharp/)
* [Daha fazla Visual Basic öğretici](/visualstudio/get-started/visual-basic/)
* [C++öğreticide](/cpp/get-started/tutorial-console-cpp)

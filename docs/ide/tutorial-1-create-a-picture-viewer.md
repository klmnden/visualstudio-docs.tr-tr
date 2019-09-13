---
title: 'Öğretici 1: Resim görüntüleyici oluşturma'
ms.date: 08/30/2019
ms.assetid: 3071d6df-2b2f-4e95-ab68-bef727323136
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
ms.openlocfilehash: 2c0f867179fd78ecb753a9b66cfbdb8479e16c3b
ms.sourcegitcommit: b60a00ac3165364ee0e53f7f6faef8e9fe59ec4a
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/11/2019
ms.locfileid: "70913265"
---
# <a name="tutorial-1-create-a-picture-viewer"></a>Öğretici 1: Resim görüntüleyici oluşturma

Bu öğreticide, bir dosyadan resim yükleyen ve onu bir pencerede görüntüleyen bir uygulama oluşturacaksınız. Formunuza düğmeler ve resim kutuları gibi denetimleri sürüklemek, özelliklerini ayarlamak ve formu düzgün şekilde yeniden boyutlandırmak için kapsayıcıları kullanmak üzere **Windows Form Tasarımcısı** kullanmayı öğreneceksiniz. Ayrıca kod yazmaya başlayın.

> [!NOTE]
> Bu öğreticide hem görsel C# hem de Visual Basic ele alınmaktadır, bu nedenle kullandığınız programlama diline özgü bilgilere odaklanırsınız.

Bu öğretici aşağıdaki görevlerde size kılavuzluk eder:

* Yeni bir proje oluşturun.

* Bir uygulamayı test etme (hata ayıklama).

* Bir forma onay kutuları ve düğmeler gibi temel denetimleri ekleyin.

* Düzenleri kullanarak bir formdaki denetimleri konumlandırın.

* Bir forma **Açık dosya** ve **renk** iletişim kutuları ekleyin.

* IntelliSense ve kod parçacıkları kullanarak kod yazın.

* Olay işleyicisi yöntemlerini yazın.

Bitirdiğinizde, uygulamanız aşağıdaki görüntüye benzer görünmelidir:

![Bu öğreticide oluşturduğunuz resim görüntüleyici uygulaması](../ide/media/express_pictureviewerdone.png)

## <a name="tutorial-links"></a>Öğretici bağlantıları

|Başlık|Açıklama|
|-----------|-----------------|
|[1. Adım: Windows Forms uygulama projesi oluşturma](../ide/step-1-create-a-windows-forms-application-project.md)|Windows Forms bir uygulama projesi oluşturarak başlayın.|
|[2. Adım: Resim görüntüleyici uygulamanızı çalıştırma](../ide/step-2-run-your-program.md)|Önceki adımda oluşturduğunuz Windows Forms uygulama projesini çalıştırın.|
|[3. Adım: Form özelliklerinizi ayarlama](../ide/step-3-set-your-form-properties.md)|**Özellikler** penceresini kullanarak formunuzun görünme şeklini değiştirin.|
|[4. Adım: TableLayoutPanel denetimi ile formunuzu düzenleme](../ide/step-4-lay-out-your-form-with-a-tablelayoutpanel-control.md)|Formunuza bir `TableLayoutPanel` denetim ekleyin.|
|[5. Adım: Formunuza denetimler ekleme](../ide/step-5-add-controls-to-your-form.md)|Formunuza `PictureBox` Denetim`CheckBox` ve denetim gibi denetimler ekleyin. Formunuza düğmeler ekleyin.|
|[6. Adım: Düğme denetimlerinizi adlandırın](../ide/step-6-name-your-button-controls.md)|Düğmelerinizi daha anlamlı bir şekilde yeniden adlandırın.|
|[7. Adım: Formunuza iletişim kutusu bileşenleri ekleme](../ide/step-7-add-dialog-components-to-your-form.md)|Formunuza bir `OpenFileDialog` bileşen `ColorDialog` ve bileşen ekleyin.|
|[8. Adım: Resim göster düğmesi olay işleyicisi için kod yazma](../ide/step-8-write-code-for-the-show-a-picture-button-event-handler.md)|IntelliSense aracını kullanarak kod yazın.|
|[9. Adım: Kodunuzu gözden geçirin, yorum yapın ve test edin](../ide/step-9-review-comment-and-test-your-code.md)|Kodunuzu gözden geçirin ve test edin. Gerektiğinde Yorumlar ekleyin.|
|[10. Adım: Ek düğmeler ve onay kutusu için kod yazma](../ide/step-10-write-code-for-additional-buttons-and-a-check-box.md)|IntelliSense kullanarak diğer düğmeleri ve onay kutusunu çalışacak şekilde kod yazın.|
|[11. Adım: Uygulamanızı çalıştırın ve diğer özellikleri deneyin](../ide/step-11-run-your-program-and-try-other-features.md)|Uygulamanızı çalıştırın ve arka plan rengini ayarlayın. Renkleri, yazı tiplerini ve kenarlıkları değiştirme gibi diğer özellikleri deneyin.|

## <a name="next-steps"></a>Sonraki adımlar

**Öğreticiye[başlamak için adım 1: Windows Forms bir uygulama projesi](../ide/step-1-create-a-windows-forms-application-project.md)** oluşturun.

## <a name="see-also"></a>Ayrıca bkz.

* [Diğer C# öğreticiler](/visualstudio/get-started/csharp/)
* [Visual Basic öğreticileri](/visualstudio/get-started/visual-basic/)
* [C++izleyin](../ide/getting-started-with-cpp-in-visual-studio.md)

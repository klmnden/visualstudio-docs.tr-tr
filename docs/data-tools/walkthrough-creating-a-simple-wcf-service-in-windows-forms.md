---
title: "İzlenecek yol: Windows Forms'ta basit bir WCF hizmeti oluşturma"
ms.date: 11/04/2016
ms.topic: conceptual
dev_langs:
- VB
- CSharp
helpviewer_keywords:
- WCF, walkthrough [Visual Studio]
- WCF, Visual Studio tools for
- WCF services
- WCF services, walkthrough
ms.assetid: 5fef1a64-27a4-4f10-aa57-29023e28a2d6
author: gewarren
ms.author: gewarren
manager: jillfra
ms.workload:
- data-storage
ms.openlocfilehash: 64d5ce818e44f3bf4b0844d4a6fbd25e922a33d7
ms.sourcegitcommit: 5af29226aef0a3b4a506b69a08a97cfd21049521
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/20/2019
ms.locfileid: "58268589"
---
# <a name="walkthrough-create-a-simple-wcf-service-in-windows-forms"></a>İzlenecek yol: Windows Forms'ta basit bir WCF hizmeti oluşturma

Bu izlenecek yol basit bir Windows Communication Foundation (WCF) hizmet oluşturma, test etmesine ve ardından bir Windows Forms uygulamasından erişmek nasıl gösterir.

[!INCLUDE[note_settings_general](../data-tools/includes/note_settings_general_md.md)]

## <a name="create-a-service"></a>Bir hizmet oluşturma

1. Visual Studio'yu açın.

::: moniker range="vs-2017"

2. Üzerinde **dosya** menüsünde seçin **yeni** > **proje**.

3. İçinde **yeni proje** iletişim kutusunda **Visual Basic** veya **Visual C#**  düğümünü seçip **WCF** çizgidir**WCF hizmet Kitaplığı**.

4. Tıklayın **Tamam** projeyi oluşturmak için.

   ![WCF hizmet kitaplığı projesi](../data-tools/media/wcf1.png)

::: moniker-end

::: moniker range=">=vs-2019"

2. Pencerenin başlangıç seçin **yeni bir proje oluşturma**.

3. Tür **wcf hizmet Kitaplığı** arama kutusuna **yeni bir proje oluşturma** sayfası. Şunlardan birini seçin C# veya Visual Basic şablonu **WCF hizmet Kitaplığı**ve ardından **sonraki**.

   ![Visual Studio 2019 içinde yeni bir WCF hizmet kitaplığı projesi oluşturun](media/vs-2019/create-new-wcf-service-library.png)

   > [!TIP]
   > Şablonlardan görmüyorsanız yüklemeniz gerekebilir **Windows Communication Foundation** Visual Studio bileşen. Seçin **daha fazla araçları ve özellikleri yükleme** Visual Studio Yükleyicisi'ni açın. Seçin **tek tek bileşenler** sekmesinde, aşağı kaydırarak **geliştirme etkinliklerini**ve ardından **Windows Communication Foundation**. Tıklayın **değiştirme**.

4. Üzerinde **yeni projenizi yapılandırın** sayfasında **Oluştur**.

::: moniker-end

   > [!NOTE]
   > Bu, test ve erişilen bir çalışma hizmet oluşturur. Aşağıdaki iki adımı farklı bir veri türü kullanılacak varsayılan yöntemini nasıl değişiklik yapabileceğiniz gösterir. Gerçek bir uygulamada hizmete kendi işlevlerinizi eklersiniz.

5. İçinde **Çözüm Gezgini**, çift **Iservice1.vb** veya **Iservice1.cs**.

   ![Iservice1 dosyası](../data-tools/media/wcf2.png)

   Şu satırı bulun:

   [!code-csharp[WCFWalkthrough#4](../data-tools/codesnippet/CSharp/walkthrough-creating-a-simple-wcf-service-in-windows-forms_1.cs)]
   [!code-vb[WCFWalkthrough#4](../data-tools/codesnippet/VisualBasic/walkthrough-creating-a-simple-wcf-service-in-windows-forms_1.vb)]

   Değişiklik türü için `value` dize parametresi:

   [!code-csharp[WCFWalkthrough#1](../data-tools/codesnippet/CSharp/walkthrough-creating-a-simple-wcf-service-in-windows-forms_2.cs)]
   [!code-vb[WCFWalkthrough#1](../data-tools/codesnippet/VisualBasic/walkthrough-creating-a-simple-wcf-service-in-windows-forms_2.vb)]

   Yukarıdaki kodda Not `<OperationContract()>` veya `[OperationContract]` öznitelikleri. Bu öznitelik hizmet tarafından sunulan herhangi bir yöntem için gerekli değildir.

6. İçinde **Çözüm Gezgini**, çift **Service1.vb** veya **Service1.cs**.

   ![Service1 dosyası](../data-tools/media/wcf3.png)

   Şu satırı bulun:

   [!code-vb[WCFWalkthrough#5](../data-tools/codesnippet/VisualBasic/walkthrough-creating-a-simple-wcf-service-in-windows-forms_3.vb)]
   [!code-csharp[WCFWalkthrough#5](../data-tools/codesnippet/CSharp/walkthrough-creating-a-simple-wcf-service-in-windows-forms_3.cs)]

   Değişiklik türü için `value` dize parametresi:

   [!code-csharp[WCFWalkthrough#2](../data-tools/codesnippet/CSharp/walkthrough-creating-a-simple-wcf-service-in-windows-forms_4.cs)]
   [!code-vb[WCFWalkthrough#2](../data-tools/codesnippet/VisualBasic/walkthrough-creating-a-simple-wcf-service-in-windows-forms_4.vb)]

## <a name="test-the-service"></a>Hizmeti test etme

1. Tuşuna **F5** hizmeti çalıştırmak için. A **WCF Test istemcisi** form görünür ve hizmeti yükler.

2. İçinde **WCF Test istemcisi** formunda, çift **GetData()** altındaki yöntemin **Iservice1**. **GetData** sekmesi görünür.

     ![GetData&#40; &#41; yöntemi](../data-tools/media/wcf4.png)

3. İçinde **istek** kutusunda **değer** alan ve tür `Hello`.

     ![Değer alanı](../data-tools/media/wcf5.png)

4. Tıklayın **Invoke** düğmesi. Varsa bir **Güvenlik Uyarısı** iletişim kutusu görüntülendikten sonra **Tamam**. Sonuç görüntüler **yanıt** kutusu.

     ![Yanıt kutusunda sonucu](../data-tools/media/wcf6.png)

5. Üzerinde **dosya** menüsünde tıklatın **çıkış** test formu kapatmak için.

## <a name="access-the-service"></a>Hizmete erişim

### <a name="reference-the-wcf-service"></a>WCF hizmeti başvurusu

1. Üzerinde **dosya** menüsünde **Ekle** ve ardından **yeni proje**.

2. İçinde **yeni proje** iletişim kutusunda **Visual Basic** veya **Visual C#** düğümünü **Windows**ve ardından  **Windows Forms uygulamalarındaki**. Tıklayın **Tamam** projeyi açmak için.

     ![Windows Forms uygulaması projesi](../data-tools/media/wcf7.png)

3. Sağ **WindowsApplication1** tıklatıp **hizmet Başvurusu Ekle**. **Hizmet Başvurusu Ekle** iletişim kutusu görüntülenir.

4. İçinde **hizmet Başvurusu Ekle** iletişim kutusu, tıklayın **bulma**.

     ![Hizmet Başvurusu Ekle iletişim kutusu](../data-tools/media/wcf8.png)

     **Service1** görüntüler **Hizmetleri** bölmesi.

5. Tıklayın **Tamam** hizmet başvurusu eklemek için.

### <a name="build-a-client-application"></a>İstemci uygulaması oluşturma

1. İçinde **Çözüm Gezgini**, çift **Form1.vb** veya **Form1.cs** Windows Form Tasarımcısı zaten açık değilse açın.

2. Gelen **araç kutusu**, sürükleyin bir `TextBox` denetimi, bir `Label` denetimi ve bir `Button` forma denetim.

     ![Formu için denetimler ekleme](../data-tools/media/wcf9.png)

3. Çift `Button`ve aşağıdaki kodu ekleyin `Click` olay işleyicisi:

     [!code-csharp[WCFWalkthrough#3](../data-tools/codesnippet/CSharp/walkthrough-creating-a-simple-wcf-service-in-windows-forms_5.cs)]
     [!code-vb[WCFWalkthrough#3](../data-tools/codesnippet/VisualBasic/walkthrough-creating-a-simple-wcf-service-in-windows-forms_5.vb)]

4. İçinde **Çözüm Gezgini**, sağ **WindowsApplication1** tıklatıp **başlangıç projesi olarak ayarla**.

5. Tuşuna **F5** projeyi çalıştırın. Bir metin girin ve düğmeye tıklayın. Etiket görüntüler "girdiniz:", girdiğiniz metni gösterir.

     ![Formun sonucu gösteriliyor](../data-tools/media/wcf10.png)

## <a name="see-also"></a>Ayrıca bkz.

- [Visual Studio'da Windows Communication Foundation Hizmetleri ve WCF Veri Hizmetleri](../data-tools/windows-communication-foundation-services-and-wcf-data-services-in-visual-studio.md)
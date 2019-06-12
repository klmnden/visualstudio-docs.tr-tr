---
title: .NET Framework 4 ve 4.5 güncelleştirme Outlook projelerindeki form bölgelerini geçişi
ms.date: 02/02/2017
ms.topic: conceptual
dev_langs:
- VB
- CSharp
helpviewer_keywords:
- Office projects [Office development in Visual Studio], migrating to .NET Framework 4
author: John-Hart
ms.author: johnhart
manager: jillfra
ms.workload:
- office
ms.openlocfilehash: e7e300cd9f6f7d631a029310b01fbfdad7cb4686
ms.sourcegitcommit: cc5fd59e5dc99181601b7db8b28d7f8a83a36bab
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/11/2019
ms.locfileid: "66836054"
---
# <a name="update-form-regions-in-outlook-projects-that-you-migrate-to-the-net-framework-4-or-the-net-framework-45"></a>.NET Framework 4 veya .NET Framework 4.5 için geçirdiğiniz Outlook projelerindeki form bölgelerini güncelleştirme
  Outlook VSTO eklenti projesinde bir form bölgesi hedef Framework'ü değiştirilirse [!INCLUDE[net_v40_short](../sharepoint/includes/net-v40-short-md.md)] veya daha sonra oluşturulan form bölge kodu ve çalışma zamanında belirli form bölgelerini başlatan kodlar için bazı değişiklikler yapmalısınız.

## <a name="update-the-generated-form-region-code"></a>Oluşturulan form bölgesi kodunu güncelleştirme
 Projenin hedef çerçevesi için değişip değişmediğini [!INCLUDE[net_v40_short](../sharepoint/includes/net-v40-short-md.md)] veya daha sonra oluşturulan form bölgesi kodunu değiştirmeniz gerekir. Yaptığınız değişiklikler, Visual Studio ve form bölgelerindeki Outlook'tan alınan tasarlanan form bölgeleri için farklıdır. Bu tür bir form bölgeleri arasındaki farklar hakkında daha fazla bilgi için bkz. [oluşturma Outlook form bölgeleri](../vsto/creating-outlook-form-regions.md).

### <a name="to-update-the-generated-code-for-a-form-region-that-you-designed-in-visual-studio"></a>Visual Studio'da tasarlanan form bölgesini için üretilen kod güncelleştirmek için

1. Form bölgesi arka plan kod dosyası Kod Düzenleyicisi'nde açın. Bu dosya adlı *YourFormRegion*. Designer.cs veya *YourFormRegion*. Designer.vb olarak adlandırılır. Bu dosya Visual Basic projelerinde görmek için tıklayın **tüm dosyaları göster** düğmesine **Çözüm Gezgini**.

2. Öğesinden türetilen form bölgesi sınıf bildirimini değiştirin <xref:Microsoft.Office.Tools.Outlook.FormRegionBase> yerine `Microsoft.Office.Tools.Outlook.FormRegionControl`.

3. Form bölgesi sınıfının oluşturucusu, aşağıdaki kod örnekte gösterildiği gibi değiştirin.

     Aşağıdaki kod örneği, bir form bölgesi sınıfının oluşturucusu, bir projede hedefleyen .NET Framework 3.5 gösterir.

    ```vb
    Public Sub New(ByVal formRegion As Microsoft.Office.Interop.Outlook.FormRegion)
        MyBase.New(formRegion)
        Me.InitializeComponent()
    End Sub
    ```

    ```csharp
    public FormRegion1(Microsoft.Office.Interop.Outlook.FormRegion formRegion)
        : base(formRegion)
    {
        this.InitializeComponent();
    }
    ```

     Aşağıdaki kod örneği bir form bölgesi sınıfının oluşturucusu, bir projede hedefleyen gösterilmektedir [!INCLUDE[net_v40_short](../sharepoint/includes/net-v40-short-md.md)].

    ```vb
    Public Sub New(ByVal formRegion As Microsoft.Office.Interop.Outlook.FormRegion)
        MyBase.New(Globals.Factory, formRegion)
        Me.InitializeComponent()
    End Sub
    ```

    ```csharp
    public FormRegion1(Microsoft.Office.Interop.Outlook.FormRegion formRegion)
        : base(Globals.Factory, formRegion)
    {
        this.InitializeComponent();
    }
    ```

4. Değişiklik imzası `InitializeManifest` aşağıda gösterildiği gibi yöntemi. Yöntemindeki kodu değiştirmeyin emin olun; Bu kod, Tasarımcı içinde uygulanan form bölgesi ayarlarını temsil eder. Görselde C# projeleri adlı bölgeyi genişletmeniz gerekir `Form Region Designer generated code` bu yöntem görmek için.

     Aşağıdaki kod örneği imzası gösterilmektedir `InitializeManifest` yöntem .NET Framework 3. 5'i hedefleyen bir proje.

    ```vb
    Private Shared Sub InitializeManifest(ByVal manifest As Microsoft.Office.Tools.Outlook.FormRegionManifest)

        ' Do not change code in this method.
    End Sub
    ```

    ```csharp
    private static void InitializeManifest(Microsoft.Office.Tools.Outlook.FormRegionManifest manifest)
    {
        // Do not change code in this method.
    }
    ```

     Aşağıdaki kod örneği imzası gösterilmektedir `InitializeManifest` hedefleyen bir projeye yönteminde [!INCLUDE[net_v40_short](../sharepoint/includes/net-v40-short-md.md)].

    ```vb
    Private Shared Sub InitializeManifest(ByVal manifest As Microsoft.Office.Tools.Outlook.FormRegionManifest,
        ByVal factory As Microsoft.Office.Tools.Outlook.Factory)

        ' Do not change code in this method.
    End Sub
    ```

    ```csharp
    private static void InitializeManifest(Microsoft.Office.Tools.Outlook.FormRegionManifest manifest,
        Microsoft.Office.Tools.Outlook.Factory factory)
    {
        // Do not change code in this method.
    }
    ```

5. Yeni bir Outlook Form bölgesi öğe projenize ekleyin. Yeni form bölgesi için arka plan kod dosyası açmanız, *YourNewFormRegion* `Factory` ve `WindowFormRegionCollection` dosyasında, sınıfları ve bu sınıflar panoya kopyalayın.

6. Projenize eklediğiniz yeni form bölgesi silin.

7. Yeniden hedeflenen projedeki iş güncelleştirmekte olduğunuz form bölgesi arka plan kod dosyasında *YourOriginalFormRegion* `Factory` ve `WindowFormRegionCollection` sınıfları ve bunları kopyalama kod ile değiştirin Yeni form bölgesi.

8. İçinde *YourNewFormRegion* `Factory` ve `WindowFormRegionCollection` sınıfları aramak için tüm başvuruları *YourNewFormRegion* sınıfı ve her referansını değiştirme  *YourOriginalFormRegion* bunun yerine sınıf. Örneğin, form bölgesini güncelleştirme yapıyorsanız adlı `SalesDataFormRegion` ve 5. adımda oluşturduğunuz yeni form bölgesi adlı `FormRegion1`, tüm başvuruları değiştirme `FormRegion1` için `SalesDataFormRegion`.

#### <a name="to-update-the-generated-code-for-a-form-region-that-you-imported-from-outlook"></a>Form bölgesini Outlook uygulamasından alınan için üretilen kod güncelleştirmek için

1. Form bölgesi arka plan kod dosyası Kod Düzenleyicisi'nde açın. Bu dosya adlı *YourFormRegion*. Designer.cs veya *YourFormRegion*. Designer.vb olarak adlandırılır. Bu dosya Visual Basic projelerinde görmek için tıklayın **tüm dosyaları göster** düğmesine **Çözüm Gezgini**.

2. Öğesinden türetilen form bölgesi sınıf bildirimini değiştirin <xref:Microsoft.Office.Tools.Outlook.ImportedFormRegionBase> yerine `Microsoft.Office.Tools.Outlook.ImportedFormRegion`.

3. Form bölgesi sınıfının oluşturucusu, aşağıdaki kod örnekte gösterildiği gibi değiştirin.

     Aşağıdaki kod örneği, bir form bölgesi sınıfının oluşturucusu, bir projede hedefleyen .NET Framework 3.5 gösterir.

    ```vb
    Public Sub New(ByVal formRegion As Microsoft.Office.Interop.Outlook.FormRegion)
        MyBase.New(formRegion)
    End Sub
    ```

    ```csharp
    public ImportedFormRegion1(Microsoft.Office.Interop.Outlook.FormRegion formRegion)
        : base(formRegion)
    {
        this.FormRegionShowing += new System.EventHandler(this.TaskFormRegion_FormRegionShowing);
        this.FormRegionClosed += new System.EventHandler(this.TaskFormRegion_FormRegionClosed);
    }
    ```

     Aşağıdaki kod örneği bir form bölgesi sınıfı Oluşturucu imzasının hedefleyen bir proje gösterilmektedir [!INCLUDE[net_v40_short](../sharepoint/includes/net-v40-short-md.md)].

    ```vb
    Public Sub New(ByVal formRegion As Microsoft.Office.Interop.Outlook.FormRegion)
        MyBase.New(Globals.Factory, formRegion)
    End Sub
    ```

    ```csharp
    public ImportedFormRegion1(Microsoft.Office.Interop.Outlook.FormRegion formRegion)
        : base(Globals.Factory, formRegion)
    {
        this.FormRegionShowing += new System.EventHandler(this.TaskFormRegion_FormRegionShowing);
        this.FormRegionClosed += new System.EventHandler(this.TaskFormRegion_FormRegionClosed);
    }
    ```

4. Her kod satırı için `InitializeControls` aşağıda gösterildiği gibi başlatan bir denetimde bir form bölgesi sınıfı yöntemi kodu değiştirin.

     Aşağıdaki kod örneği bir projedeki bir denetimi başlatmak .NET Framework 3.5 hedefleyen gösterilmektedir. Bu kodda, `GetFormRegionControl` yöntemi döndürülen denetim türünü belirten bir tür parametresi vardır.

    ```vb
    Me.olkTextBox1 = Me.GetFormRegionControl(Of Microsoft.Office.Interop.Outlook.OlkTextBox)("OlkTextBox1")
    ```

    ```csharp
    this.olkTextBox1 = this.GetFormRegionControl<Microsoft.Office.Interop.Outlook.OlkTextBox>("OlkTextBox1");
    ```

     Aşağıdaki kod örneği bir projedeki bir denetimi başlatmak hedefleyen gösterilmektedir [!INCLUDE[net_v40_short](../sharepoint/includes/net-v40-short-md.md)]. Bu kodda, <xref:Microsoft.Office.Tools.Outlook.ImportedFormRegionBase.GetFormRegionControl%2A> yöntemi, bir tür parametresi yok. Dönüş değeri, başlattığınız denetim türü için dönüştürmeniz gerekir.

    ```vb
    Me.olkTextBox1 = CType(GetFormRegionControl("OlkTextBox1"), Microsoft.Office.Interop.Outlook.OlkTextBox)
    ```

    ```csharp
    this.olkTextBox1 = (Microsoft.Office.Interop.Outlook.OlkTextBox)GetFormRegionControl("OlkTextBox1");
    ```

5. Yeni bir Outlook Form bölgesi öğe projenize ekleyin. Yeni form bölgesi için arka plan kod dosyası açmanız, *YourNewFormRegion* `Factory` ve `WindowFormRegionCollection` dosyasında, sınıfları ve bu sınıflar panoya kopyalayın.

6. Projenize eklediğiniz yeni form bölgesi silin.

7. Yeniden hedeflenen projedeki iş güncelleştirmekte olduğunuz form bölgesi arka plan kod dosyasında *YourOriginalFormRegion* `Factory` ve `WindowFormRegionCollection` sınıfları ve bunları kopyalama kod ile değiştirin Yeni form bölgesi.

8. İçinde *YourNewFormRegion* `Factory` ve `WindowFormRegionCollection` sınıfları aramak için tüm başvuruları *YourNewFormRegion* sınıfı ve her referansını değiştirme  *YourOriginalFormRegion* bunun yerine sınıf. Örneğin, form bölgesini güncelleştirme yapıyorsanız adlı `SalesDataFormRegion` ve 5. adımda oluşturduğunuz yeni form bölgesi adlı `FormRegion1`, tüm başvuruları değiştirme `FormRegion1` için `SalesDataFormRegion`.

## <a name="instantiate-form-region-classes"></a>Form bölgesi sınıflarını örneği
 Dinamik olarak belirli bir form bölgesi sınıflarını başlatır herhangi bir kodu değiştirmeniz gerekir. .NET Framework 3. 5'i hedefleyen projelerde form bölgesi sınıflarını gibi örneği oluşturabilir `Microsoft.Office.Tools.Outlook.FormRegionManifest` doğrudan. ' İ hedefleyen projelerde [!INCLUDE[net_v40_short](../sharepoint/includes/net-v40-short-md.md)] ya da daha sonra bu sınıflar arabirimleri doğrudan örneği oluşturulamıyor.

 Hedef Çerçeve proje değiştirilirse [!INCLUDE[net_v40_short](../sharepoint/includes/net-v40-short-md.md)] veya tarafından sağlanan yöntemleri kullanarak arabirimler daha sonra oluşturmalıdır `Globals.Factory` özelliği. Hakkında daha fazla bilgi için `Globals.Factory` özelliğine bakın [Office projelerindeki nesnelere genel erişim](../vsto/global-access-to-objects-in-office-projects.md).

 Form bölgesi türleri aşağıdaki tabloda listelenmekte ve türleri örneklemek için kullanılacak yöntemi hedefleyen projeleri [!INCLUDE[net_v40_short](../sharepoint/includes/net-v40-short-md.md)] veya üzeri.

|Tür|Kullanılacak Üreteç yöntemi|
|----------|---------------------------|
|<xref:Microsoft.Office.Tools.Outlook.FormRegionCustomAction>|<xref:Microsoft.Office.Tools.Outlook.Factory.CreateFormRegionCustomAction%2A>|
|<xref:Microsoft.Office.Tools.Outlook.FormRegionInitializingEventArgs>|<xref:Microsoft.Office.Tools.Outlook.Factory.CreateFormRegionInitializingEventArgs%2A>|
|<xref:Microsoft.Office.Tools.Outlook.FormRegionManifest>|<xref:Microsoft.Office.Tools.Outlook.Factory.CreateFormRegionManifest%2A>|

## <a name="see-also"></a>Ayrıca bkz.
- [Office çözümlerini .NET Framework 4 veya sonraki sürümlere geçirme](../vsto/migrating-office-solutions-to-the-dotnet-framework-4-or-later.md)
- [Outlook form bölgeleri oluşturma](../vsto/creating-outlook-form-regions.md)

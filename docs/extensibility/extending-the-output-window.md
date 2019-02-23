---
title: Çıkış penceresini genişletme | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
helpviewer_keywords:
- Output window, about Output window
ms.assetid: b02fa88c-f92a-4ff6-ba5f-2eb4d48a643a
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: 03e7cb1a462c79f498687296afd8c64accfc1458
ms.sourcegitcommit: b0d8e61745f67bd1f7ecf7fe080a0fe73ac6a181
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/22/2019
ms.locfileid: "56706216"
---
# <a name="extend-the-output-window"></a>Çıkış penceresini genişletme
**Çıkış** penceresinde okuma/yazma metin bölmelerinin bir kümesidir. Visual Studio, bu yerleşik bölmeler sahiptir: **Derleme**, hangi projelerinde yapılar hakkındaki iletileri iletişim kurmak ve **genel**, hangi [!INCLUDE[vsprvs](../code-quality/includes/vsprvs_md.md)] iletileri IDE hakkında iletişim kurar. Projeleri, bir başvuru alma **derleme** bölmesinde otomatik olarak ile <xref:Microsoft.VisualStudio.Shell.Interop.IVsBuildableProjectCfg> arabirim yöntemleri ve Visual Studio, doğrudan erişim sunar **genel** bölmesi aracılığıyla <xref:Microsoft.VisualStudio.Shell.Interop.SVsGeneralOutputWindowPane> hizmeti. Ek olarak yerleşik bölmeler, oluşturabilir ve kendi özel bölmeleri yönetin.

 Denetleyebileceğiniz **çıkış** penceresini doğrudan aracılığıyla <xref:Microsoft.VisualStudio.Shell.Interop.IVsOutputWindow> ve <xref:Microsoft.VisualStudio.Shell.Interop.IVsOutputWindowPane> arabirimleri. <xref:Microsoft.VisualStudio.Shell.Interop.IVsOutputWindow> Tarafından sunulan arabirimi <xref:Microsoft.VisualStudio.Shell.Interop.SVsOutputWindow> hizmet, oluşturmaya, almaya ve yok etme için yöntemleri tanımlar **çıkış** pencere bölmeleri. <xref:Microsoft.VisualStudio.Shell.Interop.IVsOutputWindowPane> Arabirimi bölmelerini gösterme, bölmelerini gizleme ve metin işlemek için yöntemleri tanımlar. Denetlemeye yönelik alternatif bir yolu **çıkış** penceredir aracılığıyla <xref:EnvDTE.OutputWindow> ve <xref:EnvDTE.OutputWindowPane> Visual Studio Otomasyon nesne modelindeki nesneler. Bu nesneler neredeyse tüm işlevselliğini kapsülleyen <xref:Microsoft.VisualStudio.Shell.Interop.IVsOutputWindow> ve <xref:Microsoft.VisualStudio.Shell.Interop.IVsOutputWindowPane> arabirimleri. Ayrıca, <xref:EnvDTE.OutputWindow> ve <xref:EnvDTE.OutputWindowPane> nesneleri numaralandırır daha kolay hale getirmek için daha yüksek düzeydeki bazı işlevler eklemek **çıkış** pencere bölmeleri ve metin bölmeden alınacak.

## <a name="create-an-extension-that-uses-the-output-pane"></a>Çıkış Bölmesi ' kullanan bir uzantı oluşturma
 Çıkış bölmesinde farklı yönlerini sınayan bir uzantı yapabilirsiniz.

1.  Adlı bir VSIX projesi oluşturun `TestOutput` bir menü komutuyla adlı **TestOutput**. Daha fazla bilgi için [bir menü komutuyla uzantı oluşturma](../extensibility/creating-an-extension-with-a-menu-command.md).

2.  Aşağıdaki başvuruları ekleyin:

    1.  EnvDTE

    2.  EnvDTE80

3.  İçinde *TestOutput.cs*, aşağıdaki using deyimi:

    ```f#
    using EnvDTE;
    using EnvDTE80;
    ```

4.  İçinde *TestOutput.cs*, silme `ShowMessageBox` yöntemi. Aşağıdaki metot taslağı ekleyin:

    ```csharp
    private void OutputCommandHandler(object sender, EventArgs e)
    {
    }
    ```

5.  TestOutput oluşturucusunun içinde komut işleyici OutputCommandHandler için değiştirin. Komutları ekler bölümü aşağıda verilmiştir:

    ```csharp
    OleMenuCommandService commandService = this.ServiceProvider.GetService(typeof(IMenuCommandService)) as OleMenuCommandService;
    if (commandService != null)
    {
        CommandID menuCommandID = new CommandID(MenuGroup, CommandId);
        EventHandler eventHandler = OutputCommandHandler;
        MenuCommand menuItem = new MenuCommand(eventHandler, menuCommandID);
        commandService.AddCommand(menuItem);
    }
    ```

6.  Aşağıdaki bölümlerde, çıkış bölmesine uğraşmanızı farklı şekillerde gösterir farklı yöntemleri vardır. Body bu yöntemleri çağırabilirsiniz `OutputCommandHandler()` yöntemi. Örneğin, aşağıdaki kodu ekler `CreatePane()` sonraki bölümde verilen yöntemi.

    ```csharp
    private void OutputCommandHandler(object sender, EventArgs e)
    {
        CreatePane(new Guid(), "Created Pane", true, false);
    }
    ```

## <a name="create-an-output-window-with-ivsoutputwindow"></a>IVsOutputWindow ile bir çıkış penceresi oluştur
 Bu örnek, yeni bir oluşturma işlemi gösterilmektedir **çıkış** kullanarak pencere bölmesi <xref:Microsoft.VisualStudio.Shell.Interop.IVsOutputWindow> arabirimi.

```csharp
void CreatePane(Guid paneGuid, string title,
    bool visible, bool clearWithSolution)
{
    IVsOutputWindow output =
        (IVsOutputWindow)GetService(typeof(SVsOutputWindow));
    IVsOutputWindowPane pane;

    // Create a new pane.
    output.CreatePane(
        ref paneGuid,
        title,
        Convert.ToInt32(visible),
        Convert.ToInt32(clearWithSolution));

    // Retrieve the new pane.
    output.GetPane(ref paneGuid, out pane);

     pane.OutputString("This is the Created Pane \n");
}
```

 Bu yöntem uzantıya'a tıkladığınızda önceki bölümde verilen eklerseniz **çağırma TestOutput** görmeniz komutu **çıkış** bildiren bir başlık penceresiyle **çıktıyı Göster Kaynak: CreatedPane** ve sözcükler **oluşturulan bölmesinde budur** bölmesinde.

## <a name="create-an-output-window-with-outputwindow"></a>OutputWindow ile bir çıkış penceresi oluştur
 Bu örnek nasıl oluşturulacağını gösterir. bir **çıkış** kullanarak pencere bölmesi <xref:EnvDTE.OutputWindow> nesne.

```csharp
void CreatePane(string title)
{
    DTE2 dte = (DTE2)GetService(typeof(DTE));
    OutputWindowPanes panes =
        dte.ToolWindows.OutputWindow.OutputWindowPanes;

    try
    {
        // If the pane exists already, write to it.
        panes.Item(title);
    }
    catch (ArgumentException)
    {
        // Create a new pane and write to it.
        panes.Add(title);
    }
}
```

 Ancak <xref:EnvDTE.OutputWindowPanes> alma koleksiyonu sağlar bir **çıkış** pencere bölmesi başlığı tarafından bölmesinde başlıkları garanti edilmez benzersiz olmalıdır. Bir başlık benzersizliğini doubt kullanırsanız <xref:Microsoft.VisualStudio.Shell.Interop.IVsOutputWindow.GetPane%2A> GUID'sine doğru bölmede almak için yöntemi.

 Bu yöntem uzantıya'a tıkladığınızda önceki bölümde verilen eklerseniz **çağırma TestOutput** olan çıkış penceresine bildiren bir başlık görmeniz komut **çıktıyı göster: DTEPane** ve sözcükler **eklenen DTE bölmesinde** bölmesinde.

## <a name="delete-an-output-window"></a>Çıkış penceresi Sil
 Bu örnek nasıl sileceğiniz gösterilmektedir bir **çıkış** pencere bölmesi.

```csharp
void DeletePane(Guid paneGuid)
{
    IVsOutputWindow output =
    (IVsOutputWindow)ServiceProvider.GetService(typeof(SVsOutputWindow));

    IVsOutputWindowPane pane;
    output.GetPane(ref paneGuid, out pane);

    if (pane == null)
    {
        CreatePane(paneGuid, "New Pane\n", true, true);
    }
     else
    {
        output.DeletePane(ref paneGuid);
    }
}
```

 Bu yöntem uzantıya'a tıkladığınızda önceki bölümde verilen eklerseniz **çağırma TestOutput** olan çıkış penceresine bildiren bir başlık görmeniz komut **çıktıyı göster: Yeni bir bölme** ve sözcükler **oluşturulan bölmesinde eklenen** bölmesinde. Tıklarsanız **çağırma TestOutput** bölmesinde silinip yeniden komutu.

## <a name="get-the-general-pane-of-the-output-window"></a>Çıkış penceresi genel bölmesi
 Bu örnek, yerleşik alınacağı gösterilmektedir **genel** bölmesinde **çıkış** penceresi.

```csharp
IVsOutputWindowPane GetGeneralPane()
{
    return (IVsOutputWindowPane)GetService(
        typeof(SVsGeneralOutputWindowPane));
}
```

 Bu yöntem uzantıya'a tıkladığınızda önceki bölümde verilen eklerseniz **çağırma TestOutput** komutu, görmeniz **çıkış** penceresi sözcükleri gösterir **bulunan genel bölmesinde** bölmesinde.

## <a name="get-the-build-pane-of-the-output-window"></a>Çıkış penceresi derleme bölmesi
 Bu örnek nasıl bulunacağını gösterir **derleme** bölmesi ve ona yazma. Bu yana **derleme** bölmesinde, varsayılan olarak etkin değildir, bu da etkinleştirir.

```csharp
void OutputTaskItemStringExExample(string buildMessage)
{
    EnvDTE80.DTE2 dte = (EnvDTE80.DTE2)ServiceProvider.GetService(typeof(EnvDTE.DTE));

    EnvDTE.OutputWindowPanes panes =
        dte.ToolWindows.OutputWindow.OutputWindowPanes;
    foreach (EnvDTE.OutputWindowPane pane in panes)
        {
            if (pane.Name.Contains("Build"))
            {
                pane.OutputString(buildMessage + "\n");
                pane.Activate();
                return;
             }
        }
}
```

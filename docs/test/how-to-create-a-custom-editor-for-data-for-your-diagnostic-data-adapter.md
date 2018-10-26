---
title: Özel tanılama veri bağdaştırıcısı için veri Düzenleyicisi Visual Studio'nun içinde oluşturun.
ms.date: 10/19/2016
ms.topic: conceptual
helpviewer_keywords:
- Diagnostic Data Adapter, creating custom editor
ms.assetid: 24970227-d1ea-4f6d-9839-e911478848ba
author: gewarren
ms.author: gewarren
manager: douge
ms.prod: visual-studio-dev15
ms.technology: vs-ide-test
ms.openlocfilehash: 41008d1c2808a5a6e6428670a3e7dbbf1041caee
ms.sourcegitcommit: 240c8b34e80952d00e90c52dcb1a077b9aff47f6
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/23/2018
ms.locfileid: "49819345"
---
# <a name="how-to-create-a-custom-editor-for-data-for-your-diagnostic-data-adapter"></a>Nasıl yapılır: tanılama veri bağdaştırıcınızın verileri için özel bir düzenleyici oluşturma

Tanılama veri bağdaştırıcısı oluşturduğunuzda, özel tanılama veri bağdaştırıcınız test ayarları için seçildiğinde belirli verileri yapılandırmak son kullanıcı etkinleştirmek isteyebilirsiniz. Örneğin, ayıklamak için hangi düzeyde benzetimini yapmak için Ağ Yük veya geçici dosyaları veya iliştirilecek dosyaları için dizin hangi kayıt defteri anahtarlarını belirten yapılandırma verilerini seçebilirsiniz.

Tanılama veri bağdaştırıcınız için ilk değerleri ayarlamak için bir yapılandırma dosyası kullanmanız gerekir. Yapılandırma verisini değiştirmesine olanak vermek için özel bir düzenleyici sağlayabilirsiniz.

Kendi düzenleyicinizi oluşturmak için uygulayan bir kullanıcı denetimi oluşturacaksınız <xref:Microsoft.VisualStudio.TestTools.Execution.IDataCollectorConfigurationEditor>.

Tanılama veri bağdaştırıcınızı kullanabileceğiniz bir <xref:Microsoft.VisualStudio.TestTools.Execution.DataCollectorConfigurationEditorAttribute> tanılama verisi yapılandırma ayarlarını düzenlemek üzere kullanılacak düzenleyici sınıfı belirlemek için.

Ayrıca, kullanmak istediğiniz varsayılan yapılandırma verilerini de belirtin.  Bkz: [tanılama veri bağdaştırıcısı oluşturmak için örnek proje](../test/sample-project-for-creating-a-diagnostic-data-adapter.md) varsayılan yapılandırma örneği için.

Özel veri tanılama bağdaştırıcınız kullanıldığında test ayarlarınız için verileri güncelleştirmek için özel bir düzenleyici oluşturmak için aşağıdaki yordamı kullanın.

> [!NOTE]
> Özel bir düzenleyici oluşturmak için öncelikle sahip tanılama veri bağdaştırıcınızı oluşturmanız gerekir <xref:Microsoft.VisualStudio.TestTools.Execution.DataCollectorConfigurationEditorAttribute> sınıfa uygulanır. Kullanabileceğiniz isteğe bağlı <xref:Microsoft.VisualStudio.TestTools.Execution.DataCollectorConfigurationEditorAttribute.HelpUri*> özelliğini düzenleyiciniz için Yardım içerik kaynağını belirtmek için bu özniteliği. Tanılama veri bağdaştırıcınızı oluşturmakla ilgili daha fazla bilgi için bkz. [nasıl yapılır: tanılama veri bağdaştırıcısı oluşturma](../test/how-to-create-a-diagnostic-data-adapter.md).

Özel yapılandırma Düzenleyicisi içeren tam bir örnek tanılama veri bağdaştırıcısı için bir proje, bkz: [tanılama veri bağdaştırıcısı oluşturmak için örnek proje](../test/sample-project-for-creating-a-diagnostic-data-adapter.md).

## <a name="to-create-a-custom-editor-for-your-diagnostic-data-adapter"></a>Tanılama veri bağdaştırıcınız için özel bir düzenleyici oluşturmak için

1. Veri tanılama bağdaştırıcınız için projeniz üzerinde bir kullanıcı denetimi oluşturun:

   1.  Kendi tanılama veri bağdaştırıcısı sınıfınızı içeren kod projesini sağ tıklatın, **Ekle** gelin ve ardından **kullanıcı denetimi**.

   2.  Bu örnekte, forma bu metin içeren bir etiket ekleyin: **veri dosyası ismi:** ve adlı bir metin kutusu **etiketiyle basit** kullanıcının gerekli verileri girmesini etkinleştirilir.

   > [!NOTE]
   > Şu anda, yalnızca Windows Forms kullanıcı denetimleri desteklenir.

2. Bu satırları bildirim bölümüne ekleyin:

   ```csharp
   using System.Xml;
   using Microsoft.VisualStudio.TestTools.Common;
   using Microsoft.VisualStudio.TestTools.Execution;
   ```

3. Bu kullanıcı denetimi, özel bir düzenleyiciye ayarlayın.

   1.  Kod projenizde kullanıcı denetimine sağ tıklayın ve fareyle **kod**.

   2.  Set sınıfı, düzenleyici arabirimini uygulamak için <xref:Microsoft.VisualStudio.TestTools.Execution.IDataCollectorConfigurationEditor> gibi:

   ```csharp
   public partial class MyDataConfigEditor :
        UserControl, IDataCollectorConfigurationEditor
   ```

   1.  Sağ <xref:Microsoft.VisualStudio.TestTools.Execution.IDataCollectorConfigurationEditor> kodu ve select **arabirim uygulama** komutu. Bu arabirim için uygulamanız gereken yöntemler sınıfınıza eklenir.

   2.  Ekleme <xref:Microsoft.VisualStudio.TestTools.Execution.DataCollectorConfigurationEditorAttribute> değiştirerek bir tanılama veri bağdaştırıcısı Düzenleyicisi tanımlamak düzenleyiciniz için kullanıcı denetleyicinize **şirket**, **ürün**, ve **sürüm** ile tanılama veri bağdaştırıcınız için uygun bilgileri:

       ```csharp
       [DataCollectorConfigurationEditorTypeUri(
           "configurationeditor://MyCompany/MyConfigEditor/1.0")]
       ```

4. İki özel değişkeni aşağıdaki şekilde ekleyin:

   ```csharp
   private DataCollectorSettings collectorSettings;
   private IServiceProvider ServiceProvider { get; set; }
   ```

5. Tanılama veri bağdaştırıcınız için düzenleyicinizi başlatmak için kod ekleyin. Ayarlar değişkeninde bulunan veriyi kullanarak kullanıcı Denetiminizdeki alanlara varsayılan değerler ekleyebilirsiniz. Bu olan verilerdir `<DefaultConfiguration>` bağdaştırıcınızın XML yapılandırma dosyasında öğesi.

   ```csharp
   public void Initialize(
       IServiceProvider svcProvider,
       DataCollectorSettings settings)
   {
       ServiceProvider = svcProvider;
       collectorSettings = settings;

       // Display the default file name as listed in the settings file.
       this.SuspendLayout();
       this.FileTextBox.Text = getText(collectorSettings.Configuration);
       this.ResumeLayout();
   }
   ```

6. Denetimlerinizi düzenleyicinizde verileri geri tanılama veri bağdaştırıcısı API gibi gerekli XML biçimine kaydetmek için kodu ekleyin:

   ```csharp
   public DataCollectorSettings SaveData()
   {
       collectorSettings.Configuration.InnerXml =
           String.Format(
   @"<MyCollectorName
       xmlns=""http://MyCompany/schemas/MyDiagnosticDataCollector/1.0"">
     <File FullPath=""{0}"" />
   </MyCollectorName>",
       FileTextBox.Text);
       return collectorSettings;
   }
   ```

7. Sizin için önemli olan verilerin doğru olduğunu doğrulamak için kod ekleyin `VerifyData` yöntemi veya yöntem dönüş olabilir `true`.

   ```csharp
   public bool VerifyData()
   {
       // Not currently verifying data
       return true;
   }
   ```

8. (İsteğe bağlı) Veri XML yapılandırma dosyasında sağlanan başlangıç ayarlarına sıfırlamak için kod ekleyebilirsiniz `ResetToAgentDefaults()` yöntemi private kullanan `getText()` yöntemi.

   ```csharp
   // Reset to default value from XML configuration
   // using a custom getText() method
   public void ResetToAgentDefaults()
   {
       this.FileTextBox.Text = getText(collectorSettings.DefaultConfiguration);
   }

   // Local method to read the configuration settings
   private string getText(XmlElement element)
   {
       // Setup namespace manager with our namespace
       XmlNamespaceManager nsmgr =
           new XmlNamespaceManager(
               element.OwnerDocument.NameTable);

       // Find all the "File" elements under our configuration
       XmlNodeList files = element.SelectNodes("//ns:MyCollectorName/ns:File", nsmgr);

       string result = String.Empty;
       if (files.Count > 0)
       {
           XmlAttribute pathAttribute = files[0].Attributes["FullPath"];
           if (pathAttribute != null &&
               !String.IsNullOrEmpty(pathAttribute.Value))
           {
               result = pathAttribute.Value;
           }
       }

       return result;
   }
   ```

9. Çözümünüzü oluşturun. Veri tanılama bağdaştırıcısı derlemesini ve XML yapılandırma dosyasını kopyalayın (`<diagnostic data adapter name>.dll.config`), yükleme dizinine dayanan aşağıdaki konuma: *% ProgramFiles (x86) %\Microsoft Visual Studio\2017\Enterprise\Common7\IDE\ PrivateAssemblies\DataCollectors*.

    > [!NOTE]
    > Yapılandırma Düzenleyicisi, bir proje ve tanılama veri bağdaştırıcısından farklı bir derleme olabilir, ancak aynı derlemede de olabilirler.

10. Test tanılama veri bağdaştırıcınızı kullanmak için varolan test ayarları listesinden seçin veya yeni bir Microsoft Test Yöneticisi ya da Visual Studio ve gerekir, tanılama veri bağdaştırıcısı'ı seçin.

     Bağdaştırıcı görüntülenir **veri ve tanılama** test ayarlarınızı sınıfa atadığınız yakın ad ile sekmesindeki.

11. Test ayarlarınız için tanılama veri bağdaştırıcınızı yapılandırmak için **yapılandırma** bağdaştırıcı adı yanındaki.

     Özel düzenleyiciniz şimdi görüntüleniyor.

12. Gerektiği gibi özel düzenleyiciniz üzerindeki alanları düzenleyin ve ardından **Kaydet**.

13. Testlerinizi Microsoft Test Yöneticisi'nden çalıştırıyorsanız, bunları atayabilir ve testlerinizi çalıştırmak veya kullanmadan önce test planınıza test **seçenekler ile Çalıştır** komut test ayarlarınızı atamak ve yok saymak için test ayarları. Test ayarları hakkında daha fazla bilgi için bkz. [test ayarlarını kullanarak tanılama bilgi toplayan](../test/collect-diagnostic-information-using-test-settings.md).

14. Yeni yapılandırma düzenleyicinizi bir tanılama veri bağdaştırıcısı ile kullanmadan önce uygulamalısınız <xref:Microsoft.VisualStudio.TestTools.Execution.DataCollectorConfigurationEditorAttribute> Düzenleyicisi'ni kullanın ve yeniden derleyin ve onları istemci bilgisayarda yeniden istediğiniz her tanılama veri bağdaştırıcısını sınıf için. Tanılama veri bağdaştırıcısı ve yapılandırma düzenleyicileri yükleme hakkında daha fazla bilgi için bkz. [nasıl yapılır: özel tanılama veri bağdaştırıcısı yükleme](../test/how-to-install-a-custom-diagnostic-data-adapter.md).

15. Seçilen tanılama veri bağdaştırıcısıyla test ayarlarını kullanarak testlerinizi çalıştırın.

     Düzenleyicinizde belirttiğiniz veri dosyası test sonuçlarınıza eklenir.

    Test ayarlarınızı testlerinizi çalıştırdığınızda kullanacağınız ortam için yapılandırma hakkında daha fazla bilgi için bkz. [(Azure Test planları) test sırasında tanılama verilerini toplama](/azure/devops/test/collect-diagnostic-data?view=vsts) veya [testleri (el ile Tanılama verileri toplama Azure Test planlarını)](/azure/devops/test/mtm/collect-more-diagnostic-data-in-manual-tests?view=vsts).

## <a name="see-also"></a>Ayrıca bkz.

- <xref:Microsoft.VisualStudio.TestTools.Execution.IDataCollectorConfigurationEditor>
- <xref:Microsoft.VisualStudio.TestTools.Execution.DataCollectorConfigurationEditorAttribute>
- <xref:Microsoft.VisualStudio.TestTools.Execution.DataCollectorConfigurationEditorAttribute>
- [Özel veri toplayan veya test makinesini etkileyen tanılama veri bağdaştırıcısı oluşturma](../test/create-a-diagnostic-data-adapter-to-collect-custom-data-or-affect-a-test-machine.md)
- [Test ayarlarını kullanarak tanılama bilgileri Topla](../test/collect-diagnostic-information-using-test-settings.md)
- [Tanılama veri bağdaştırıcısı oluşturmak için örnek proje](../test/sample-project-for-creating-a-diagnostic-data-adapter.md)
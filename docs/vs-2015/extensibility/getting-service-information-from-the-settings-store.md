---
title: Ayarları Store ' hizmet bilgilerini alma | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-sdk
ms.topic: conceptual
ms.assetid: 7028d440-d16d-4b08-9b94-eb8cc93b25fc
caps.latest.revision: 5
ms.author: gregvanl
manager: jillfra
ms.openlocfilehash: cfe754203ae9b4e951de5beef8cd829f9d7716bb
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "68204305"
---
# <a name="getting-service-information-from-the-settings-store"></a>Ayarlar Deposu'ndan Hizmet Bilgilerini Alma
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Ayarlar deposu, tüm kullanılabilir hizmetleri bulmak için veya belirli bir hizmet yüklü olup olmadığını belirlemek için kullanabilirsiniz. Hizmet sınıfı türünü bilmeniz gerekir.  
  
### <a name="to-list-the-available-services"></a>Kullanılabilir hizmetleri listeleyin  
  
1. FindServicesExtension adlı bir VSIX projesi oluşturun ve ardından FindServicesCommand adlı özel bir komut ekleyin. Özel komut oluşturma hakkında daha fazla bilgi için bkz. [bir menü komutuyla uzantı oluşturma](../extensibility/creating-an-extension-with-a-menu-command.md)  
  
2. FindServicesCommand.cs içinde aşağıdaki ekleme using deyimlerini:  
  
    ```vb  
    using System.Collections.Generic;  
    using Microsoft.VisualStudio.Settings;  
    using Microsoft.VisualStudio.Shell.Settings;  
    using System.Windows.Forms;  
    ```  
  
3. Yapılandırma ayarları deposu alın ve ardından Hizmetleri adlı koleksiyon bulunamadı. Bu koleksiyon, kullanılabilir hizmetlerin hepsini içerir. MenuItemCommand yöntemi mevcut kodu kaldırın ve aşağıdakiyle değiştirin:  
  
    ```  
    private void MenuItemCallback(object sender, EventArgs e)  
    {  
        SettingsManager settingsManager = new ShellSettingsManager(ServiceProvider);  
        SettingsStore configurationSettingsStore = settingsManager.GetReadOnlySettingsStore(SettingsScope.Configuration);  
        string message = "Available services:\n";  
        IEnumerable<string> collection = configurationSettingsStore.GetSubCollectionNames("Services");  
        int n = 0;  
        foreach (string service in collection)  
        {  
            message += configurationSettingsStore.GetString("Services\\" + service, "Name", "Unknown") + "\n";  
        }  
  
        MessageBox.Show(message);  
    }  
    ```  
  
4. Projeyi oluşturmak ve hata ayıklamaya başlayın. Deneysel örneği açılır.  
  
5. Deneysel örneğinde üzerinde **Araçları** menüsünde tıklatın **çağırma FindServicesCommand**.  
  
     Tüm hizmetler listeleyen bir ileti kutusu görmeniz gerekir.  
  
     Bu ayarları doğrulamak için Kayıt Defteri Düzenleyicisi'ni kullanabilirsiniz.  
  
## <a name="finding-a-specific-service"></a>Belirli bir hizmet bulma  
 Ayrıca <xref:Microsoft.VisualStudio.Settings.SettingsStore.CollectionExists%2A> belirli bir hizmet yüklü olup olmadığını belirlemek için yöntemi. Hizmet sınıfı türünü bilmeniz gerekir.  
  
1. İçinde MenuItemCallback önceki yordamda oluşturduğunuz proje için yapılandırma ayarları deposu arama `Services` hizmetinin GUID ile adlı koleksiyon içeren koleksiyon. Bu durumda biz Yardım hizmeti için görünür.  
  
    ```  
    private void MenuItemCallback(object sender, EventArgs e)  
    {  
        SettingsManager settingsManager = new ShellSettingsManager(ServiceProvider);  
        SettingsStore configurationSettingsStore = settingsManager.GetReadOnlySettingsStore(SettingsScope.Configuration);  
        string helpServiceGUID = typeof(SVsHelpService).GUID.ToString("B").ToUpper();  
        bool hasHelpService = configurationSettingsStore.CollectionExists("Services\\" + helpServiceGUID);  
        string message = "Help Service Available: " + hasHelpService;  
  
        MessageBox.Show(message);  
    }  
    ```  
  
2. Projeyi oluşturmak ve hata ayıklamaya başlayın.  
  
3. Deneysel örneğinde üzerinde **Araçları** menüsünde tıklatın **çağırma FindServicesCommand**.  
  
     Metin içeren bir ileti görürsünüz **hizmet kullanılabilir Yardım:** ardından **True** veya **False**. Bu ayarı doğrulamak için önceki adımlarda gösterildiği gibi bir kayıt defteri düzenleyicisi kullanabilirsiniz.

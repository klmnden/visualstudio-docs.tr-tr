---
title: Yükseltme SharePoint çözüm paketlerini dağıtma ve yayımlama | Microsoft Docs
ms.date: 02/02/2017
ms.topic: conceptual
f1_keywords:
- VS.SharePointTools.Project.SharePointProjectPropertyTab
- VS.SharePointTools.Project.Publishing
dev_langs:
- VB
- CSharp
helpviewer_keywords:
- deploying [SharePoint development in Visual Studio]
- SharePoint development in Visual Studio, deploying
author: John-Hart
ms.author: johnhart
manager: jillfra
ms.workload:
- office
ms.openlocfilehash: ebe207bffe16ef7b8dc7af5a79c01b3ee74abe3f
ms.sourcegitcommit: c0202a77d4dc562cdc55dc2e6223c062281d9749
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/24/2019
ms.locfileid: "54863285"
---
# <a name="deploy-publish-and-upgrade-sharepoint-solution-packages"></a>SharePoint çözüm paketleri yükseltme dağıtma ve yayımlama
  Bir SharePoint çözümünü Visual Studio'da geliştirdiğiniz sonra paket (.wsp) dosyası yerel SharePoint sunucusuna dağıtın veya bir uzak veya yerel SharePoint sunucusuna yayımlama. Dosyaları dağıtırsanız, paket dosyaları (.wsp) nasıl dağıtılacağını özelleştirebilirsiniz.  
  
> [!NOTE]  
>  Şu anda yalnızca korumalı çözümler için Uzak SharePoint sunucularını yayımlanabilir. Daha fazla bilgi için [korumalı çözümle ilgili konular](../sharepoint/sandboxed-solution-considerations.md).  
  
## <a name="deploy-publish-and-upgrade"></a>Dağıtma, yayımlama ve yükseltme
 *Dağıtımı* bir SharePoint Proje Visual Studio'da bir yerel ana bilgisayarı için oluşturulmuş bir SharePoint çözüm dosyası kopyalama işlemini ifade eder. Dağıtılmış bir çözümde dağıtımdan sonra çözümün etkinleştirilmesi Internet Information Services (IIS) havuzu geri dönüştürülüyor gibi dağıtım adımları, yapılandırma ve VS. Dağıtmak için **Dağıt** komutunu **derleme** menüsü. Daha fazla bilgi için [nasıl yapılır: SharePoint dağıtım yapılandırmasını düzenleme](../sharepoint/how-to-edit-a-sharepoint-deployment-configuration.md) ve [nasıl yapılır: Dağıtma ve bir SharePoint çözümünü yerel bir SharePoint sitesine yayımlama](../sharepoint/how-to-deploy-and-publish-a-sharepoint-solution-to-a-local-sharepoint-site.md).  
  
 *Yayımlama* gelir için uzak bir SharePoint korumalı bir SharePoint çözüm dosyası site; diğer bir deyişle, başka bir sistemde bulunan bir site. SharePoint Korumalı çözüm dosyası yerel bir SharePoint sitesinde yayımlayabilirsiniz ancak yayımlanan site yerel veya uzak olup bağımsız olarak, dağıtım adımlarını yapılandıramazsınız.  
  
 *Yükseltme* var olan uzaktan veya yerel olarak yayımlanmış SharePoint çözüm güncelleştirmeye ifade eder. Visual Studio'da SharePoint çözüm için herhangi bir değişiklik yapıldıktan sonra çözümü yeniden yayımlamanız çözümün paketi dosya adını değiştirin ve sonra başarıyla yeniden yayımlar ardından çözüm yükseltin. Yerel olarak yayımlanmış bir çözüm yeniden yayımlarsanız, var olan çözüm dosyası geçersiz kılabilirsiniz.  
  
## <a name="deploy-packages"></a>Paketleri Dağıt
 Paket dosyaları, test ve hata ayıklama için geliştirme bilgisayarınızda SharePoint sunucusuna dağıtabilirsiniz. Başka bir bilgisayarda seçerek kurabileceğiniz bir paket dosyası da oluşturabilirsiniz **dosya sistemi Yayımla** seçenek düğmesini **Yayımla** iletişim kutusu. Paket oluşturulur ve belirtilen yerel dosya yoluna kopyalanır. Bir SharePoint çözümünü yerel sunucuya dağıtmak için kullanın **Dağıt** komutunu **derleme** menüsü. Daha fazla bilgi için [nasıl yapılır: Dağıtma ve bir SharePoint çözümünü yerel bir SharePoint sitesi için Yayımlama](../sharepoint/how-to-deploy-and-publish-a-sharepoint-solution-to-a-local-sharepoint-site.md).  
  
 Listesi tanımını dağıtma, bir olay alıcısı Ekle ve özellik Tasarımcısı ve paket Tasarımcısı'nı kullanma hakkında bilgi edinmek için [izlenecek yol: Proje Görev listesi tanımını dağıtma](../sharepoint/walkthrough-deploying-a-project-task-list-definition.md).  
  
## <a name="customize-the-deployment-process"></a>Dağıtım işlemini özelleştirme
 Aşağıdaki tabloda iki dağıtım yapılandırması hata ayıklama ve bir SharePoint çözümünü dağıtırken kullanabileceğiniz kullanabileceğiniz gösterilmektedir.  
  
|Dağıtım Yapılandırması|Açıklama|  
|------------------------------|-----------------|  
|Varsayılan|Varsayılan dağıtım yapılandırması. Aşağıdaki dağıtım adımları gerçekleştirilir:<br /><br /> 1.  Dağıtım öncesi komutu çalıştırın.<br />2.  IIS uygulama havuzunu geri dönüştürün.<br />3.  Çözüm geri çekilir.<br />4.  Çözüme ekleyin.<br />5.  Özelliklerini etkinleştirin.<br />6.  Dağıtım sonrası komutu çalıştırın.<br /><br /> Bir paket kaldırıldığında, aşağıdaki geri çekme adımları gerçekleştirilir.<br /><br /> 1.  IIS uygulama havuzunu geri dönüştürün.<br />2.  Çözüm geri çekilir.|  
|Etkinleştirme yok|Bu dağıtım yapılandırması aynı adımları varsayılan yapılandırma olarak çalışır, ancak etkinleştirme adımı atlar.|  
  
 Tek bir adımda tamamlayın veya dağıtım işlemindeki adımları sırasını değiştirmek için kendi dağıtım yapılandırmaları oluşturabilirsiniz. Daha fazla bilgi için [nasıl yapılır: SharePoint dağıtım yapılandırmasını düzenleme](../sharepoint/how-to-edit-a-sharepoint-deployment-configuration.md).  

 Önce ve dağıtımdan sonra çalıştırılacak komutları da ekleyebilirsiniz. Daha fazla bilgi için [nasıl yapılır: SharePoint dağıtım komutlarını ayarlama](../sharepoint/how-to-set-sharepoint-deployment-commands.md).  
  
## <a name="publish-packages-to-a-remote-or-local-server"></a>Uzak veya yerel bir sunucuya paketleri yayımlama
 Korumalı bir SharePoint çözüm menü çubuğunda, bir uzak sunucuya yayımlamayı tercih **derleme**, **Yayımla**ve ardından **Yayımla** iletişim kutusunda,**SharePoint sitesi için Yayımlama** seçenek düğmesini, uzak sunucunun URL'sini gibi sağlama **https://someremoteserver.sharepoint.microsoftonline.com**.  
  
 Bir SharePoint çözümünü yerel bir sunucuya yayımlamak için **Yayımla** iletişim kutusunda **dosya sistemi Yayımla** seçenek düğmesi, bir yerel sistem yol sağlama.  
  
 Çözüme bir çözüm SharePoint'e başarıyla yayımlar sonra görünür **çözüm Galerisi** Burada, etkinleştirebilir. Daha fazla bilgi için [nasıl yapılır: Dağıtma, yayımlama ve uzak bir sunucudaki SharePoint çözümlerini yükseltmek](../sharepoint/how-to-deploy-publish-and-upgrade-sharepoint-solutions-on-a-remote-server.md).  
  
### <a name="upgrade-published-packages"></a>Yükseltme yayımlanan paketleri
 Visual Studio'da bir SharePoint projesine herhangi bir değişiklik yaparsanız yayımlandıktan sonra değişikliklerin eklenmesi için yayımlanan paket yükseltilmelidir. Başarılı bir şekilde yükseltmek için bir paket adları benzersiz olmalıdır. Aynı ada sahip bir paket hatası uyarıları - var olan bir uygulamayı güncelleştirirken, oluşabilir - SharePoint sitesinde bulunursa, dosya adı çakışıyor ve paketi yeniden adlandır olanak tanır. Yayınlanmasını sonra yeni paketi SharePoint sitesinde görünen ve yükseltilebilir. Yükseltilmiş bir paket eski paketi verileri kullanarak çözüm güncelleştirir ve sonra çözüm SharePoint etkinleştirir. Daha fazla bilgi için [nasıl yapılır: Dağıtma, yayımlama ve uzak bir sunucudaki SharePoint çözümlerini yükseltmek](../sharepoint/how-to-deploy-publish-and-upgrade-sharepoint-solutions-on-a-remote-server.md).  
  
## <a name="see-also"></a>Ayrıca bkz.
 [Paketleme ve SharePoint çözümlerini dağıtma](../sharepoint/packaging-and-deploying-sharepoint-solutions.md)  

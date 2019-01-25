---
title: 'Nasıl yapılır: Yükseltme uzak bir sunucudaki SharePoint çözümlerini dağıtma ve yayımlama | Microsoft Docs'
ms.date: 02/02/2017
ms.topic: conceptual
dev_langs:
- VB
- CSharp
helpviewer_keywords:
- remote deployment [SharePoint development in Visual Studio]
- SharePoint development in Visual Studio, remote deployment
- deploying [SharePoint development in Visual Studio]
- SharePoint development in Visual Studio, deploying
author: John-Hart
ms.author: johnhart
manager: jillfra
ms.workload:
- office
ms.openlocfilehash: 4aafc503ff2b8dffed5b70d17f4eb488baf72704
ms.sourcegitcommit: c0202a77d4dc562cdc55dc2e6223c062281d9749
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/24/2019
ms.locfileid: "54865092"
---
# <a name="how-to-deploy-publish-and-upgrade-sharepoint-solutions-on-a-remote-server"></a>Nasıl yapılır: Uzak bir sunucudaki SharePoint çözümlerini yükseltmek dağıtma ve yayımlama
  SharePoint çözümleri için yerel sistem dağıtmanın yanı sıra, uzak sitelerin veya yerel SharePoint sitelerine korumalı SharePoint çözümlerine yayımlayabilirsiniz. Uzaktan yayımlama işlemi kopyaları *.wsp* dosyasını SharePoint sunucusuna çözümü yükler ve ardından çözümü etkinleştirmek sağlar. Ona değişiklikler yapıldıktan sonra uzak bir SharePoint çözüm yükleme yükseltebilirsiniz.  
  
## <a name="to-publish-a-sandboxed-sharepoint-solution-to-a-remote-sharepoint-server"></a>Korumalı bir SharePoint çözüm uzak bir SharePoint sunucusuna yayımlama  
  
1.  İçinde **Çözüm Gezgini**, yayımlayın ve ardından istediğiniz korumalı SharePoint projesi için kısayol menüsünü açın **Yayımla**.  
  
2.  İçinde **Yayımla** iletişim kutusunda **SharePoint sitesi için Yayımlama** seçenek düğmesini ve ardından bir URL çevrimiçi yayımlama bir site için aşağıdaki gibi girin: `https://mytestsite.sharepoint.microsoftonline.com`.  
  
3.  Seçin **yayımlama sonrasında tarayıcıda çözüm Galerisi sayfasını açın** çözümlerinde listesini görüntülemek için seçenek düğmesini **çözüm Galerisi** yayımlamadan sonra sayfa.  
  
4.  Seçin **Yayımla** düğmesi.  
  
5.  Kullanıcı kimlik doğrulaması gerekiyorsa uzak sunucuya oturum açın.  
  
     Visual Studio'da yayımlama ilerleme görünür **çıkış** penceresi. İşlem tamamlandığında, çözüm (*.wsp*) dosyası, uzak SharePoint sunucusunda yüklü. SharePoint'te kullanılmadan önce ancak bu yine de etkinleştirilmesi gerekir.  
  
6.  Üzerinde **çözüm Galerisi** sayfasında, SharePoint uygulaması'nı seçin ve sonra Şerit üzerinde **etkinleştirme** düğmesi.  
  
7.  İçinde **etkinleştirme çözüm** Seç iletişim kutusu, Şeritteki **etkinleştirme** düğmesini tekrar.  
  
     **Durumu** sütunu **çözüm Galerisi** sayfa uygulama etkin olduğunu gösterir.  
  
## <a name="to-upgrade-a-sandboxed-sharepoint-solution-on-a-remote-sharepoint-server"></a>Korumalı bir SharePoint çözüm uzak bir SharePoint sunucusuna yükseltmek için  
 Korumalı bir SharePoint çözüm zaten uzak bir sunucuda yayımladıysanız, şu işlem için uygulamada değişiklikler yaptıktan sonra yükseltmenize olanak tanır [!INCLUDE[vsprvs](../sharepoint/includes/vsprvs-md.md)].  
  
1.  SharePoint paketi Yeniden Adlandır [!INCLUDE[vsprvs](../sharepoint/includes/vsprvs-md.md)]. Bunu yapmak için **Çözüm Gezgini** paketi açılamadı. Görünür **paket Gezgini**.  
  
2.  İçinde **paket Gezgini**, **adı** kutusunda, paket adı benzersiz bir adla değiştirin.  
  
3.  Projeyi kaydedin.  
  
4.  İçinde **Çözüm Gezgini**, proje için kısayol menüsünü açın ve ardından **Yayımla**.  
  
5.  İçinde **Yayımla** iletişim kutusunda **SharePoint sitesi için Yayımlama** seçenek düğmesini ve ardından çözüm kaydedildiği uzak sunucusu için URL'yi eksikse girin.  
  
6.  Seçin **yayımlama sonrasında tarayıcıda çözüm Galerisi sayfasını açın** çözümlerinde listesini görüntülemek için seçenek düğmesini **çözüm Galerisi** yayımlamadan sonra sayfa.  
  
7.  Seçin **Yayımla** düğmesi.  
  
8.  Kullanıcı kimlik doğrulaması gerekiyorsa uzak sunucuya oturum açın.  
  
     Uzak sunucuya yakın zamanda oturum, kimlik doğrulaması gerekli olmayabilir.  
  
     Aynı ada sahip bir uygulamanın daha eski sürümü SharePoint sunucusunda hala varsa, SharePoint sunucusunda aynı ada sahip bir paket zaten bir hata alırsınız. Yayımlamadan önce benzersiz bir ad için paketi yeniden adlandırmanız gerekir.  
  
9. SharePoint'te yeni bir uygulama seçin ve ardından, Şeritte **yükseltme** düğmesi.  
  
10. İçinde **yükseltme çözüm** Seç iletişim kutusu, Şeritteki **yükseltme** düğmesini tekrar. **Durumu** sütunu **çözüm Galerisi** sayfa artık belirtmek uygulama etkin olduğunu.  
  
     Çözüm eski sürümünü devre dışı, çözümünün yeni sürümü eski çözümden tutulan verilerle yükseltilir ve yeni çözüm SharePoint'te etkinleştirilir.  
  
## <a name="see-also"></a>Ayrıca bkz.
 [Nasıl yapılır: Bir SharePoint çözümünü yerel bir SharePoint sitesi için yayımlama ve dağıtma](../sharepoint/how-to-deploy-and-publish-a-sharepoint-solution-to-a-local-sharepoint-site.md)   
 [SharePoint çözüm paketleri oluşturma](../sharepoint/creating-sharepoint-solution-packages.md)   
 [Nasıl yapılır: Bir SharePoint çözüm paketini özelleştirme](../sharepoint/how-to-customize-a-sharepoint-solution-package.md)   
 [Nasıl yapılır: Ekleme ve özellikler ve öğeler bir paketi paket Tasarımcısını kullanarak kaldırma](../sharepoint/how-to-add-and-remove-features-and-items-to-a-package-by-using-the-package-designer.md)  

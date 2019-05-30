---
title: SharePoint çözümünü yerel SharePoint sitesi için yayımlama ve dağıtma
ms.date: 02/02/2017
ms.topic: conceptual
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
ms.openlocfilehash: 3e68fc4e49311535169ab37a2332b443ba632fb5
ms.sourcegitcommit: 25570fb5fb197318a96d45160eaf7def60d49b2b
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/30/2019
ms.locfileid: "66401460"
---
# <a name="how-to-deploy-and-publish-a-sharepoint-solution-to-a-local-sharepoint-site"></a>Nasıl yapılır: Bir SharePoint çözümünü yerel bir SharePoint sitesi için yayımlama ve dağıtma
  Dağıtın veya SharePoint çözümleri geliştirme bilgisayarınızda yerel bir SharePoint sunucusuna yayımlama. Dağıtım işlemi kopyaları *.wsp* dosyasını SharePoint sunucusuna çözümü yükler ve ardından özellikleri etkinleştirir. Yayımlama işlemi yalnızca kopyaları *.wsp* dosyasını SharePoint sunucusuna ve yükler. SharePoint'te etkinleştirmek için el ile etkinleştirmeniz gerekir.

## <a name="to-deploy-a-sharepoint-solution-to-the-local-sharepoint-server"></a>Bir SharePoint çözümünü yerel SharePoint sunucusuna dağıtmak için

1. İçinde **Çözüm Gezgini**, dağıtmak istediğiniz projeyi seçin.

2. Menü çubuğunda, **derleme**, **çözüm dağıtma**.

     *.Wsp* dosyası oluşturulup yerel SharePoint sunucusunda yüklü. Ayrıca, Özellikler etkinleştirilir.

## <a name="to-publish-a-sharepoint-solution-to-a-local-sharepoint-server"></a>Bir SharePoint çözümünü yerel bir SharePoint sunucusuna yayımlama

1. İçinde **Çözüm Gezgini**, yayımlayın ve ardından istediğiniz SharePoint projesi için kısayol menüsünü açın **Yayımla**.

2. İçinde **Yayımla** iletişim kutusunda **dosya sistemi Yayımla** seçenek düğmesini.

3. İçinde **hedef konum** metin kutusunda, yerel bir yol girin ve ardından **Yayımla** düğmesi.

     Visual Studio'da yayımlama ilerleme görünür **çıkış** penceresi. İşlem tamamlandığında, çözüm ( *.wsp*) dosyası yerel SharePoint sunucusuna yüklenir. Ancak, yine de SharePoint'te kullanılacak etkinleştirilmesi gerekir. Çözüm dosyası zaten varsa, bir hata oluşur ve var olan dosyanın üzerine yazmak isteyip istemediğinizi sorar. Paket yükseltme hakkında daha fazla bilgi için Uzak paketleri yükseltme bölümüne bakın. [nasıl yapılır: Dağıtma, yayımlama ve uzak bir sunucudaki SharePoint çözümlerini yükseltmek](../sharepoint/how-to-deploy-publish-and-upgrade-sharepoint-solutions-on-a-remote-server.md).

## <a name="see-also"></a>Ayrıca bkz.
- [Nasıl yapılır: Uzak bir sunucudaki SharePoint çözümlerini yükseltmek dağıtma ve yayımlama](../sharepoint/how-to-deploy-publish-and-upgrade-sharepoint-solutions-on-a-remote-server.md)
- [SharePoint çözüm paketleri oluşturma](../sharepoint/creating-sharepoint-solution-packages.md)
- [Nasıl yapılır: Bir SharePoint çözüm paketini özelleştirme](../sharepoint/how-to-customize-a-sharepoint-solution-package.md)
- [Nasıl yapılır: Ekleme ve özellikler ve öğeler bir paketi paket Tasarımcısını kullanarak kaldırma](../sharepoint/how-to-add-and-remove-features-and-items-to-a-package-by-using-the-package-designer.md)

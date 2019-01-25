---
title: 'Nasıl yapılır: Eşlenmiş klasörler ekleme ve kaldırma | Microsoft Docs'
ms.date: 02/02/2017
ms.topic: conceptual
f1_keywords:
- VS.SharePointTools.Project.MappedFolder
dev_langs:
- VB
- CSharp
helpviewer_keywords:
- SharePoint development in Visual Studio, mapped folders
- mapped folders [SharePoint development in Visual Studio]
author: John-Hart
ms.author: johnhart
manager: jillfra
ms.workload:
- office
ms.openlocfilehash: 357eb8c16487f625d4c2a7c675e3709f2190ca03
ms.sourcegitcommit: c0202a77d4dc562cdc55dc2e6223c062281d9749
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/24/2019
ms.locfileid: "54871864"
---
# <a name="how-to-add-and-remove-mapped-folders"></a>Nasıl yapılır: eşlenmiş klasörler ekleme ve kaldırma
  Görüntüleri ve düzenleri, katıştırılmış derin bir şekilde dosya hiyerarşide olarak bazı klasörler SharePoint, yaygın olarak kullanılan. Bu klasörleri daha kolay erişmek için bir SharePoint projesine eşleyebilirsiniz. Eşlenen klasörler SharePoint Server'ın yükleme dosyalarının fiziksel konuma karşılık gelen SharePoint Proje klasörlerdir.  
  
 Bir SharePoint uygulaması dağıttığınızda, içeriği eşlenmiş klasör ve tüm alt klasörlerinde çözüm paketine (.wsp) tarafından sunucuya kopyalanır, SharePoint SharePoint klasörü ağacında belirtilen konumda çalışıyor. Bu konumu tarafından belirlenir **dağıtım konumu** eşlenmiş klasör için ayarlanmış özelliği. Eşlenen klasörün tüm alt klasörlerinde göreli olan **dağıtım konumu** eşlenen klasörün. Unutmayın **dağıtım konumu** özelliği, eşlenmiş klasör adını değil, öğeleri dağıtıldığı belirler.  
 Eşlenen klasörler proje için komutları menü çubuğundan veya kısayol menüsünü kullanarak, bir projeye ekleyebilirsiniz. Kullanabilirsiniz **SharePoint Ekle "Görüntüler" eşlenen klasörü** ve **SharePoint Ekle "Düzenler" klasörü** komutları bu eklemek için en sık kullanılan klasörleri eşlenmiş. Kullanarak diğer kullanılabilir SharePoint klasörlerden herhangi biri projenize eşleyebilirsiniz **SharePoint eşlenen klasörü Ekle** komutu kısayol menüsünde ve klasörlerde belirterek **SharePoint eşlenen klasörü Ekle** iletişim kutusu.  
  
## <a name="add-mapped-folders-to-a-project"></a>Projeye eşlenmiş klasörler ekleme  
 Aşağıdaki yordam, bir görsel web bölümü projesi iki eşlenmiş klasör eklemeyi açıklar. Başlamak için bir görsel web bölümü projesi oluşturun.  
  
#### <a name="to-add-mapped-folders-to-a-project"></a>Eşlenen klasörler bir projeye eklemek için  
  
1.  Menü çubuğunda, **dosya** > **yeni** > **proje**.  
  
2.  İçinde **yeni proje** iletişim kutusunda, ya da genişletin **Visual Basic** veya **Visual C#**  düğümünü genişletin **Office/SharePoint** düğümünü seçip **SharePoint çözümleri** düğümü.  
  
3.  Proje şablonları listesinde seçin **SharePoint 2013 görsel Web Bölümü** şablonu.  
  
4.  İçinde **adı** kutusuna **TestProject1**ve ardından **Tamam** düğmesi.  
  
5.  İçinde **SharePoint Özelleştirme Sihirbazı**, seçin **son** varsayılan ayarları korumak için düğme.  
  
6.  İçinde **Çözüm Gezgini**, proje düğümünü seçin ve ardından, menü çubuğunda, **proje** > **SharePoint Ekle "Görüntüler" eşlenen klasörü**.  
  
     Adlı bir klasör **görüntüleri** projenizde görünür ve TestProject1 adlı bir alt klasör içerir. Bu eşlenmiş klasör visual web bölümü projesi için görüntüleri içerir.  
  
7.  İçinde **Çözüm Gezgini**, proje düğümünü seçin ve ardından, menü çubuğunda, **proje** > **SharePoint eşlenen klasörü Ekle** görüntülemekiçin **SharePoint eşlenen klasörü Ekle** iletişim kutusu.  
  
8.  Eşleme için kullanılabilir olan klasörler ağaç görünümünde seçin **kaynakları** klasörünü ve ardından **Tamam** düğmesi.  
  
     Adlı bir klasör **kaynakları** projenizde görünür. Bu klasör, dize kaynak dosyaları gibi öğeleri depolayabilirsiniz. Alt klasörleri eşlenen klasörün içeriği düzenlemek için yararlı olabilir, ancak eşlenmiş bir klasöre kullanarak eklediğinizde, bunlar otomatik olarak oluşturulan **SharePoint eşlenen klasörü Ekle** komutu. Bir alt klasör eklemek için **kaynakları** klasörünü ve ardından, menü çubuğunda, **proje** > **yeni klasör**.  
  
## <a name="change-the-deployment-location-of-a-mapped-folder"></a>Eşlenmiş bir klasöre dağıtım konumunu değiştirme  
 Varsayılan olarak, belirli konumlara göre SharePoint kök yükleme yolunu, eşlenmiş klasörler eklenir, belirteç \<SharePointRoot > gösterir. Ancak, bu konuma değiştirerek değiştirebileceğiniz **dağıtım konumu** eşlenen klasörün özelliği. Her eşlenen klasörü kendi bölümüne sahiptir **dağıtım konumu** özelliği.  
  
#### <a name="to-change-the-deployment-location-of-a-mapped-folder"></a>Eşlenmiş bir klasöre dağıtım konumunu değiştirmek için  
  
1.  Daha önce oluşturduğunuz projede, eşleşen bir klasör seçin.  
  
2.  İçinde **özellikleri** penceresinde üç noktayı seçin (![ASP.NET Mobil Tasarımcısı elips](../sharepoint/media/mwellipsis.gif "ASP.NET Mobil Tasarımcısı elips")) düğmesini **dağıtım Konum** özelliği.  
  
3.  İçinde **SharePoint eşlenen klasörü Ekle** iletişim kutusunda, işaret edecek şekilde eşlenen klasörü istediğiniz klasöre gidin.  
  
4.  Düğümü seçin ve ardından **Tamam** düğmesi.  
  
## <a name="rename-or-remove-mapped-folders"></a>Yeniden adlandırma veya eşlenmiş klasörler Kaldır  
  
#### <a name="to-rename-or-remove-a-mapped-folder"></a>Yeniden adlandırmakta ya da eşlenen klasörü Kaldır  
  
1.  Daha önce oluşturduğunuz projede, eşleşen bir klasör seçin.  
  
2.  Eşlenen klasörü yeniden adlandırmak için kısayol menüsünü açın, **Yeniden Adlandır**, yeni bir ad girin ve ardından Enter tuşuna basın.  
  
     Alternatif olarak, yeniden adlandırma, açmak istediğiniz eşlenen klasörü seçebilirsiniz **özellikleri** penceresinde ve ardından değerini **klasör adı** özelliğini yeni adı.  
  
3.  Eşlenmiş bir klasöre projeden kaldırmak için kısayol menüsünü açın, **Sil**ve ardından **Tamam** kaldırma işlemini onaylamak için iletişim kutusunda düğmesi.  
  
## <a name="see-also"></a>Ayrıca bkz.
 [SharePoint çözümleri geliştirme](../sharepoint/developing-sharepoint-solutions.md)  

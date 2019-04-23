---
title: 'Nasıl yapılır: Ana sayfa veya temayı içeri aktarma | Microsoft Docs'
ms.date: 02/02/2017
ms.topic: conceptual
dev_langs:
- VB
- CSharp
helpviewer_keywords:
- SharePoint development in Visual Studio, importing items
- importing items [SharePoint development in Visual Studio]
author: John-Hart
ms.author: johnhart
manager: jillfra
ms.workload:
- office
ms.openlocfilehash: 1be553955abdc42c2a9b4d09ff857e9236b1a002
ms.sourcegitcommit: 1fc6ee928733e61a1f42782f832ead9f7946d00c
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/22/2019
ms.locfileid: "60081912"
---
# <a name="how-to-import-a-master-page-or-theme"></a>Nasıl yapılır: Ana sayfa veya temayı içeri aktarma
  Sayfaları SharePoint sitenizde tutarlı bir görünüm oluşturma ve ana sayfalar ve Temalar kullanarak verebilirsiniz. [!INCLUDE[vsprvs](../sharepoint/includes/vsprvs-md.md)] Bu öğeler için şablonlar içermez, ancak bunları SharePoint Tasarımcısı'nda oluşturabilir ve bunları içe [!INCLUDE[vsprvs](../sharepoint/includes/vsprvs-md.md)]. Daha fazla bilgi için [yapı taşı: Sayfalar ve kullanıcı arabirimi](http://go.microsoft.com/fwlink/?LinkID=182095) Microsoft Web sitesinde.

### <a name="to-import-a-master-page-or-theme"></a>Bir ana sayfa veya temayı içeri aktarmak için

1. İçinde [!INCLUDE[vsprvs](../sharepoint/includes/vsprvs-md.md)]oluşturun veya bir SharePoint projesi açın.

     Bir SharePoint projesi oluşturma hakkında daha fazla bilgi için bkz: [SharePoint projesi ve proje öğesi şablonları](../sharepoint/sharepoint-project-and-project-item-templates.md).

2. Menü çubuğunda, **proje** > **Yeni Öğe Ekle**.

3. İçinde **Yeni Öğe Ekle** iletişim kutusunda **SharePoint** düğümünü seçip **2010** düğümü.

4. SharePoint şablonları listesinde seçin **Modülü** şablonu ve ardından modül için bir ad belirtin.

     Bir modül, SharePoint'te belirttiğiniz bir konuma dağıtımı için (örneğin, ana sayfa veya temayı dosyaları) dosyalarını içerir.

5. Modülde adlı varsayılan dosyayı Sil *örnek.txt*.

6. Modül düğümü seçin.

7. Menü çubuğunda, **proje** > **varolan öğeyi Ekle**, ana sayfa veya temayı dosyası seçin.

     Ana sayfa dosyalar .master uzantısına sahiptir ve tema dosyalar .thmx uzantısına sahiptir.

8. Ana sayfa eklediyseniz, değiştirme, **dağıtım çakışması çözümü** ayarını **otomatik** modülün özellikleri.

    > [!NOTE]
    >  Ana sayfa adını varsayılan ana sayfa veya özel bir ana sayfa olarak işaretlenmiş var olan bir ana sayfa adı ile aynı olduğunda hatalar oluşabilir. Bu sorunun nasıl giderileceği hakkında daha fazla bilgi için bkz. [izlenecek yol: Özel ana sayfasını ve görüntü ile site sayfasını içeri aktarma](../sharepoint/walkthrough-import-a-custom-master-page-and-site-page-with-an-image.md).

9. Modülde açın *Elements.xml*.

     Güncelleştirmeniz gerekir *Elements.xml* ana sayfa veya eklediğiniz tema başvurmak için dosya.

10. Bir ana sayfa için mevcut modülü biçimlendirmeyi aşağıdaki biçimlendirme ile değiştirin.

    ```xml
    <Module Name="[Module Name]" Url="_catalogs/masterpage">
        <File Path="[Module Name]\[Master Page Name].master"
          Url="[Master Page Name].master" Type="GhostableInLibrary" />
    </Module>
    ```

     Bir tema için mevcut modülü biçimlendirmeyi aşağıdaki biçimlendirme ile değiştirin.

    ```xml
    <Module Name="[Module Name]" Url="_catalogs/theme"
        <File Path="[Module Name]\[Theme Name].thmx" Url="[Theme
          Name].thmx" Type="GhostableInLibrary" />
    </Module>
    ```

     Yer tutucu değerlerini modülü ve ana sayfa veya temayı gerçek adlarını ile değiştirdiğinizden emin olun.

     Öznitelik `Type="GhostableInLibrary"` belirtir öğe içerik veritabanına eklenir ve `Url` modülünün özniteliği SharePoint içerik veritabanı dosyasının depolanacağı konumu belirtir.

11. Bir ana sayfa için dağıtım kapsamına değiştirmek için **Çözüm Gezgini**, özellik Tasarımcısı'nda özellik dosyasını açın ve yeni bir dağıtım kapsamından ardından **kapsam** listesi.

     Değerini **Web** geçerli projede belirtilen Web sitesinin ana sayfaya uygulandığı anlamına gelir. Değerini **Site** ana sayfanın tüm alt siteleri ve kök web içeren geçerli site koleksiyonuna uygulanacağı anlamına gelir. Diğer değerleri için geçerli değildir.

    > [!NOTE]
    >  Temalar yalnızca site koleksiyonu düzeyi için geçerli olduğundan, bir tema kapsamı için herhangi bir şey dışında ayarladığınız yoksa öneririz **Site**. Bir alt sitede bir tema kullanılıyorsa hatalar oluşabilir.

12. Menü çubuğunda, **derleme** > **çözüm dağıtma**.

13. Dosyaların doğru bir şekilde dağıtılıp dağıtılmadığını doğrulamak için SharePoint sitesi açın, **Site eylemleri** menüsünde seçin **Site Ayarları** komutunu ve ardından ya da **ana sayfalar**  bağlantı veya **Temalar** bağlantı.

     Ana sayfa veya temaları listesinde görünür ve ana sayfa veya temayı içeri aktardığınız içeriyor.

## <a name="see-also"></a>Ayrıca bkz.
- [Ana Sayfalar](http://go.microsoft.com/fwlink/?LinkId=184955)
- [Mevcut bir SharePoint sitesinden öğeleri içeri aktarma](../sharepoint/importing-items-from-an-existing-sharepoint-site.md)
- [SharePoint için sayfa oluşturma](../sharepoint/creating-pages-for-sharepoint.md)
- [Çözüme dosyaları dahil etmek için modül kullanma](../sharepoint/using-modules-to-include-files-in-the-solution.md)

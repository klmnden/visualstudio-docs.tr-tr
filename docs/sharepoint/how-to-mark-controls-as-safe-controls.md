---
title: 'Nasıl yapılır: Denetimleri güvenli denetim olarak işaretleme | Microsoft Docs'
ms.date: 02/02/2017
ms.topic: conceptual
dev_langs:
- VB
- CSharp
helpviewer_keywords:
- SharePoint development in Visual Studio, safe controls
- SharePoint development in Visual Studio, advanced packaging tools
- safe controls [SharePoint development in Visual Studio]
author: John-Hart
ms.author: johnhart
manager: jillfra
ms.workload:
- office
ms.openlocfilehash: d3f0ff39658aca76318174143da52e17594ace24
ms.sourcegitcommit: c0202a77d4dc562cdc55dc2e6223c062281d9749
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/24/2019
ms.locfileid: "54875474"
---
# <a name="how-to-mark-controls-as-safe-controls"></a>Nasıl yapılır: Denetimleri güvenli denetim olarak işaretleme
  Güvenlik için SharePoint, betik ekleme karşı korumalı Web denetimleri ve olmayan Web denetimleri ayırır. Denetimler, korumalı veya *güvenli denetimler*, güvenilir olmayan kullanıcılar tarafından erişilebilir. Denetimleri güvenli denetim girdileri özelliğini bir SharePoint Proje öğesinin veya güvende olarak işaretleyebilirsiniz **paket Tasarımcısı** eklediğinizde bir derleme paketi. Daha fazla bilgi için bkz.  
  
 [Web.config dosyasının ayarlarını değiştir](http://go.microsoft.com/fwlink/?LinkId=178965) ve [güvenli denetim olarak bir Web Bölümü derlemeyi Kaydettirdikten](http://go.microsoft.com/fwlink/?LinkId=171013).  
  
> [!IMPORTANT]  
>  Bu yordamlar yalnızca tanım amaçlıdır. Yalnızca güvenli olduğundan eminseniz güvenli işareti denetler.  
  
## <a name="marking-safe-controls-in-the-safe-control-entries-property"></a>Güvenli denetimler güvenli denetim girdileri özelliğinde işaretleme  
  
#### <a name="to-mark-controls-as-safe-or-unsafe-in-the-safe-control-entries-property"></a>Denetimleri güvenli veya güvenli denetim girdileri özelliğinde Güvensiz olarak işaretlemek için
  
1.  Bir SharePoint çözümünü bir görsel Web Bölümü projesi oluşturun.  
  
2.  İki denetimi Web bölümüne ekleyin: bir metin kutusu ve düğme. Adları, varsayılan değerlerinde, TextBox1 ve Button1, sırasıyla bırakın.  
  
3.  Web Bölümü'nın iki giriş eklemek **güvenli denetim girdileri** özelliği. Bunu yapmak için üç noktayı seçin (![ASP.NET Mobil Tasarımcısı elips](../sharepoint/media/mwellipsis.gif "ASP.NET Mobil Tasarımcısı elips")) düğmesinin yanındaki **güvenli denetim girdileri** özelliği **Özellikleri** penceresi.  
  
     **Güvenli denetim girdileri** iletişim kutusu görüntülenir.  
  
4.  İçinde **güvenli denetim girdileri** iletişim kutusunda **Ekle** iki kez için iki güvenli denetim girdileri eklemek için Ekle düğmesine **üyeleri** bölmesi: düğme ve metin kutusu için bir tane.  
  
5.  İlk güvenli denetim girişi seçin ve ardından değerini değiştirebilir, **güvenli** özelliğini **False**, kendi **tür adı** özelliğini **Button1**ve onun **karşı güvenli betik** özelliğini **False**.  
  
     Bu adım, bir güvenli denetim olarak düğme denetimini tanımlar.  
  
6.  İkinci güvenli denetim girişi listeden seçin. Değerini değiştirmeden bırakın, **güvenli** özelliği olarak **True** ve kendi **tür adı** özelliğini **TextBox1** ve kendi **güvenli Betiğe karşı** özelliğini **True**.  
  
     Metin kutusu denetimini betik ekleme karşı güvenli bir denetim olarak işaretlendi.  
  
7.  Seçin **Tamam** iletişim kutusunu kapatmak için düğme.  
  
## <a name="marking-safe-controls-in-the-package-designer"></a>Paket Tasarımcısı'nda güvenli denetim olarak işaretleme  
  
#### <a name="to-mark-controls-as-safe-or-unsafe-in-the-package-designer"></a>Güvenli veya paket Tasarımcısı'nda güvenli olarak işaretlemek için denetler
  
1.  Bir SharePoint çözümünü bir görsel Web Bölümü projesi oluşturun.  
  
2.  İki denetimi Web bölümüne ekleyin: bir metin kutusu ve düğme. Adları, varsayılan değerlerinde, TextBox1 ve Button1, sırasıyla bırakın.  
  
     Daha sonra kullanıldığından denetimin ad alanı not alın.  
  
3.  Menü çubuğunda, **derleme** > **Çözümü Derle** Projeyi derlemek için.  
  
4.  Başka bir SharePoint çözüm oluşturun.  
  
5.  İçinde **Çözüm Gezgini**, kısayol menüsünü açın *Package.Package* dosya ve ardından **açın** açmak için **paket Tasarımcısı**.  
  
6.  İçinde **paket Tasarımcısı**, seçin **Gelişmiş** sekmesi.  
  
7.  Altında **ek derlemeler**, seçin **Ekle** düğmesine ve ardından **mevcut bütünleştirilmiş kodu Ekle** listeden.  
  
8.  İçinde **mevcut bütünleştirilmiş kodu Ekle** iletişim kutusunda, üç noktayı seçin (![ASP.NET Mobil Tasarımcısı elips](../sharepoint/media/mwellipsis.gif "ASP.NET Mobil Tasarımcısı elips")) düğmesinin yanındaki  **Kaynak yolu**.  
  
9. 1. adımda oluşturduğunuz SharePoint çözümünden derlemeyi seçin ve ardından **açık** düğmesi.  
  
10. Bu örnekte, bırakın **dağıtım hedefi** seçeneği GlobalAssemblyCache olarak.  
  
     Bu adım sisteme Genel Derleme Önbelleği (GAC) dağıtmak derleme neden olur. Web uygulaması (depo) klasörüne dağıtmak için derleme istiyorsanız bu seçeneği yerine belirleyin. Daha fazla bilgi için [dağıtma Web Bölümleri SharePoint Foundation'da](http://go.microsoft.com/fwlink/?LinkId=177509).  
  
11. İçinde **güvenli denetimler** kutusunda **yeni bir öğe eklemek için burayı tıklatın** düğmesi.  
  
12. Değerleri olan özellikler için aşağıdaki tablodan girin.  
  
    |Özellik Adı|Değer|  
    |-------------------|-----------|  
    |Ad Alanı|Tam ad alanı için denetim gibi **BdcModelProject1.VisualWebPart1**.|  
    |Tür adı|Button1|  
    |Derleme adı|Güçlü bir derleme adı, örneğin: Microsoft.Office.SharePoint.ClientExtensions, sürüm 14.0.0.0, Culture = neutral, PublicKeyToken = 71e9bce111e9429c =.|  
    |Güvenli|NET **güvenli** onay kutusu.|  
    |Betiğe karşı güvenli|Bırakın **karşı güvenli betik** onay kutusunun işaretini kaldırın.|  
  
    > [!NOTE]  
    >  **Derleme adı** aracılığıyla eklenen derlemeler için değer **Gelişmiş** sekmesinde **paket Tasarımcısı** edilemez bir belirteç olması, bu kesin adlandırılmış bütünleştirilmiş kod olmalıdır. Daha fazla bilgi için [bkz](http://go.microsoft.com/fwlink/?LinkId=177513).  
  
13. Seçin **sekmesini** başka bir güvenli denetim girişi oluşturmak için anahtar.  
  
14. Seçin **yeni bir öğe eklemek için burayı tıklatın** düğmesini tekrar.  
  
15. Değerleri olan özellikler için aşağıdaki tablodan girin.  
  
    |Özellik Adı|Değer|  
    |-------------------|-----------|  
    |Ad Alanı|Tam ad alanı için denetim gibi **BdcModelProject1.VisualWebPart1**.|  
    |Tür adı|TextBox1|  
    |Derleme adı|Güçlü bir derleme adı, örneğin: Microsoft.Office.SharePoint.ClientExtensions, sürüm 14.0.0.0, Culture = neutral, PublicKeyToken = 71e9bce111e9429c =.|  
    |Güvenli|Seçin **güvenli** onay kutusu.|  
    |Betiğe karşı güvenli|Seçin **karşı güvenli betik** onay kutusu.|  
  
16. Seçin **sekmesini** anahtar ve ardından **Tamam** iletişim kutusunu kapatmak için düğme.  
  
## <a name="see-also"></a>Ayrıca bkz.
 [Proje öğelerinde paketleme ve dağıtım bilgileri sağlayın](../sharepoint/providing-packaging-and-deployment-information-in-project-items.md)   
 [Paket ve SharePoint çözümlerini dağıtma](../sharepoint/packaging-and-deploying-sharepoint-solutions.md)  

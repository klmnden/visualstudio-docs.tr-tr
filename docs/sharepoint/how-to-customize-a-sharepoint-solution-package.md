---
title: 'Nasıl yapılır: Bir SharePoint çözüm paketini özelleştirme | Microsoft Docs'
ms.date: 02/02/2017
ms.topic: conceptual
f1_keywords:
- VS.SharePointTools.RAD.PackageDesignerAdvanced
- VS.SharePointTools.RAD.PackageDesigner.Manifest
- VS.SharePointTools.RAD.PackageDesignerProperties
- VS.SharePointTools.RAD.PackageDesigner.SwitchView
dev_langs:
- VB
- CSharp
helpviewer_keywords:
- SharePoint development in Visual Studio, packages
author: John-Hart
ms.author: johnhart
manager: jillfra
ms.workload:
- office
ms.openlocfilehash: 5e1c2e86f489191c3876154143706be4f9b0f1e4
ms.sourcegitcommit: c0202a77d4dc562cdc55dc2e6223c062281d9749
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/24/2019
ms.locfileid: "54874945"
---
# <a name="how-to-customize-a-sharepoint-solution-package"></a>Nasıl yapılır: Bir SharePoint çözüm paketini özelleştirme
  Paket Tasarımcısı oluşturmak ve bir paket özelleştirmek için kullanabileceğiniz (*.wsp*). Örneğin, SharePoint Proje öğeleri ve Özellik Ekle, Web sunucusu çözümü dağıtıldığında sıfırlama ve dağıtım sunucusu türü,'nı belirtin.  
  
## <a name="open-the-package-designer"></a>Paket Tasarımcısı'nı açın  
  
#### <a name="to-open-the-package-designer"></a>Paket Tasarımcısı'nı açmak için
  
-   İçinde **Çözüm Gezgini**, çift **paket**, ya da seçin **Görünüm Tasarımcısı** kısayol menüsünde **paket**.  
  
## <a name="view-the-packaged-manifestffile"></a>Paketlenmiş manifestfFile görüntüleyin  
 Paket Tasarımcısı, paket bildirim dosyası oluşturmak ve değiştirmek için kullanabilirsiniz. Ardından, bu dosya için XML kodu Visual Studio'da görüntüleyebilirsiniz.  
  
#### <a name="to-view-the-xml-source-file"></a>XML kaynak dosyası görüntülemek için  
  
1.  İçinde **paket Tasarımcısı**, seçin **bildirim**.  
  
#### <a name="to-view-the-packaged-manifest-file-by-using-solution-explorer"></a>Paket bildirim dosyası Çözüm Gezgini'ni kullanarak görüntülemek için  
  
1.  İçinde **Çözüm Gezgini**, seçin **tüm dosyaları göster**.  
  
2.  Paket genişletin Package.package genişletin ve ardından açın *Package.Template.xml* dosya.  
  
    > [!NOTE]  
    >  Paket şablon bildirim XML dosyasını açtığınızda, dosyaları otomatik olarak doğrulanır ve Hata Listesi penceresinde görünen uyarıları gözardı edebilirsiniz.  
  
## <a name="change-the-manifest-template"></a>Bildirim şablonu değiştirme  
 Visual Studio XML Düzenleyicisi'ni veya şablon bildirim bölmesini paket bildirim dosyasında XML kodunu değiştirebilirsiniz. XML kodu herhangi bir değişiklik, paket için paket bildirim dosyası kullanılarak birleştirilir.  
  
#### <a name="to-change-the-manifest-template-by-using-the-xml-editor"></a>XML Düzenleyicisi'ni kullanarak bildirim şablonu değiştirmek için  
  
1.  İçinde **paket Tasarımcısı**, seçin **bildirim** sekmesinde, genişletin **düzenleme seçenekleri** düğümünü seçip **XML Düzenleyicisi'nde açık** bağlantı.  
  
     XML değişiklikleri paket bildirim dosyası birleştirilir.  
  
#### <a name="to-change-the-manifest-template-by-using-the-manifest-template-pane"></a>Bildirim şablonu bölmesini kullanarak bildirim şablonu değiştirmek için  
  
1.  İçinde **paket Tasarımcısı**, seçin **bildirim** sekmesinde, genişletme **düzenleme seçenekleri** düğüm ve bildirim şablonu bölmesinde görüntülenen XML değiştirin.  
  
     XML değişiklikleri görünür **paketlenmiş Önizleme, bildirim** bölmesi.  
  
## <a name="overwrite-the-packaged-manifest-file"></a>Paket bildirim dosyasının üzerine yaz  
 Paket Tasarımcısı devre dışı bırakabilir ve oluşturma *manifest.xml* el ile dosya. Bu yordamı gerçekleştirmek ilk kez geçerli ayarları paket Tasarımcısı içinde paket şablonu XML dosyasına kaydedilir. Ardından, değiştirebilir veya XML üzerine yazın.  
  
> [!NOTE]  
>  Bu proje öğeleri ve özellikleri ekleyin veya paket Tasarımcısı devre dışı bırakıldığında, SharePoint Proje öğeleri ve Özellikler XML dosyasında kaldırırsanız, paketlenmiş değildir.  
  
#### <a name="to-overwrite-packaged-manifest-file-by-disabling-the-designer"></a>Tasarımcı devre dışı bırakarak paket bildirim dosyasının üzerine yazmak için  
  
1.  İçinde **paket Tasarımcısı**, seçin **bildirim** sekmesi.  
  
2.  Genişletin **düzenleme seçenekleri** düğümünü seçin **üzerine yaz XML düzenleyicisinde oluşturulan XML'in ve düzenleme bildiriminin** bağlantısını ve ardından **Evet** düğmesi.  
  
     Şablonu geçerli paket bildirim dosyası ile güncelleştirilir.  
  
## <a name="enable-the-package-designer"></a>Paket Tasarımcısı'nı etkinleştir  
 Paket Tasarımcısı özelleştirmek için yeniden etkinleştirebilirsiniz *manifest.xml* dosya.  
  
#### <a name="to-re-enable-the-designer"></a>Tasarımcı yeniden etkinleştirmek için  
  
1.  İçinde **paket Tasarımcısı**, seçin **atma bildirim düzenlemelerini ve yeniden Tasarımcısı'nı etkinleştirmeniz** bağlantısını ve ardından **Evet** düğmesi.  
  
     Orijinal metin şablonu yenilenir ve XML için tüm değişiklikler kaybedilir.  
  
## <a name="see-also"></a>Ayrıca bkz.
 [Paketleme ve SharePoint çözümlerini dağıtma](../sharepoint/packaging-and-deploying-sharepoint-solutions.md)  

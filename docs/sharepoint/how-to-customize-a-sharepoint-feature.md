---
title: 'Nasıl yapılır: Bir SharePoint özelliğini özelleştirme | Microsoft Docs'
ms.date: 02/02/2017
ms.topic: conceptual
f1_keywords:
- VS.SharePointTools.RAD.FeatureDesigner.SwitchView
- VS.SharePointTools.RAD.featureDesigner.Manifest
- VS.SharePointTools.RAD.FeatureDesignerProperties
dev_langs:
- VB
- CSharp
helpviewer_keywords:
- SharePoint development in Visual Studio, features
author: John-Hart
ms.author: johnhart
manager: jillfra
ms.workload:
- office
ms.openlocfilehash: e7a00f3c58f917e7355a63ebca71c74127826a2e
ms.sourcegitcommit: 47eeeeadd84c879636e9d48747b615de69384356
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "63429223"
---
# <a name="how-to-customize-a-sharepoint-feature"></a>Nasıl yapılır: Bir SharePoint özelliğini özelleştirme
  Oluşturun ve Visual Studio özellik Tasarımcısı kullanarak SharePoint özelliklerini özelleştirin. Örneğin, özellik kapsamı ayarlayın ve diğer özellikleri bağımlılıkları olarak ekleyin. Çözüm Gezgini veya SharePoint paket Gezgini içinde yeni bir özellik eklediğinizde, varsayılan olarak, özellik Tasarımcısı açılır.

## <a name="opening-the-feature-designer"></a>Özellik Tasarımcısı açma
 Ekleyebilir veya özellik Tasarımcısı'nı kullanarak bir özelliğin SharePoint Proje öğeleri kaldırın.

#### <a name="to-open-the-feature-designer"></a>Özellik Tasarımcısı'nı açmak için

1. İçinde **Çözüm Gezgini**, genişletme **özellikleri**.

2. Çift *özellik1* öğesini veya kısayol menüsünü açın *özellik1* öğesini ve ardından **Görünüm Tasarımcısı**.

## <a name="view-the-packaged-manifest-file"></a>Paket bildirim dosyasını görüntüleyin
 Özellik Tasarımcısı özellik için paket bildirim dosyası oluşturmak ve değiştirmek için kullanabilirsiniz (*gt;Feature.xml*). Ardından, bu dosya için XML kodu Visual Studio'da görüntüleyebilirsiniz.

#### <a name="to-view-the-packaged-manifest-file"></a>Paket bildirim dosyasını görüntülemek için

1. İçinde **özellik Tasarımcısı**, seçin **bildirim** sekmesi.

#### <a name="to-view-the-packaged-manifest-file-by-using-solution-explorer"></a>Paket bildirim dosyası Çözüm Gezgini'ni kullanarak görüntülemek için

1. İçinde **Çözüm Gezgini**, seçin **tüm dosyaları göster** simgesi.

2. Özellikleri'ni genişletin, FeatureName genişletin, FeatureName.feature genişletin ve ardından açın  *\<FeatureName >. Template.xml* dosya.

    > [!NOTE]
    > Özellik şablon bildirimi XML dosyasını açtığınızda, dosyaları otomatik olarak doğrulanır ve Hata Listesi penceresinde görünen uyarıların yoksayılabilir.

## <a name="change-the-manifest-template"></a>Bildirim şablonu değiştirme
 Özellik bildirimi dosyasını Visual Studio XML Düzenleyicisi'ni veya bildirim şablonu bölmesindeki için XML kodu değiştirebilirsiniz. XML kodu herhangi bir değişiklik, paket bildirim dosyası özellik için birleştirilir. Örneğin, bir özellik özelleştirmek için bildirim şablonu değiştirmek isteyebilirsiniz.

#### <a name="to-change-the-manifest-template-by-using-the-xml-editor"></a>XML Düzenleyicisi'ni kullanarak bildirim şablonu değiştirmek için

1. İçinde **özellik Tasarımcısı**, seçin **bildirim** sekmesinde, genişletin **düzenleme seçenekleri** düğümünü seçip **XML Düzenleyicisi'nde açık** bağlantı.

     XML değişiklikleri paket bildirim dosyası birleştirilir.

#### <a name="to-change-the-manifest-template-by-using-the-manifest-template-pane"></a>Bildirim şablonu bölmesini kullanarak bildirim şablonu değiştirmek için

1. İçinde **özellik Tasarımcısı**, seçin **bildirim** sekmesinde, genişletme **düzenleme seçenekleri** düğüm ve bildirim şablonu bölmesinde görüntülenen XML değiştirin.

     XML değişiklikleri görünür **paketlenmiş Önizleme, bildirim** bölmesi.

## <a name="overwrite-the-packaged-manifest-file"></a>Paket bildirim dosyasının üzerine yaz
 Özellik Tasarımcısı devre dışı bırakabilir ve oluşturma *gt;Feature.xml* el ile dosya. Bu yordamı gerçekleştirmek ilk kez özellik Tasarımcısı'nda geçerli ayarları özellik şablonu XML dosyasına kaydedilir. Ardından, değiştirebilir veya XML üzerine yazın.

> [!NOTE]
> Bu proje öğeleri ekleyin veya özellik Tasarımcısı devre dışıyken XML dosyasında SharePoint Proje öğeleri kaldırın, paketlenmiş değil.

#### <a name="to-overwrite-packaged-manifest-file-by-disabling-the-designer"></a>Tasarımcı devre dışı bırakarak paket bildirim dosyasının üzerine yazmak için

1. İçinde **özellik Tasarımcısı**, seçin **bildirim** sekmesi.

2. Genişletin **düzenleme seçenekleri** düğümünü seçin **üzerine yaz XML düzenleyicisinde oluşturulan XML'in ve düzenleme bildiriminin** bağlantısını ve ardından **Evet** düğmesi.

     Şablonu geçerli paket bildirim dosyası ile güncelleştirilir.

## <a name="enable-the-feature-designer"></a>Özellik Tasarımcısı'nı etkinleştir
 Özelleştirme özellik Tasarımcısı yeniden etkinleştirebilirsiniz *gt;Feature.xml* dosya.

#### <a name="to-re-enable-the-designer"></a>Tasarımcı yeniden etkinleştirmek için

1. İçinde **özellik Tasarımcısı**, seçin **atma bildirim düzenlemelerini ve yeniden Tasarımcısı'nı etkinleştirmeniz** bağlantısını ve ardından **Evet** düğmesi.

2. Orijinal metin şablonu yenilenir ve XML için tüm değişiklikler kaybedilir.

## <a name="see-also"></a>Ayrıca bkz.
- [Paketleme ve SharePoint çözümlerini dağıtma](../sharepoint/packaging-and-deploying-sharepoint-solutions.md)

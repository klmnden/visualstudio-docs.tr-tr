---
title: 'Nasıl yapılır: Özellik bağımlılıkları ekleme ve kaldırma | Microsoft Docs'
ms.date: 02/02/2017
ms.topic: conceptual
f1_keywords:
- MICROSOFT.VISUALSTUDIO.SHAREPOINT.DESIGNERS.CUSTOMDEPENDENCYWINDOW
- VS.SHAREPOINTTOOLS.RAD.FEATUREDESIGNERDEPENDENCY
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
ms.openlocfilehash: 9373ed07ec49bd41dad343dc447b4b2026793492
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62967017"
---
# <a name="how-to-add-and-remove-feature-dependencies"></a>Nasıl yapılır: Ekleme ve kaldırma özellik bağımlılıkları
  SharePoint özelliğinizi işlevi veya verileri diğer özelliklere bağlı olabilir. Bu durumlarda, bu diğer özellikleri özelliğiniz için bağımlılıklar olarak işaretleyebilirsiniz. Bu şekilde, özellik etkinleştirilmeden önce bağımlı özellikleri etkinleştirilir SharePoint sunucusu sağlar.

## <a name="add-dependencies"></a>Bağımlılıkları ekleyin
 Bağımlılıklar olarak çözümünüzdeki diğer özellikler ekleyebilirsiniz. Bu şekilde, gerekli özellikleri yüklü ve özelliğinizi yüklenmeden önce etkinleştirilmiş olduğundan emin yapabilirsiniz.

#### <a name="to-add-a-dependency-on-a-feature-in-the-solution"></a>Bir bağımlılık çözümdeki bir özellik eklemek için

1. Özellik Tasarımcısı'nı açın, **özellik etkinleştirme bağımlılıkları** düğümünü seçip **Ekle** düğmesi.

2. İçinde **özellik etkinleştirme bağımlılıkları Ekle** iletişim kutusunda **çözümdeki özelliklere bir bağımlılık ekleme** seçenek düğmesini, bir bağımlılık olarak eklemek istediğiniz özelliğin başlığını seçin ve ardından seçin **Ekle** düğmesi.

     Seçerken birden çok başlığını seçerek birden fazla özellik ekleyebilirsiniz **Ctrl** anahtarı.

## <a name="addi-custom-dependencies"></a>Addi özel bağımlılıklar
 Bir bağımlılık olarak bir SharePoint sunucu üzerinde zaten dağıtılmış olan özellikleri ekleyebilirsiniz. Bu şekilde özelliğinizi yüklenmeden önce tüm bağımlı özellikler etkinleştirildiğinden emin olmak için SharePoint etkinleştirme işlemini denetler.

#### <a name="to-add-a-dependency-by-the-feature-id"></a>Özellik kimliği ile bir bağımlılık eklemek için

1. Özellik Tasarımcısı'nı açın, **özellik etkinleştirme bağımlılıkları** düğümünü seçip **Ekle** düğmesi.

2. İçinde **özellik etkinleştirme bağımlılıkları Ekle** iletişim kutusunda **özel bağımlılık Ekle** seçenek düğmesini.

3. İçinde **özellik kimliği** metin kutusunda, bir etkinleştirme bağımlılık olarak işaretleyin ve ardından istediğiniz özellik için GUID girin **Ekle** düğmesi.

## <a name="edit-custom-dependencies"></a>Özel bağımlılıklar Düzenle
 Daha önce eklemiş olduğunuz özel bağımlılıklar düzenleyebilirsiniz. Ancak, yalnızca, çözüm can kaldırılır, bağımlı özellik düzenlenemez.

#### <a name="to-change-a-dependency-on-a-feature-in-the-solution"></a>Bir çözümdeki bir özellik bağımlılığı değiştirmek için

1. Özellik Tasarımcısı'nı açın ve ardından **özellik etkinleştirme bağımlılıkları** düğümü.

2. Düzenleyin ve ardından istediğiniz özelliğin adını seçin **Düzenle** düğmesi.

3. İçinde **özel özellik etkinleştirme bağımlılığı Düzenle** iletişim kutusu, başlık, özellik Kimliğine veya açıklamasına değiştirin ve ardından **Gönder** düğmesi.

## <a name="remove-dependencies"></a>Bağımlılıkları kaldırın

#### <a name="to-remove-a-dependency-on-a-feature-in-the-solution"></a>Çözümdeki bir özellik üzerinde bir bağımlılık kaldırmak için

1. Özellik Tasarımcısı'nda genişletin **özellik etkinleştirme bağımlılıkları** düğümünü kaldırın ve ardından istediğiniz özelliğin adını seçin **Kaldır** düğmesi.

## <a name="see-also"></a>Ayrıca bkz.
- [SharePoint özellikleri oluşturma](../sharepoint/creating-sharepoint-features.md)
- [Nasıl yapılır: Bir SharePoint özelliğini özelleştirme](../sharepoint/how-to-customize-a-sharepoint-feature.md)
- [Nasıl yapılır: SharePoint özelliklerine öğe ekleyip](../sharepoint/how-to-add-and-remove-items-to-sharepoint-features.md)

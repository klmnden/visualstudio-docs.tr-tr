---
title: 'Nasıl yapılır: SharePoint dağıtım yapılandırmasını düzenleme | Microsoft Docs'
ms.date: 02/02/2017
ms.topic: conceptual
f1_keywords:
- VS.SharePointTools.Project.DeploymentConfig
dev_langs:
- VB
- CSharp
helpviewer_keywords:
- SharePoint development in Visual Studio, deploying
author: John-Hart
ms.author: johnhart
manager: jillfra
ms.workload:
- office
ms.openlocfilehash: ffa7923bbe7e8a7b44fec280a5528ab023feed37
ms.sourcegitcommit: 47eeeeadd84c879636e9d48747b615de69384356
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "63444704"
---
# <a name="how-to-edit-a-sharepoint-deployment-configuration"></a>Nasıl yapılır: SharePoint dağıtım yapılandırmasını düzenleme
  Bir dağıtım yapılandırması oluşturun veya var olan bir dağıtım yapılandırmasını Değiştir. Örneğin, tek bir adım çalıştırın veya dağıtım işlemindeki adımları sırasını değiştirin. Yapılandırmaları oluşturmak veya yerleşik ve program aracılığıyla eklenen yapılandırmaları değiştirilemediğinden dağıtım değiştirmek isteyebilirsiniz.

## <a name="create-a-sharepoint-deployment-configuration"></a>SharePoint dağıtım yapılandırmasını oluşturma

#### <a name="to-create-a-sharepoint-deployment-configuration"></a>SharePoint dağıtım yapılandırmasını oluşturmak için

1. İçinde **Çözüm Gezgini**, bir SharePoint proje seçin ve ardından, menü çubuğunda, **proje**, _ProjectName_**özellikleri**.

2. Üzerinde **SharePoint** sekmesini, **yeni** düğmesi.

     **Yeni dağıtım yapılandırması Ekle** iletişim kutusu görüntülenir.

3. İçinde **adı** metin kutusunda, dağıtım yapılandırması için bir ad girin.

4. İçinde **kullanılabilir dağıtım adımları** bölmesinde için Dağıtım Yapılandırması Ekle öğesini istediğiniz adımları seçin (**>**) düğmesini ve ardından **Tamam** düğmesi.

    > [!NOTE]
    > Yalnızca bir özelleştirilmiş dağıtım yapılandırması için eklerseniz, dağıtım öncesi komutu veya dağıtım sonrası komutu yapılandırdıysanız, aşağıdaki adımları çalıştırın.

## <a name="change-the-active-deployment-configuration"></a>Etkin dağıtım yapılandırması değiştirme

#### <a name="to-change-the-active-deployment-configuration"></a>Etkin dağıtım yapılandırmasını değiştirmek için

1. İçinde **Çözüm Gezgini**, bir SharePoint proje seçin ve ardından, menü çubuğunda, **proje** > **\<*ProjectName*> Özellikleri**.

2. Seçin **SharePoint** sekmesi.

3. İçinde **etkin Dağıtım Yapılandırması** liste kutusunda, kullanmak istediğiniz dağıtım yapılandırmasının adı seçin.

## <a name="see-also"></a>Ayrıca bkz.
- [Paketleme ve SharePoint çözümlerini dağıtma](../sharepoint/packaging-and-deploying-sharepoint-solutions.md)

---
title: 'Nasıl yapılır: Bir modül kullanarak dosyaları içerme | Microsoft Docs'
ms.date: 02/02/2017
ms.topic: conceptual
dev_langs:
- VB
- CSharp
helpviewer_keywords:
- SharePoint development in Visual Studio, modules
- modules [SharePoint development in Visual Studio]
author: John-Hart
ms.author: johnhart
manager: jillfra
ms.workload:
- office
ms.openlocfilehash: 5813a6f89062bf53f7f8c0b57b4ed3a8ef9c4edf
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62813650"
---
# <a name="how-to-include-files-by-using-a-module"></a>Nasıl yapılır: Bir modül kullanarak dosyaları içerme
  *Modüller* (ile karıştırılmamalıdır [!INCLUDE[vbprvb](../sharepoint/includes/vbprvb-md.md)] modülleri) dosyaları gibi ASPX ana sayfalar, metin dosyaları ya da görüntülerini SharePoint'e dağıtmanıza olanak tanıyan kapsayıcılardır.

 Belge kitaplığına veya normal bir dosya (örneğin, default.aspx) gibi bir dosya dağıtmak bir belge kitaplığı dışında seçebilirsiniz. Bir belge kitaplığına bir dosya eklemek için belirtin `Type="GhostableInLibrary"` özniteliği olarak **dosya** öğesi. SharePoint kitaplığına eklendiğinde dosyanızla gitmek için bir liste öğesi oluşturmak için bu ayarı bildirir. Bir belge kitaplığının dışındaki bir dosya dağıtmak için seçeneklerinden birini belirtin `Type="Ghostable"` veya yalnızca çıkarın **türü** özniteliği.

## <a name="add-a-module-to-a-sharepoint-solution"></a>Bir modül için bir SharePoint çözümünü ekleyin

#### <a name="to-add-a-module"></a>Bir modül eklemek için

1. İçinde [!INCLUDE[vsprvs](../sharepoint/includes/vsprvs-md.md)]bir SharePoint projesi oluşturun veya açın.

     Daha fazla bilgi için [SharePoint projesi ve proje öğesi şablonları](../sharepoint/sharepoint-project-and-project-item-templates.md).

2. İçinde **Çözüm Gezgini**, proje düğümünü seçin ve ardından, menü çubuğunda, **proje** > **Yeni Öğe Ekle**.

     **Yeni Öğe Ekle** iletişim kutusu açılır.

3. SharePoint şablonları listesinde seçin **Modülü** şablonu seçip **Ekle** düğmesi.

     Bu adımda, bir düğüm Module1 adlı projede oluşturulur.

4. Module1'ın altında Sil *örnek.txt* dosya.

     Örnek.txt tüm yeni modüller örneğin amacıyla bulunur ve gerekli değildir. (Dosyayı silme da girdisini modülün kaldırır, Not *Elements.xml* dosyası.)

5. Dosyaları SharePoint'teki belirli bir klasör yapısı dağıtmak istiyorsanız, bu klasörleri Module1 altında oluşturma [!INCLUDE[vsprvs](../sharepoint/includes/vsprvs-md.md)] Module1 düğüm seçerek ve ardından, menü çubuğundan seçme **proje**, **yeni Klasör**.

6. Dosyayı ekleyin ve ardından menü çubuğunda, istediğiniz klasörü seçin **proje**, **varolan öğeyi Ekle**.

7. SharePoint'e dağıtmanıza ve ardından istediğiniz bir veya daha fazla dosya seçin **Ekle** düğmesi.

     Projeye bir dosya eklediğinizde, bunun için bir giriş için modülün Elements.xml dosyası otomatik olarak eklenir. Proje dağıtılırken, dosyalar tarafından belirtilen proje kök dizinine göreli bir SharePoint sunucusuna kopyalanır **dosya** öğenin **Url** gibi öznitelik `Url="Module1/New Folder/SomeFile.doc`. Dağıtım konumu bir dosya için değiştirmek istiyorsanız, ya da başka bir klasöre taşıyın **Çözüm Gezgini** veya değiştirmek, **Url** ayarı.

8. Bir belge kitaplığındaki görünmesini istediğiniz tüm dosyaları için ekleme `Type="GhostableInLibrary"` girdisini özniteliği *Elements.xml*. Örneğin,

    ```xml
    <File Path="Module1\Some Folder\SomePage.aspx" Url="Module1/Some Folder/SomePage.aspx" Type="GhostableInLibrary" />
    ```

9. Projeyi dağıtın.

     SharePoint içinde belirtilen konuma dosyaları kopyalayın.

## <a name="see-also"></a>Ayrıca bkz.
- [Paketleme ve SharePoint çözümlerini dağıtma](../sharepoint/packaging-and-deploying-sharepoint-solutions.md)
- [SharePoint Çözümleri Geliştirme](../sharepoint/developing-sharepoint-solutions.md)

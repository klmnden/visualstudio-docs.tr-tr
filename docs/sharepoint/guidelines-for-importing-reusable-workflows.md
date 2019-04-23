---
title: Yeniden kullanılabilir iş akışlarını içeri aktarma yönergeleri | Microsoft Docs
ms.date: 02/02/2017
ms.topic: conceptual
dev_langs:
- VB
- CSharp
helpviewer_keywords:
- SharePoint development in Visual Studio, importing items
- SharePoint development in Visual Studio, reusable workflows
- importing items [SharePoint development in Visual Studio]
- reusable workflows [SharePoint development in Visual Studio]
author: John-Hart
ms.author: johnhart
manager: jillfra
ms.workload:
- office
ms.openlocfilehash: bb386a2d80931ece415b0b3939f2947678808261
ms.sourcegitcommit: 1fc6ee928733e61a1f42782f832ead9f7946d00c
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/22/2019
ms.locfileid: "60041227"
---
# <a name="guidelines-for-importing-reusable-workflows"></a>Yeniden kullanılabilir iş akışlarını içeri aktarma yönergeleri
  SharePoint Tasarımcısı'nda oluşturulan yeniden kullanılabilir iş akışlarını içeri aktarmak için yeniden kullanılabilir SharePoint 2010 iş akışını içe proje şablonunda kullanmak [!INCLUDE[vsprvs](../sharepoint/includes/vsprvs-md.md)]. Bu şablon alır bir *bildirim temelli* *iş akışı* ([!INCLUDE[TLA2#tla_xml](../sharepoint/includes/tla2sharptla-xml-md.md)]-yalnızca) ve içine dönüştürür bir *iş akışı kodu*, ikisiyle geliştiren bir iş akışı olduğu [!INCLUDE[vbprvb](../sharepoint/includes/vbprvb-md.md)] veya [!INCLUDE[csprcs](../sharepoint/includes/csprcs-md.md)] kod. [!INCLUDE[crdefault](../sharepoint/includes/crdefault-md.md)] [İzlenecek yol: Bir SharePoint Tasarımcısı yeniden kullanılabilir iş akışını Visual Studio'ya içeri aktarma](../sharepoint/walkthrough-import-a-sharepoint-designer-reusable-workflow-into-visual-studio.md).

 Ancak, yeniden kullanılabilir SharePoint 2010 iş akışını içeri aktarma şablonu sadece grup çözümlerini içeri aktarabilirsiniz. İş akışınızı bir korumalı çözüm olarak dağıtmak istiyorsanız, SharePoint 2010 çözüm paketini içeri aktarma şablonla içeri aktarın. Ancak, bunu yaparak iş akışı kodu üzere dönüştüremezsiniz ve bu nedenle değiştirmek mümkün olmayacaktır.

## <a name="import-reusable-workflows-by-using-the-import-reusable-workflow-template"></a>Yeniden kullanılabilir iş akışlarını içeri aktarma yeniden kullanılabilir iş akışı şablonu kullanarak içeri aktarın.
 Yeniden kullanılabilir SharePoint 2010 iş akışını içeri aktarma şablonu kullanarak bir yeniden kullanılabilir iş akışını içeri aktarırsanız, çalıştırmak veya çözüm gibi diğer değiştirmek [!INCLUDE[vsprvs](../sharepoint/includes/vsprvs-md.md)] SharePoint çözüm, ancak bazı öğeleri el ile düzeltmeniz olabilir.

### <a name="import-task-forms"></a>Al görevi formlar
 Yeniden kullanılabilir SharePoint 2010 iş akışını içeri aktar proje şablonu, tüm başlatma ve ilişkilendirme formları alır, ancak kodu iş akışı şema yalnızca bir görev form izin verdiği için yalnızca bir görev formu alır. Özgün iş akışı çözümü herhangi bir ek görev formlardan yerleştirerek **diğer içeri aktarılan dosyaları** klasöründe **Çözüm Gezgini**.

## <a name="import-reusable-workflows-by-using-the-import-sharepoint-2010-solution-package-template"></a>SharePoint 2010 çözüm paketini İçeri Aktar şablonu kullanarak yeniden kullanılabilir iş akışlarını içeri aktarma
 SharePoint 2010 çözüm paketini içeri aktarma şablonu kullanarak bir yeniden kullanılabilir iş akışını içeri aktarırsanız, aşağıdaki konuları göz önünde bulundurmanız gerekir:

- İş akışını içeri aktardıktan sonra hemen dağıtabilir ve çalıştırabilir [!INCLUDE[vsprvs](../sharepoint/includes/vsprvs-md.md)] seçerek **F5** anahtarı. Ancak, içeri aktarılan çözümdeki iş akışındaki herhangi bir ayarı değiştirmek, dağıtma ve iş akışını çalıştırmak için önce öğeleri projede el ile düzeltmeniz gerekebilir.

- İş akışı bildirime dayalı olduğu için kod eklenemiyor. Bir kod iş akışına iş akışı dönüştürmek için içine almalısınız [!INCLUDE[vsprvs](../sharepoint/includes/vsprvs-md.md)] yeniden kullanılabilir SharePoint 2010 iş akışını içeri aktarma şablonunu kullanarak.

- İş Akışı Tasarımcısı (.xoml) dosyasını Tasarım görünümünde düzenleyebilir, ancak iş akışı Tasarımcısı yanlış hatalar görüntülediğinden Kaynak Görünümü'nde Düzenle önerilir.

- İş akışında hata ayıklama için bildirim temelli içeriği çalışmaz. Kesme noktaları ayarlayın [!INCLUDE[wfd2](../sharepoint/includes/wfd2-md.md)] isabet değil.

## <a name="import-globally-reusable-workflow-solutions"></a>Genel olarak yeniden kullanılabilir iş akışı çözümleri alın
 Genel olarak yeniden kullanılabilir iş akışlarını içeri aktarma yeniden kullanılabilir SharePoint 2010 iş akışı şablonu kullanarak içeri aktarılamaz. Genel olarak yeniden kullanılabilir iş akışı almak için bir genel olmayan yeniden kullanılabilir iş akışına dönüştürmek sahip olduğunuz veya SharePoint 2010 çözüm paketini içeri aktarma şablonu kullanmak zorunda.

 İş akışını dönüştürmek için SharePoint Tasarımcısı'nda genel olarak yeniden kullanılabilir iş akışı bir kopyasını oluşturun (iş akışı için kısayol menüsünü açarak ve ardından **kopyayı Farklı Kaydet**). Ardından yeniden kullanılabilir SharePoint 2010 iş akışını içeri aktarma şablonuyla yeni yeniden kullanılabilir iş akışını içeri [!INCLUDE[vsprvs](../sharepoint/includes/vsprvs-md.md)].

 Değişiklik yapmadan genel olarak yeniden kullanılabilir iş akışını içeri aktarmak için SharePoint 2010 çözüm paketini içeri aktarma şablonu kullanın. Bu yöntemi kullandığınızda, iş akışı bir kod iş akışına dönüştürülmüş değil ve bildirim temelli bir iş akışı kalır.

## <a name="see-also"></a>Ayrıca bkz.
- [Mevcut bir SharePoint sitesinden öğeleri içeri aktarma](../sharepoint/importing-items-from-an-existing-sharepoint-site.md)
- [İzlenecek yol: Bir SharePoint Tasarımcısı yeniden kullanılabilir iş akışını Visual Studio'ya içeri aktarma](../sharepoint/walkthrough-import-a-sharepoint-designer-reusable-workflow-into-visual-studio.md)

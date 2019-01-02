---
title: İş verilerini SharePoint ile tümleştirme | Microsoft Docs
ms.date: 02/02/2017
ms.topic: conceptual
dev_langs:
- VB
- CSharp
helpviewer_keywords:
- Business Data Connectivity service [SharePoint development in Visual Studio], business data
- BDC [SharePoint development in Visual Studio], aggregating data
- BDC [SharePoint development in Visual Studio], business data
- Business Data Connectivity service [SharePoint development in Visual Studio], aggregating data
- BDC [SharePoint development in Visual Studio], creating a model
- Business Data Connectivity service [SharePoint development in Visual Studio], creating a model
- Business Data Connectivity service [SharePoint development in Visual Studio], data
- BDC [SharePoint development in Visual Studio], data
author: TerryGLee
ms.author: tglee
manager: douge
ms.workload:
- office
ms.openlocfilehash: 194f2e0c88a0cbce9ef34f77246cf7969066833e
ms.sourcegitcommit: 37fb7075b0a65d2add3b137a5230767aa3266c74
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/02/2019
ms.locfileid: "53934446"
---
# <a name="integrate-business-data-into-sharepoint"></a>İş verilerini SharePoint ile tümleştirme
  İş verilerini SharePoint ile tümleştirebilirsiniz. İş verileri yeniden ziyaret edebilir, arka uç sunucu uygulamalarından gibi [!INCLUDE[TLA#tla_sqlsvr](../sharepoint/includes/tlasharptla-sqlsvr-md.md)], Siebel ve SAP, veya bir Web hizmeti. Kullanıcılar görüntüleme, ekleme, güncelleştirme veya dış listeleri ya da iş verilerini SharePoint Web Bölümleri'ni kullanarak iş verilerini sil.  Kullanıcılar bu verileri çevrimdışı Microsoft Outlook gibi bir Microsoft Office uygulamasında erişebilir. Daha fazla bilgi için [burada olabilir, dış verileri Göster](http://go.microsoft.com/fwlink/?LinkId=169295).  
  
 Verilerini SharePoint ile tümleştirmek için İş Verileri Bağlantısı (BDC) hizmeti için bir modeli oluşturun. BDC hizmeti, SharePoint'te iş uygulamalarında verilerle ilgili bilgileri depolayan bir uygulamadır. Daha fazla bilgi için [İş Verileri Bağlantısı (BDC) hizmeti](http://go.microsoft.com/fwlink/?LinkID=169276).  
  
## <a name="models-in-visual-studio"></a>Visual Studio'da modelleri  
 Visual Studio'da modelleri almak ve arka uç veri kaynaklarından alınan verileri güncelleştirmek için özel kod yazmanıza olanak sağlar. Ayrıca birden çok veri kaynaklarından alınan verileri kullanabilirsiniz. Örneğin, verileri içeren müşterilerin listesini görüntüleyebileceğiniz bir [!INCLUDE[ssNoVersion](../sharepoint/includes/ssnoversion-md.md)] veritabanı ve bir Web hizmeti.  
  
 Ayrıca, SharePoint'e zaten dağıtılmış olan modeli içeri aktarabilirsiniz. Bir modeli içeri aktardıktan sonra özel kod ekleyebilir veya yalnızca paketleme ve birden çok SharePoint sunucu grupları için model dağıtma için Visual Studio'yu kullanın. Daha fazla bilgi için [iş verileri bağlantı modeli oluşturma](../sharepoint/creating-a-business-data-connectivity-model.md).  
  
## <a name="design-a-model-in-visual-studio"></a>Visual Studio'da bir model tasarlama
 Bir tasarımcı ve birkaç araç pencerelerini kullanarak bir model tasarlayabilirsiniz. Model tasarlarken, Visual Studio XML modeli oluşturur. Daha fazla bilgi için [BDC modeli Tasarım araçları genel bakış](../sharepoint/bdc-model-design-tools-overview.md).  
  
 Bir model, varlıkları ve yöntemleri içerir.  
  
### <a name="entities"></a>Varlıklar  
 Bir varlık koleksiyonu alanları açıklar. Örneğin, bir varlık, bir veritabanındaki bir tabloda temsil edebilir. Bir varlık, SharePoint'te bir dış içerik türü olarak görünür. Dış içerik türleri hakkında daha fazla bilgi için bkz. [dış içerik türleri nelerdir?](http://go.microsoft.com/fwlink/?LinkId=169293)  
  
### <a name="methods"></a>Yöntemler  
 Bir varlığın alanları bir eylemi gerçekleştirmek için bir dış içerik türü tüketicilerinin bir yöntem sağlar. Örneğin, bir güncelleyici yöntemi adresini değiştirmek kullanıcıların ve doğum tarihi bir müşterinin nerede `Address` ve `BirthDate` , alanlar `Customer` varlık.  
  
 Visual Studio, modelinizde her varlık için bir hizmet kodu dosyası oluşturur. Bir yöntem modelinize eklediğiniz zaman Visual Studio hizmeti kod dosyasını karşılık gelen bir yöntem oluşturur. Her yönteme uygun görev gerçekleştirmek için kod ekleyin. Örneğin, Visual Studio modele bir yaratıcı yöntemi ekleme, hizmet kod dosyanıza bir yaratıcı yöntemi oluşturur. Kullanıcı tıkladığında bu yöntem BDC hizmeti tarafından çağrılır **yeni öğe** modelini temel alan bir liste düğmesi. Bu nedenle, bir veri kaynağına yeni veri ekleyen Oluşturucu yöntemine kodu ekleyin. Daha fazla bilgi için [iş verileri bağlantı modeli tasarlama](../sharepoint/designing-a-business-data-connectivity-model.md).  
  
## <a name="related-topics"></a>İlgili konular
  
|Başlık|Açıklama|  
|-----------|-----------------|  
|[İş verileri bağlantı modeli oluşturma](../sharepoint/creating-a-business-data-connectivity-model.md)|Nasıl yeni bir model oluşturmak veya dışarı aktarmak istediğiniz SharePoint'ten model içeri aktarma gösterir.|  
|[İş verileri bağlantı modeli tasarlama](../sharepoint/designing-a-business-data-connectivity-model.md)|Visual Studio tasarım araçlarını kullanarak bir model öğelerini tasarım açıklanmaktadır.|  
|[Ne zaman vs SharePoint Designer'ı kullanın. Visual Studio oluştururken çözümleri BCS kullanma](http://go.microsoft.com/fwlink/?LinkID=183448)|Visual Studio veya BDC modeli oluşturmak için SharePoint Designer'ı kullanın karar vermenize yardımcı olur.|  

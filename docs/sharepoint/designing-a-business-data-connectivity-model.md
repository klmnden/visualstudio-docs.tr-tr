---
title: İş verileri bağlantı modeli tasarlama | Microsoft Docs
ms.date: 02/02/2017
ms.topic: conceptual
dev_langs:
- VB
- CSharp
helpviewer_keywords:
- BDC [SharePoint development in Visual Studio], designing a model
- Business Data Connectivity service [SharePoint development in Visual Studio], designing a model
author: John-Hart
ms.author: johnhart
manager: jillfra
ms.workload:
- office
ms.openlocfilehash: 8f322d18afdb8e14ee87ae31d30dd6bdd57b07c5
ms.sourcegitcommit: 47eeeeadd84c879636e9d48747b615de69384356
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "63431295"
---
# <a name="design-a-business-data-connectivity-model"></a>İş verileri bağlantı modeli tasarlama
  Varlıklar ve yöntemleri için bir model dosyası ekleyerek iş verileri bağlantısı (BDC) hizmeti için bir model geliştirebilirsiniz. Bir varlık koleksiyonu veri alanlarını açıklar. Örneğin, bir varlık, bir veritabanındaki bir tabloda temsil edebilir. Bir yöntemi ekleme, silme veya varlıklar tarafından temsil edilen veri güncelleştirme gibi bir görevi gerçekleştirir. Daha fazla bilgi için [iş verilerini SharePoint ile tümleştirmeyi](../sharepoint/integrating-business-data-into-sharepoint.md).

## <a name="add-entities"></a>Varlık ekleme
 Bir varlık sürükleyerek veya kopyalayarak ekleyebilirsiniz bir **varlık** Visual Studio'dan **araç kutusu** İVB tasarımcıya. Daha fazla bilgi için [nasıl yapılır: Modele bir varlık ekleme](../sharepoint/how-to-add-an-entity-to-a-model.md).

 Varlık alanlarını bir sınıfta tanımlayın. Örneğin, adında bir alan ekleyebilirsiniz `Address` için bir `Customer` sınıfı. Projeye yeni bir sınıf ekleyin veya Object Relational Designer (O/R Tasarımcısı) gibi diğer araçları kullanarak oluşturduğunuz var olan bir sınıfı kullanın. Varlık adı ve varlığı temsil eden sınıf adı eşleşen gerek kalmaz. Modelinizde yöntemleri tanımlarken varlık sınıfı ilgilidir.

## <a name="add-methods"></a>Yöntem ekleme
 Kullanıcıları görüntülemek, ekleme, güncelleştirme veya silme bilgileri bir liste veya, modelini temel alan bir Web Bölümü, BDC hizmeti modelinizde yöntemleri çağırır. Model kullanıcının gerçekleştirebileceği her görev için bir yöntem eklemeniz gerekir. Beş temel yöntemi türlerinden birini seçerek yöntemleri oluşturun **BDC yöntem ayrıntıları** penceresi. Aşağıdaki tabloda, BDC modeli beş temel yöntemlerini açıklar.

|Yöntem|Açıklama|
|------------|-----------------|
|Bulucu|Varlığın örneklerinin bir koleksiyonunu döndürür. Liste veya Web Bölümü, kullanıcı oturum açtığında çağrılır. Daha fazla bilgi için [nasıl yapılır: Bir Bulucu yöntemi eklemek](../sharepoint/how-to-add-a-finder-method.md).|
|Belirli Bir Bulucu|Bir özel varlık örneğini döndürür. Bir kullanıcı bir listede belirli bir öğenin ayrıntılarını görüntüleyen çağrılır. Daha fazla bilgi için [nasıl yapılır: Belirli bir Bulucu yöntemi eklemek](../sharepoint/how-to-add-a-specific-finder-method.md).|
|Oluşturucu|Bir varlığın veri kaynağına yeni veri ekler. Kullanıcılar seçtiğinde çağırılır **yeni öğe** modelini temel alan bir listenin Şeritteki düğme. Daha fazla bilgi için [nasıl yapılır: Bir yaratıcı metodu ekleme](../sharepoint/how-to-add-a-creator-method.md).|
|Güncelleştirici|Bir listedeki veri değiştirir. Kullanıcıların bir liste bilgilerinde güncelleştirdiğinizde çağrılır. Daha fazla bilgi için [nasıl yapılır: Bir güncelleyici metodu ekleme](../sharepoint/how-to-add-an-updater-method.md).|
|Silici|Verileri kaldırır. Kullanıcılar, listeden bir öğeyi silme çağrılır. Daha fazla bilgi için [nasıl yapılır: Silici metodu ekleme](../sharepoint/how-to-add-a-deleter-method.md).|

## <a name="define-method-parameters"></a>Yöntem parametreleri tanımlayın
 Bir yöntem oluşturduğunuzda, Visual Studio yöntem türü için uygun olan giriş ve çıkış parametrelerini ekler. Bu parametreler yalnızca tutuculardır. Çoğu durumda, böylece geçirin veya doğru veri türünü dönüş parametreleri değiştirmeniz gerekir. Örneğin, varsayılan olarak, bir Bulucu yöntemi bir dize döndürür. Çoğu durumda, böylece bir varlık koleksiyonunu döndürür dönüş parametresi Bulucu metodunu değiştirmek istediğiniz. Bu parametrenin tür tanımlayıcısını değiştirerek gerçekleştirebilirsiniz. Bir tür tanımlayıcı bir parametrenin veri türünü tanımlayan bir öznitelik koleksiyonudur. Daha fazla bilgi için [nasıl yapılır: Bir parametrenin tür tanımlayıcısını tanımlama](../sharepoint/how-to-define-the-type-descriptor-of-a-parameter.md).

 Visual Studio modelinde parametreleri arasında tür tanımlayıcısı kopyalanacağı sağlar. Örneğin, bir tür tanımlayıcı adlı tanımlayabilir `CustomerTD` dönüş parametresi için `GetCustomer` yöntemi. Kopyalayabilirsiniz `CustomerTD` tür tanımlayıcısı olarak **BDC Gezgini**ve bu tür tanımlayıcıyı giriş parametresine yapıştırın `CreateCustomer` yöntemi. Bu, birden çok kez aynı tür tanımlayıcısını tanımlamak zorunda kalmasını önler.

## <a name="method-instances"></a>Yöntem örnekleri
 Bir yöntem oluşturduğunuzda, Visual Studio varsayılan metot örneği ekler. Metot örneği bir yöntemin yanı sıra, parametrelerin varsayılan değerleri bir başvurudur. Tek bir yöntemi, birden çok yöntem örneği olabilir. Her yöntem imzası bir birleşimi ve varsayılan değerleri kümesi örneğidir. Daha fazla bilgi için [nasıl yapılır: Bir parametrenin tür tanımlayıcısını tanımlama](../sharepoint/how-to-define-the-type-descriptor-of-a-parameter.md).

 Projeyi çalıştırdığınızda, SharePoint listesinin üstünde bir açılan listedeki yöntemi örnekleri görüntülenir. Kullanıcılar verileri görüntülemek için yöntem örneklerini seçebilirler.

 Metot örneği için varsayılan değerler eklemek için model XML'sini doğrudan değiştirmeniz gerekir. Daha fazla bilgi için [DefaultValue](http://go.microsoft.com/fwlink/?LinkID=169279).

## <a name="add-filter-descriptors"></a>Filtre tanımlayıcısı ekleme
 Tüketiciler modelin bazı ölçütlerle eşleşen bir varlığın örneklerinin almak isteyebilirsiniz. Bu özelliği etkinleştirmek için bir yöntem için bir filtre tanımlayıcısı ekleyebilirsiniz. Filtre tanımlayıcıları, yürütmeden önce yöntemlere değerler geçirerek yöntemi sonuç kümesini filtrelemek model tüketiciler etkinleştirin. Daha fazla bilgi için [nasıl yapılır: Dış sistemden örneklerini sınırlandırmak için işlemleri filtre parametrelerini eklemek](http://go.microsoft.com/fwlink/?LinkID=169267).

 SharePoint filtre değerlerini sağlamak için kullanıcıların sağlayan birçok özellik sunar. Örneğin, iş verileri Web bölümlerini bir filtre metin kutusunda belirtin. Kullanıcılar, metin kutusuna bir değer girerek listesindeki verileri sınırlayabilirsiniz. Bir yönteme bir filtre tanımlayıcısı ekleme hakkında daha fazla bilgi için bkz. [nasıl yapılır: Bir Bulucu metoduna filtre tanımlayıcısı ekleme](../sharepoint/how-to-add-a-filter-descriptor-to-a-finder-method.md).

### <a name="filter-descriptor-properties"></a>Filtre tanımlayıcısı özellikleri
 Değerini ayarlamalısınız **ilişkili tür tanımlayıcı**, **adı**, ve **türü** özelliklerini filtre tanımlayıcısı. Diğer tüm özellikleri isteğe bağlıdır.

 **İlişkili tür tanımlayıcı** özelliği ilişkili filtre tanımlayıcısı için bir giriş parametresi. Bir kullanıcı bir filtre değeri sağladığında, BDC hizmeti girdi parametresini kullanarak bu değeri yönteme geçirir.

 **Türü** özelliği, kullanmak istediğiniz filtre deseni açıklar. SharePoint'te, seçtiğiniz filtre deseni kullanıcı arabirimi (UI) içinde görüntülenen metni etkiler. Örneğin, metin bir karşılaştırıcı filtre deseni için **eşittir** yukarıda bir iş verileri Web Bölümü bir denetimi olarak görünür. Her filtre desen hakkında daha fazla bilgi için bkz: [, filtre tarafından desteklenen türleri İVB](http://go.microsoft.com/fwlink/?LinkId=169287).

 Filtre tanımlayıcısı özellikleri hakkında daha fazla bilgi için bkz. [FilterDescriptor](http://go.microsoft.com/fwlink/?LinkID=169280).

### <a name="provide-default-values"></a>Varsayılan değerleri sağlayın
 Bazı durumlarda, kullanıcı bir filtre değeri sağlamayabilir. Metot örneği için varsayılan değer ekleme veya varsayılan değer yönteminizi kodda ayarlayarak, varsayılan bir değer sağlayabilirsiniz. Metot örneği için varsayılan değer ekleme hakkında daha fazla bilgi için bkz. [MethodInstance](http://go.microsoft.com/fwlink/?LinkID=169282). Yönteminizi kodda bir giriş parametresinin varsayılan değeri ayarlamak nasıl bir örnek için bkz [nasıl yapılır: Bir Bulucu metoduna filtre tanımlayıcısı ekleme](../sharepoint/how-to-add-a-filter-descriptor-to-a-finder-method.md).

## <a name="validate-the-model"></a>Model doğrulama
 Geliştirme sırasında modelinizi doğrulayabilirsiniz. Visual Studio modelinizi beklendiği gibi davrandığından dan engelleyen sorunları tanımlar. Bu sorunlar Visual Studio'da görünür **hata listesi**.

 İVB Tasarımcısı için kısayol menüsünü açarak ve ardından bir model doğrulama **doğrulama**. Model hataları içeriyorsa, görünürler **hata listesi**. Listede hataya çift tıklayarak bir hata içeriyor kodu için imleci hızlı bir şekilde taşıyabilirsiniz. Alternatif olarak, seçtiğiniz **F8** veya **Shift**+**F8** art arda adım ileriye veya geriye dönük listesinde hatalar arasında anahtarları.

 Başka bir yolla model kurallarını ihlal edildiğinde doğrulama hataları oluşabilir. Örneğin, varsa **IsCollection** özelliği, bir tür tanımlayıcı **true**, ancak mevcut hiçbir alt tür tanımlayıcısı, bir doğrulama hatası görünür. Visual Studio'da görünen bazı hatalar anlamak için bir İVB Modeli kurallarına başvurmak zorunda kalabilirsiniz **hata listesi**. Bir BDC modeli kuralları hakkında daha fazla bilgi için bkz. [BDCMetadata şema](http://go.microsoft.com/fwlink/?LinkID=169275).

## <a name="debug-the-solution-that-contains-the-model"></a>Modeli içeren bir çözüme hata ayıklaması
 Herhangi bir kod Visual Studio'da yaptığınız gibi kodunuzu ayıklayabilirsiniz. Kodunuzdaki hataları ayıklamak için kesme noktaları her yerde kodunuzda ayarlayın ve ardından hata ayıklayıcıyı başlatın. Visual Studio SharePoint sitesi açılır. SharePoint'te bir liste veya iş verilerinizi kullanan Web bölümü oluşturun. Ardından, kodunuzda adım adım ilerleyebilirsiniz. SharePoint projelerinde hata ayıklama hakkında daha fazla bilgi için bkz. [sorun giderme SharePoint çözümleri](../sharepoint/troubleshooting-sharepoint-solutions.md).

 Projeye Ekle özel bütünleştirilmiş kod hata ayıklaması yapabilirsiniz. Ancak, özel bir derleme kodunda hata ayıklamak için derleme çözüm paketine eklemeniz gerekir. Daha fazla bilgi için [nasıl yapılır: Ek derlemeler ekleyip](../sharepoint/how-to-add-and-remove-additional-assemblies.md).

 Bir özel bütünleştirilmiş kod projenize ekleme hakkında daha fazla bilgi için bkz. [nasıl yapılır: İçinde bir BDC özelliğine özel bir derlemeyi etme](../sharepoint/how-to-include-a-custom-assembly-in-a-bdc-feature.md).

### <a name="configure-bdc-security"></a>İVB güvenliği yapılandırma
 Çözümünüzü hata ayıklama yapılabilmesi SharePoint güvenlik ayarlarınızı değiştirmeniz gerekebilir. Bu ayarları değiştirmek için iş verileri bağlantı hizmeti uygulaması SharePoint 2010 Merkezi Yönetim Web sitesini açın. İçinde **meta verileri Store izinlere** iletişim kutusunda, kullanıcı hesabınızı ekleyin ve aşağıdaki seçeneklerden birini seçin:

|Görev|Seçenek|
|----------|------------|
|BDC hizmeti için modelleri dağıtmak için.|Düzenle|
|Dış listeler ve Web Bölümleri'ı kullanarak oluşturmak için modelinizde (varlıklar) içerik türleri.|İstemcilerde seçilebilir|
|Oluşturun, okuyun, güncelleştirin ve varlık verilerini silmek için.|Yürütme|

 Bu ayarlar hakkında daha fazla bilgi için bkz. [İş Verileri Bağlantı Hizmeti Yönetimi](http://go.microsoft.com/fwlink/?LinkID=178883).

 Tek tek veya dış içerik türleri için güvenlik izinleri de ayarlayabilirsiniz. Bir modelin güvenlik izinleri ayarlama hakkında daha fazla bilgi için bkz. [İVB model Yönetimi](http://go.microsoft.com/fwlink/?LinkID=178884). Dış içerik türü güvenlik izinleri ayarlama hakkında daha fazla bilgi için bkz. [dış içerik türü Yönetim](http://go.microsoft.com/fwlink/?LinkID=178885).

> [!NOTE]
> Bir çözüm yerel SharePoint sunucunuz üzerinde hata ayıklamak için bu ayarları kullanın. Üretim SharePoint sunucusunda İVB ilgili güvenlik ayarlarını yapılandırma hakkında daha fazla bilgi için bkz. [İş Verileri Bağlantı Hizmetleri güvenliğine genel bakış](http://go.microsoft.com/fwlink/?LinkID=178886).

### <a name="retract-models-that-become-corrupt"></a>Bozuk model Ayıkla
 İlk kez hata ayıklayıcıyı başlattığınızda, Visual Studio için SharePoint modelin tamamı dağıtır. Her zaman için bundan sonra dağıtımlar arasında yaptığınız tüm değişiklikler Visual Studio SharePoint modelde güncelleştirir.

 Visual Studio SharePoint modelden tamamen geri çekmek için istediğiniz durumlar olabilir. Örneğin, bir model bozuk olabilir.  SharePoint'e modelinizi yeniden dağıtmak için ayarlanmış **Artımlı güncelleştirme** modele özelliği **False**, ve ardından hata ayıklayıcıyı başlatın. **Artımlı güncelleştirme** özellik görünür **özellikleri** modelinde temsil eden düğümü seçin, pencere **BDC Gezgini**. Varsayılan olarak, model adıdır **BdcModel1**.

### <a name="change-identifier-names-of-entities-in-the-model"></a>Tanımlayıcı adlarını modeli'ndeki varlıkları değiştirme
 Model dağıttıktan sonra bir tanımlayıcı adını değiştirirseniz, bir dağıtım hatası alabilirsiniz. Bu hata ayarlayarak çözümlenemiyor **Artımlı güncelleştirme** modele özelliği **False**. Model el ile geri çekmek ve ardından çözümü yeniden dağıtın. Daha fazla bilgi için [sorun giderme SharePoint çözümleri](../sharepoint/troubleshooting-sharepoint-solutions.md). Ayarlayarak bu hatayı önleyebilirsiniz **Artımlı güncelleştirme** özelliğini **False** başlangıçta model dağıtmadan önce.

## <a name="locate-documentation-for-bdc-model-elements"></a>İVB model öğeleri için belgeleri bulun
 Visual Studio, her varlık için model için bir XML öğesi ekler yöntemi veya oluşturduğunuz başka bir öğe. Öğenin öznitelikleri görünür özellikleri olarak **özellikleri** penceresi. Visual Studio model tasarlarken oluşturan öznitelikler ve öğeler hakkında daha fazla bilgi için bkz. [BDCMetadata şema](http://go.microsoft.com/fwlink/?LinkID=169275).

## <a name="related-topics"></a>İlgili konular

|Başlık|Açıklama|
|-----------|-----------------|
|[BDC modeli tasarım araçlarına genel bakış](../sharepoint/bdc-model-design-tools-overview.md)|Görsel olarak BDC modeli tasarım için kullanabileceğiniz araçları açıklar.|
|[Nasıl yapılır: Modele bir varlık ekleme](../sharepoint/how-to-add-an-entity-to-a-model.md)|Dış içerik türleri veya varlıklar, modele ekleme işlemi gösterilmektedir.|
|[Nasıl yapılır: Bir Bulucu yöntemi ekleme](../sharepoint/how-to-add-a-finder-method.md)|Kullanıcıların bir listesi veya Web Bölümü varlıkların listesini görüntülemek sağlayan bir yöntem ekleme işlemi gösterilmektedir.|
|[Nasıl yapılır: Belirli bir Bulucu yöntemi ekleme](../sharepoint/how-to-add-a-specific-finder-method.md)|Kullanıcıların belirli bir varlığa ayrıntılarını görüntülemek sağlayan bir yöntem ekleme işlemi gösterilmektedir.|
|[Nasıl yapılır: Bir yaratıcı metodu ekleme](../sharepoint/how-to-add-a-creator-method.md)|Kayıt bir veri kaynağına doğrudan bir liste veya Web Bölümü eklemek kullanıcıların olanak sağlayan bir yöntem ekleme işlemi gösterilmektedir.|
|[Nasıl yapılır: Silici metodu ekleme](../sharepoint/how-to-add-a-deleter-method.md)|Kullanıcıların listesini, kullanıcı arabirimi (UI) veya Web Bölümü seçenekleri kullanarak bir veri kaynağından verileri kaldırma olanak sağlayan bir yöntem ekleme işlemi gösterilmektedir.|
|[Nasıl yapılır: Bir güncelleyici metodu ekleme](../sharepoint/how-to-add-an-updater-method.md)|Kullanıcıların bir veri kaynağındaki kayıtları verileri doğrudan bir liste veya Web Bölümü değiştirmesine olanak sağlayan bir yöntem ekleme işlemi gösterilmektedir.|
|[Nasıl yapılır: Bir yönteme bir parametre ekleyin](../sharepoint/how-to-add-a-parameter-to-a-method.md)|Bir yönteme giriş ve dönüş parametreleri eklemek için Visual Studio yöntemi Ayrıntıları penceresinde kullanma işlemi gösterilmektedir.|
|[Nasıl yapılır: Bir parametrenin tür tanımlayıcısını tanımlama](../sharepoint/how-to-define-the-type-descriptor-of-a-parameter.md)|Modelde parametre veri türlerini tanımlamak gösterilmektedir.|
|[Nasıl yapılır: Metot örneği tanımlama](../sharepoint/how-to-define-a-method-instance.md)|İVB yürüten bir yöntem örneği oluşturma işlemi gösterilmektedir.|
|[Nasıl yapılır: Bir Bulucu metoduna filtre tanımlayıcısı ekleme](../sharepoint/how-to-add-a-filter-descriptor-to-a-finder-method.md)|Bir bulma yöntemi tarafından döndürülen örnek sayısını sınırlamak kullanıcıları etkinleştirmek gösterilmektedir.|
|[Varlıklar Arasında İlişkilendirme Oluşturma](../sharepoint/creating-an-association-between-entities.md)|Modeldeki varlıklar arasındaki ilişkilerin nasıl tanımlayabileceğiniz açıklar. İş Verileri Web bölümleri, dış listeler ve özel uygulamalar kullanıcı arabiriminde (UI) bu veri ilişkileri görüntüleyebilirsiniz.|
|[Nasıl yapılır: Varlıklar arasında ilişkilendirme oluşturma](../sharepoint/how-to-create-an-association-between-entities.md)|Modeldeki varlıklar arasındaki ilişkileri tanımlama işlemi gösterilmektedir.|
|[İzlenecek yol: İş verileri kullanarak bir dış liste SharePoint](../sharepoint/walkthrough-creating-an-external-list-in-sharepoint-by-using-business-data.md)|Oluşturma ve test kişiler bir SharePoint Dış listede görüntüler bir modeli gösteren adım adım yönergeler sağlar.|
|[İş verilerini SharePoint ile tümleştirme](../sharepoint/integrating-business-data-into-sharepoint.md)|Oluşturma ve tasarlama modelleri BDC hizmeti için genel bir bakış sağlar.|

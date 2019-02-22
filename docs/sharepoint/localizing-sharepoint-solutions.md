---
title: SharePoint Çözümlerini Yerelleştirme | Microsoft Docs
ms.date: 02/02/2017
ms.topic: conceptual
f1_keywords:
- VS.SharePointTools.Project.GlobalAndFeatureResource
- VS.SharePoint.Project.AddResourceDialog
dev_langs:
- VB
- CSharp
helpviewer_keywords:
- globalizing [SharePoint development in Visual Studio]
- localizing [SharePoint development in Visual Studio]
- SharePoint development in Visual Studio, localizing
author: John-Hart
ms.author: johnhart
manager: jillfra
ms.workload:
- office
ms.openlocfilehash: 71d22bb6210bb515941ca00ebb8b8655a6c089e0
ms.sourcegitcommit: d0425b6b7d4b99e17ca6ac0671282bc718f80910
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/21/2019
ms.locfileid: "56639927"
---
# <a name="localize-sharepoint-solutions"></a>SharePoint Çözümlerini Yerelleştirme

  Tüm dünyada kullanılabilir, böylece uygulamalarınız Hazırlama işlemi yerelleştirme olarak bilinir. Yerelleştirme, kaynakların belirli bir kültüre çevrilmesidir. Daha fazla bilgi için [Globalizing ve yerelleştirme uygulamaları](../ide/globalizing-and-localizing-applications.md). Bu konu nasıl bir SharePoint çözümünü yerelleştirileceği konusunda genel bir bakış sağlar.

 Bir çözümü yerelleştirmek için sabit kodlanmış dizeleri koddan kaldırın ve onları kaynak dosyalarına soyut olarak ekleyin. Kaynak dosya, bir [!INCLUDE[TLA2#tla_xml](../sharepoint/includes/tla2sharptla-xml-md.md)]-ile dosya tabanlı bir *.resx* uzantısı. Kaynak dosya çözümünüzde kullanılan dizelerin çevrilmiş versiyonlarını içerir. Daha fazla bilgi için [uygulamalardaki kaynaklar](http://go.microsoft.com/fwlink/?LinkID=155844).

> [!NOTE]
>  SharePoint çözüm kaynak dosyalarına dize kaynakları ekleyin. Kaynak Düzenleyicisi dize olmayan kaynaklar eklemenize olanak sağlar, ancak dize olmayan kaynaklar SharePoint'e dağıtılmaz.

## <a name="resource-files"></a>Kaynak dosyaları
 Kaynak dosyaları üç tür vardır: varsayılan, dil nötr ve dile özgü.

|Kaynak dosyası türü|Açıklama|
|------------------------|-----------------|
|Varsayılan|Olarak da bilinen bir geri dönüş kaynak varsayılan kaynak dosyaları için varsayılan kültürü İngilizce gibi yerelleştirilmiş dizeler içerir. Belirtilen dil için yerelleştirilmiş kaynak dosyası bulunamazsa bunlar kullanılır. Varsayılan kaynaklar ayrı dosyalar içermez, bunlar ana uygulama derlemesinde depolanır.|
|Geçerli dil|Bir dil, ancak belirli bir kültür için yerelleştirilmiş dizeler içeren kaynak dosyası. Örneğin, Fransızca için "fr".|
|Dile özgü|Bir dil ve kültür için yerelleştirilmiş dizeler içeren kaynak dosyası. Örneğin, "fr-CA" Fransızca Kanada için.|

 Daha fazla bilgi için [kaynakların hiyerarşik organizasyonu yerelleştirme için](http://go.microsoft.com/fwlink/?LinkId=178360).

 İçinde geliştirdiğiniz SharePoint projeleri varsayılan kaynak dosyalarını belirtmek üzere [!INCLUDE[vsprvs](../sharepoint/includes/vsprvs-md.md)], seçin **sabit dil (sabit ülke)** kültür listesinde **kaynak Ekle** iletişim kutusunda, bir kaynak dosyası ekleyin.

## <a name="localize-visual-studio-sharepoint-solutions"></a>Visual Studio SharePoint Çözümlerini Yerelleştirme
 Bir çözümü yerelleştirdiğiniz zaman çözümünüzün kullanıcılara görüntüler metinsel bilgilerin tümünü göz önünde bulundurmalısınız. Bilgilendirme iletileri, hata iletileri ve [!INCLUDE[TLA2#tla_ui](../sharepoint/includes/tla2sharptla-ui-md.md)] dizeleri çevrilmelidir ve bu Çeviriler kaynak dosyalara yerleştirilir.

 Bir kaynak dosyasındaki her dize benzersiz bir tanımlayıcıya sahiptir. Her kaynak dosyasındaki çevrilmiş dize için aynı tanımlayıcıyı kullanın. Örneğin, "String1" varsayılan kaynak dosyasındaki ilk dize için bir tanımlayıcı ise, dile özgü kaynak dosyalarındaki ilk dize için aynı tanımlayıcıyı kullanın.

 Genel olarak yerelleştirilen üç alan vardır [!INCLUDE[vsprvs](../sharepoint/includes/vsprvs-md.md)] SharePoint uygulamaları: özellikler, ASPX sayfa biçimlendirmesi ve kod. Gösterim amacıyla aşağıdaki bölümlerde Almanca ve Japonca'ya Yerelleştirmek istediğiniz bir SharePoint çözümünüz olduğu varsayılmıştır. İngilizce varsayılan dildir.

### <a name="localize-features"></a>Özellikleri yerelleştirme
 Bir özelliği yerelleştirmek için sabit kodlanmış başlığını ve özellik açıklaması dize yerelleştirilmiş kaynaklar dosyasındaki çevrilmiş başlık ve başvuran bir ifadeyle değiştirin gerekir. Bu değişiklik yaptığınız **özellik Tasarımcısı** içinde [!INCLUDE[vsprvs](../sharepoint/includes/vsprvs-md.md)]. Daha fazla bilgi için [nasıl yapılır: Bir özelliği yerelleştirme](../sharepoint/how-to-localize-a-feature.md).

 İngilizce özelliğinizi Almanca ve Japonca'ya yerelleştirmek için üç kaynak dosyası proje öğesi projenize ekleyin: biri İngilizce, biri Almanca için ve biri Japonca. Özellik kaynak dosyaları ASPX biçimlendirmeyi veya kodu yerelleştirmek için kullanılamaz; ayrı kaynak dosyaları için gereklidir.

 Özellik kaynak dosyaları oluşturduktan sonra çevrilmiş dizeleri de bunlara ekleyin. Aşağıdaki biçimde bir ifadeyle yerelleştirilmiş dizeleri erişebilirsiniz:

```aspx-csharp
$Resources:String ID
```

 İçindeki özellik kaynakları [!INCLUDE[vsprvs](../sharepoint/includes/vsprvs-md.md)] her zaman kaynaklar olarak da adlandırılır. Bir kültür sabit dil dışında bir dil seçerseniz [!INCLUDE[TLA2#tla_id](../sharepoint/includes/tla2sharptla-id-md.md)] kaynak dosya adına eklenir. Örneğin, bir sabit dil (varsayılan) özellik kaynak dosyası eklerseniz, çağrıldığı *Resources.resx*. Japonca (Japonya) kültürünü seçerek bir dile özgü özellik kaynağı eklerseniz, dosya adı verilir *adı Resources.ja-JP.resx*. Özellik kaynak dosya adları otomatik olarak atanır ve değiştirilemez.

 Özellik kaynaklarının kapsamı eklendikleri özellik için yereldir. Çözümdeki tüm özellikler veya öğeler dosyası tarafından kullanılan kaynakları oluşturmak için bir **Genel kaynaklar dosyası** yerine özellik kaynak dosyası proje öğesi. **Genel kaynaklar dosyası** proje öğesinin bulunduğu **2010** klasörü altında **SharePoint** içinde **Yeni Öğe Ekle** iletişim kutusu. Genel kaynak dosyaları SharePoint kök klasörünün \Resources klasörüne dağıtın.

### <a name="localize-aspx-page-markup"></a>ASPX sayfa biçimlendirmeyi yerelleştirme
 Yerelleştirmek için [!INCLUDE[vstecasp](../sharepoint/includes/vstecasp-md.md)] sayfaları, üç kaynak dosyası proje öğesi projenize ekleyin: biri İngilizce, biri Almanca için ve biri Japonca. Biçimlendirmeye ek olarak kodu yerelleştirmek yoksa, bunun yerine genel kaynak dosyalarını ekleyebilirsiniz.

 Varsayılan dil kaynak dosyası için bir ad sağlayın. Yerelleştirilen kaynak dosyalara dile özgü kültürü ekleyerek aynı adı verin [!INCLUDE[TLA2#tla_id](../sharepoint/includes/tla2sharptla-id-md.md)]. Örneğin, *MyAppResources.de-DE.resx* Almanca için ve *MyAppResources.ja-JP.resx* Japonca.

 Ayarlama **dağıtım türü** özelliği için her kaynak dosyasının **AppGlobalResource**. Bu, tüm ASPX sayfaları ve denetimleri çözümdeki kullanılabilir olduğu App_GlobalResources klasörüne dağıtılacak kaynak dosyalar neden olur. App_GlobalResources klasörüne C:\inetpub\wwwroot\wss\VirtualDirectories içinde bulunan\\< bağlantı noktası numarası\>\App_GlobalResources.

> [!NOTE]
>  Genel olmayan kaynak dosyaları kullanıyorsanız, bunları dağıtım türü özelliğini ve diğer SharePoint'e özgü özellikleri etkinleştirmek için proje öğesi klasörüne taşıyın.

 ASPX biçimlendirme kaynak dosyaları kod yerelleştirmek için de kullanılabilir. ASPX biçimlendirmeye ek olarak kodu yerelleştirmek için kaynakları kullanıyorsanız, bir uydu derlemeye derlemek için derleme eylemi özelliği ayarı her dosyanın kaynak neden gömülü kaynak olarak bırakın. Ancak, kaynak dosyalarını yalnızca biçimlendirmeyi yerelleştirmek için kullanıyorsanız, yapı eylemi dosyanın ana uygulama derlemesine eklenmesini derlenmiş önlemek için içeriği için isteğe bağlı olarak değiştirebilirsiniz.

 ASPX sayfaları ve denetimleri biçimlendirme tüm sabit kodlanmış özellik dizelerini aşağıdaki biçimde bir ifadeyle değiştirin:

```aspx-csharp
<asp:<class> runat="server" Text="<%$Resources:<Resource File Name>, <String ID>%>" />
```

 Örneğin:

```aspx-csharp
<asp:Button ID="btn1" runat="server" onclick="btn1_Click" Text="<%$Resources:Resource1,String7%>"></asp:Button>
```

 Metin olarak ASPX için aşağıdaki biçimde bir ifade kullanın:

```aspx-csharp
<asp:literal ID="<ID>" runat="server" Text="<%$Resources:<Resource File Name>, <String ID>%>" />
```

 Örneğin:

```aspx-csharp
<asp:literal ID="Literal1" runat="server" Text="<%$Resources:Resource1, String9%>" />
```

 Daha fazla bilgi için [nasıl yapılır: ASPX işaretlemesini yerelleştirme](../sharepoint/how-to-localize-aspx-markup.md).

### <a name="localize-code"></a>Kod yerelleştirme
 Özellik dizelerini yerelleştirme yanı sıra ve [!INCLUDE[vstecasp](../sharepoint/includes/vstecasp-md.md)] biçimlendirme'iniz de ileti dizelerini ve çözüm kodunuzda görüntülenen hata dizelerini yerelleştirmek. Yerelleştirilen bilgiler ve hata iletileri uydu derlemelerinde toplanır. Uydu derlemeleri gibi kullanıcılar tarafından görülebilir dizeleri içeren [!INCLUDE[TLA2#tla_ui](../sharepoint/includes/tla2sharptla-ui-md.md)] metin ve çıktı iletileri özel durumlar gibi.

 [!INCLUDE[vsprvs](../sharepoint/includes/vsprvs-md.md)] Standart .NET Framework merkez ve ışınsal modelini kullanır. Hub veya ana program derlemesi varsayılan dil kaynaklarını içerir. Spoke veya uydu derlemeleri dile özel kaynaklar içerir. Daha fazla bilgi için [kaynakları paketleme ve dağıtma](http://go.microsoft.com/fwlink/?LinkId=179280). Uydu derlemeleri kaynak derlenmiş (*.resx*) dosyaları. Proje ve çözüm paketine dile özgü kaynak dosyaları eklediğinizde [!INCLUDE[vsprvs](../sharepoint/includes/vsprvs-md.md)] kaynak dosyalarını adlı uygu derlemeleri halinde derler *{proje adı}.resources.dll*.

 ASPX biçimlendirmesi ile SharePoint uygulama kodunu projenize ayrı kaynak dosyası proje öğeleri ekleyerek yerelleştirin; Varsayılan dil için bir tane ve her bir dil yerelleştirilmiş. Ancak, kaynak dosyaları ASPX biçimlendirmesini yerelleştirmek için zaten varsa, daha önce belirtildiği gibi bunları kodu yerelleştirmek için yeniden kullanabilirsiniz. Kaynak dosyalar oluşturmanız gerekiyorsa varsayılan kaynak dosyasına protokolün kendi tercih ettiğiniz bir ad verin. bir *.resx* uzantısı. Yerelleştirilen kaynak dosyalara dile özgü kültürü ekleyerek aynı adı verin [!INCLUDE[TLA2#tla_id](../sharepoint/includes/tla2sharptla-id-md.md)]. Her kaynak dosyasının yapı eylemi özelliğini katıştırılmış kaynak için uydu kaynağı derlemelerinin oluşturulmasına olanak ayarlayın.

 Uydu derlemeleri oluşturmak için projeyi oluşturun ve dosyalarını ek derlemeler olarak eklersiniz **Gelişmiş** sekmesinde **paket Tasarımcısı**. Derlemeleri eklerken bir kültür önüne ekleyin [!INCLUDE[TLA2#tla_id](../sharepoint/includes/tla2sharptla-id-md.md)] klasörünü konum yolunun gibi *de-DE\\{proje öğesi adı}.resources.dll*. Bu paketin aynı ada sahip dosyaları içermesini sağlar.

 Kodunuzda, sabit kodlanmış dizeleri çağrılarıyla değiştirin. <xref:System.Web.HttpContext.GetGlobalResourceObject%2A> yöntemi aşağıdaki sözdizimini kullanarak:

```aspx-csharp
HttpContext.GetGlobalResourceObject("<Resource File Name>", "<String ID>")
```

 Daha fazla bilgi için [nasıl yapılır: Kod yerelleştirme](../sharepoint/how-to-localize-code.md).

#### <a name="web-part-code-localization"></a>Web Bölümü kod yerelleştirme
 Web bölümleri, WebDisplayName, Category ve WebDescription gibi sabit kodlanmış dizeleri kullanan kod öznitelikleri içeren bir özel özellik Düzenleyici özelliği içerir. Bu öznitelikler için dize değerlerini değiştirmek için özniteliğin sınıfından türetilen ayrı bir sınıf oluşturun. Bu sınıflarda özniteliğin özelliğini ayarlayın. Öznitelik özelliği taban sınıfa bağlıdır. Örneğin, WebDisplayName özniteliği DisplayNameValue özelliğindedir ve WebDescription özniteliği DescriptionValue özelliğindedir.

 Türetilen bir sınıfta, dize kimliği kaynak dosyasını ve dize kimliği için yerelleştirilen değeri almak için ve ResourceManager nesnesine başvuru Bu değer, Özellik Düzenleyici özniteliğine döndür.

## <a name="see-also"></a>Ayrıca bkz.
- [Nasıl yapılır: Bir özelliği yerelleştirme](../sharepoint/how-to-localize-a-feature.md)
- [Nasıl yapılır: ASPX işaretlemesini yerelleştirme](../sharepoint/how-to-localize-aspx-markup.md)
- [Nasıl yapılır: Kod yerelleştirme](../sharepoint/how-to-localize-code.md)
- [Nasıl yapılır: Kaynak dosyası ekleme](../sharepoint/how-to-add-a-resource-file.md)
- [Nasıl yapılır: Yerelleştirilmiş adlar, özellikler ve izinleri belirtmek için bir kaynak dosyası kullanma](../sharepoint/how-to-use-a-resource-file-to-specify-localized-names-properties-and-permissions.md)

---
title: XML özellik ve paket bildirimleriyle | Microsoft Docs
ms.date: 02/02/2017
ms.topic: conceptual
dev_langs:
- VB
- CSharp
helpviewer_keywords:
- SharePoint development in Visual Studio, packaging
author: John-Hart
ms.author: johnhart
manager: jillfra
ms.workload:
- office
ms.openlocfilehash: 1378cddbc9770af923a98f1b7083a8792874b5b3
ms.sourcegitcommit: 47eeeeadd84c879636e9d48747b615de69384356
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "63429281"
---
# <a name="merge-xml-in-feature-and-package-manifests"></a>XML özellik ve paket Bildirimlerde Birleştir
  Özellikleriniz ve paketleriniz tarafından tanımlanmıştır [!INCLUDE[TLA2#tla_xml](../sharepoint/includes/tla2sharptla-xml-md.md)] bildirim dosyaları. Bu paket bildirimleri tasarımcıları ve özel oluşturulan verileri bir bileşimidir [!INCLUDE[TLA2#tla_xml](../sharepoint/includes/tla2sharptla-xml-md.md)] bildirim şablonunda kullanıcı tarafından girilen. Paketleme zaman [!INCLUDE[vsprvs](../sharepoint/includes/vsprvs-md.md)] özel birleştirir [!INCLUDE[TLA2#tla_xml](../sharepoint/includes/tla2sharptla-xml-md.md)] tasarımcısı tarafından sağlanan ifadelerle [!INCLUDE[TLA2#tla_xml](../sharepoint/includes/tla2sharptla-xml-md.md)] paket oluşturmak üzere [!INCLUDE[TLA2#tla_xml](../sharepoint/includes/tla2sharptla-xml-md.md)] bildirim dosyası. Benzer öğeleri daha sonra birleştirme özel durumları, belirtilen özel durum ile birleştirilir önlemek için [!INCLUDE[TLA2#tla_xml](../sharepoint/includes/tla2sharptla-xml-md.md)] dosyaları SharePoint'e dağıtmanıza ve bildirim yapmak için daha küçük ve daha verimli dosyaları sonra doğrulama hataları.

## <a name="modify-the-manifests"></a>Bildirimleri değiştirme
 Özellik veya paket tasarımcıları devre dışı bırakmadıkça paket bildirim dosyaları doğrudan değişiklik yapamazsınız. Ancak, el ile özel ekleyebilirsiniz [!INCLUDE[TLA2#tla_xml](../sharepoint/includes/tla2sharptla-xml-md.md)] bildirim şablonu öğelerine özellik ve paket tasarımcıları aracılığıyla veya [!INCLUDE[TLA2#tla_xml](../sharepoint/includes/tla2sharptla-xml-md.md)] Düzenleyicisi. Daha fazla bilgi için [nasıl yapılır: Bir SharePoint özelliğini özelleştirme](../sharepoint/how-to-customize-a-sharepoint-feature.md) ve [nasıl yapılır: Bir SharePoint çözüm paketini özelleştirme](../sharepoint/how-to-customize-a-sharepoint-solution-package.md).

## <a name="feature-and-package-manifest-merge-process"></a>Birleştirme işlemi özellik ve paket bildirimi
 Öğe, tasarımcı tarafından sağlanan birlikte özel öğeleri birleştirilirken [!INCLUDE[vsprvs](../sharepoint/includes/vsprvs-md.md)] aşağıdaki işlemi kullanır. [!INCLUDE[vsprvs](../sharepoint/includes/vsprvs-md.md)] her öğenin benzersiz bir anahtar değere sahip olup olmadığını denetler. Öğenin benzersiz anahtar değeri yoksa, paket bildirim dosyasına eklenir. Benzer şekilde, birden çok anahtar olan öğeler birleştirilemiyor. Bu nedenle, bunlar için bildirim dosyası eklenir.

 Öğenin benzersiz bir anahtar varsa [!INCLUDE[vsprvs](../sharepoint/includes/vsprvs-md.md)] Tasarımcısı ve özel anahtarlar değerlerini karşılaştırır. Değerleri eşleşirse, tek bir değerde birleştirmeniz gerekir. Değerler farklıysa, Tasarımcı anahtar değeri atılır ve özel anahtar değeri kullanılır. Koleksiyonlar ayrıca birleştirilir. Örneğin, tasarımcı tarafından oluşturulan [!INCLUDE[TLA2#tla_xml](../sharepoint/includes/tla2sharptla-xml-md.md)] ve özel [!INCLUDE[TLA2#tla_xml](../sharepoint/includes/tla2sharptla-xml-md.md)] hem derlemeleri koleksiyonu içeren, paket bildirimi yalnızca bir derlemeleri koleksiyonu içerir.

## <a name="merge-exceptions"></a>Özel durumlar Birleştir
 [!INCLUDE[vsprvs](../sharepoint/includes/vsprvs-md.md)] Çoğu Tasarımcısı birleştirir [!INCLUDE[TLA2#tla_xml](../sharepoint/includes/tla2sharptla-xml-md.md)] öğeleri benzer özel birlikte [!INCLUDE[TLA2#tla_xml](../sharepoint/includes/tla2sharptla-xml-md.md)] öğeleri tek bir benzersiz tanımlayıcı özniteliği sahip oldukları sürece. Ancak, bazı öğeler için gerekli benzersiz tanımlayıcısı eksik [!INCLUDE[TLA2#tla_xml](../sharepoint/includes/tla2sharptla-xml-md.md)] birleştiriliyor. Bu öğeleri olarak bilinen *birleştirme özel durumları*. Bu gibi durumlarda, [!INCLUDE[vsprvs](../sharepoint/includes/vsprvs-md.md)] özel birleştirmez [!INCLUDE[TLA2#tla_xml](../sharepoint/includes/tla2sharptla-xml-md.md)] öğeleri tasarımcısı tarafından sağlanan birlikte [!INCLUDE[TLA2#tla_xml](../sharepoint/includes/tla2sharptla-xml-md.md)] öğeleri, ancak bunun yerine bunları için paket bildirim dosyası ekler.

 Özellik ve paket için birleştirme özel durumların bir listesi aşağıdadır [!INCLUDE[TLA2#tla_xml](../sharepoint/includes/tla2sharptla-xml-md.md)] bildirim dosyaları.

|Tasarımcı|XML öğesi|
|--------------|-----------------|
|Özellik Tasarımcısı|ActivationDependency|
|Özellik Tasarımcısı|UpgradeAction|
|Paket Tasarımcısı|SafeControl|
|Paket Tasarımcısı|CodeAccessSecurity|

## <a name="feature-manifest-elements"></a>Özellik liste öğeleri
 Aşağıdaki tabloda, birleştirilebilir tüm özellik liste öğeleri ve eşleştirmek için kullanılan kendi benzersiz anahtar listesidir.

|Öğe adı|Benzersiz anahtar|
|------------------|----------------|
|Özellik (tüm öznitelikler)|*Öznitelik adı* (her özniteliği özellik öğesi benzersiz bir anahtar adıdır.)|
|ElementFile|Konum|
|ElementManifests/ElementManifest|Konum|
|Properties/özelliği|Anahtar|
|CustomUpgradeAction|Ad|
|CustomUpgradeActionParameter|Ad|

> [!NOTE]
> Özel CustomUpgradeAction öğeyi değiştirmek için tek yolu olduğundan [!INCLUDE[TLA2#tla_xml](../sharepoint/includes/tla2sharptla-xml-md.md)] Düzenleyicisi değil birleştirme etkisini düşük.

## <a name="package-manifest-elements"></a>Paket bildirim öğeleri
 Aşağıdaki tabloda, birleştirilebilir tüm paket bildirim öğeleri ve eşleştirmek için kullanılan kendi benzersiz anahtar listesidir.

|Öğe adı|Benzersiz anahtar|
|------------------|----------------|
|Çözüm (tüm öznitelikler)|*Öznitelik adı* (her özniteliği çözüm öğesi benzersiz bir anahtar adıdır.)|
|ApplicationResourceFiles/ApplicationResourceFile|Konum|
|Derlemeleri/derleme|Konum|
|ClassResources/ClassResource|Konum|
|DwpFiles/DwpFile|Konum|
|FeatureManifests/FeatureManifest|Konum|
|Kaynak/kaynak|Konum|
|RootFiles/RootFile|Konum|
|SiteDefinitionManifests/SiteDefinitionManifest|Konum|
|WebTempFile|Konum|
|TemplateFiles/TemplateFile|Konum|
|SolutionDependency|SolutionID|

## <a name="manually-add-deployed-files"></a>Dağıtılan dosyalar el ile Ekle
 ApplicationResourceFile ve DwpFiles, gibi bazı bildirim öğeleri, bir dosya adı içeren bir konum belirtin. Ancak, bildirim şablonu için bir dosya adı girişi ekleme temel alınan dosyanın pakete eklemez. Dosyanın pakete dahil ve onun dağıtım türü özelliğini uygun şekilde ayarlamak için projeye eklemeniz gerekir.

## <a name="see-also"></a>Ayrıca bkz.
- [Paketleme ve SharePoint çözümlerini dağıtma](../sharepoint/packaging-and-deploying-sharepoint-solutions.md)
- [Derleme ve SharePoint çözümlerinde hata ayıklama](../sharepoint/building-and-debugging-sharepoint-solutions.md)

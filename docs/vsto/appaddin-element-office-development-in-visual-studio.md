---
title: "&lt;appAddin&gt; öğesi (Visual Studio'da Office Geliştirme)"
titleSuffix: ''
ms.date: 02/02/2017
ms.prod: visual-studio-dev15
ms.topic: conceptual
dev_langs:
- VB
- CSharp
helpviewer_keywords:
- application manifests [Office development in Visual Studio], <appAddin> element
author: John-Hart
ms.author: johnhart
manager: jillfra
ms.workload:
- office
ms.openlocfilehash: b53fcfaa28694b88f3401d0e2e40b157ba7c3201
ms.sourcegitcommit: c0202a77d4dc562cdc55dc2e6223c062281d9749
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/24/2019
ms.locfileid: "54875998"
---
# <a name="ltappaddingt-element-office-development-in-visual-studio"></a>&lt;appAddin&gt; öğesi (Visual Studio'da Office Geliştirme)
  **AppAddin** öğesinin `vstov4` ad alanı, VSTO eklentileri için özelleştirme özel bilgileri depolar.

## <a name="syntax"></a>Sözdizimi

```xml
<appAddin
  application
  loadBehavior
  keyName>
  <friendlyName>
  <description>
  <formRegions></formRegions>
</appAddin>
```

## <a name="elements-and-attributes"></a>Öğeler ve öznitelikler
 **AppAddin** öğesi gereklidir ve içinde `vstov4` ad alanı. Yalnızca bir tane **appAddin** uygulama bildiriminde tanımlanan öğe.

 **AppAddin** öğesinde şu öznitelikler bulunur.

|Öznitelik|Açıklama|
|---------------|-----------------|
|**Uygulama**|Gerekli. Microsoft Office uygulamasını tanımlar. Değerin aşağıdakilerden biri olabilir: Excel, InfoPath, Outlook, PowerPoint, proje, Visio veya Word.|
|**LoadBehavior**|İsteğe bağlı. Varsayılan olarak, **loadBehavior** , bu değeri ayarlamak etkinleştirilir. Hata ayıklama için VSTO eklentisi iki değere ayarlayarak devre dışı bırakılabilir. LoadBehavior değerleri adlı tabloyu daha fazla bilgi için bkz. [VSTO eklentileri için kayıt defteri girdileri](../vsto/registry-entries-for-vsto-add-ins.md).|
|**anahtar adı**|Gerekli. Uygulama tarafından VSTO eklenti yüklemek için kullanılan kayıt defteri anahtarı adını değerdir. Daha fazla bilgi için [VSTO eklentileri için kayıt defteri girdileri](../vsto/registry-entries-for-vsto-add-ins.md).|

 **AppAddin** öğesi şu alt öğelerden sahiptir.

### <a name="friendlyname"></a>FriendlyName
 İsteğe bağlı. **FriendlyName** öğesi içinde açıklanan [ &#60;friendlyName&#62; öğesi &#40;Visual Studio'da Office geliştirme&#41;](../vsto/friendlyname-element-office-development-in-visual-studio.md).

### <a name="description"></a>açıklama
 İsteğe bağlı. **Açıklama** öğesi içinde açıklanan [ &#60;açıklama&#62; öğesi &#40;Visual Studio'da Office geliştirme&#41;](../vsto/description-element-office-development-in-visual-studio.md).

### <a name="formregions"></a>formRegions
 Yalnızca Outlook VSTO form bölgeleri içeren eklentileri için gereklidir. **FormRegions** öğesi içinde açıklanan [ &#60;formRegions&#62; öğesi &#40;Visual Studio'da Office geliştirme&#41;](../vsto/formregions-element-office-development-in-visual-studio.md).

## <a name="vsto-add-in-example"></a>VSTO eklenti örneği

### <a name="description"></a>Açıklama
 Aşağıdaki kod örneğinde gösterilmiştir **appAddin** kullanılarak dağıtılan bir Outlook çözüm öğelerinde [!INCLUDE[ndptecclick](../vsto/includes/ndptecclick-md.md)]. Bu kod örneği, sağlanan daha büyük bir örneğin parçasıdır [Office çözümleri için uygulama bildirimleri](../vsto/application-manifests-for-office-solutions.md).

### <a name="code"></a>Kod

```xml
<vstov4:appAddIn
  application="Outlook"
  loadBehavior="3"
  keyName="ContosoOutlookAddIn">
  <vstov4:friendlyName>
    ContosoOutlookAddIn
  </vstov4:friendlyName>
  <vstov4:description>
    ContosoOutlookAddIn - Outlook VSTO Add-in
    created with Visual Studio Tools for Office
  </vstov4:description>
  <vstov4:formRegions>
    <vstov4:formRegion
        name="OutlookAddIn1.FormRegion1">
      <vstov4:messageClass name="IPM.Note" />
      <vstov4:messageClass name="IPM.Contact" />
      <vstov4:messageClass name="IPM.Appointment" />
    </vstov4:formRegion>
  </vstov4:formRegions>
</vstov4:appAddIn>
```

## <a name="see-also"></a>Ayrıca bkz.

- [Office çözümleri için uygulama bildirimleri](../vsto/application-manifests-for-office-solutions.md)
- [Office çözümleri için dağıtım bildirimleri](../vsto/deployment-manifests-for-office-solutions.md)
- [ClickOnce Uygulama bildirimi](../deployment/clickonce-application-manifest.md)
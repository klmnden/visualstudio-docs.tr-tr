---
title: SafeControl öğesi | Microsoft Docs
ms.date: 02/02/2017
ms.topic: conceptual
dev_langs:
- VB
- CSharp
helpviewer_keywords:
- SafeControl element
author: John-Hart
ms.author: johnhart
manager: jillfra
ms.workload:
- office
ms.openlocfilehash: a80606297c61d59d5670473755e667c6d3c538de
ms.sourcegitcommit: d0425b6b7d4b99e17ca6ac0671282bc718f80910
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/21/2019
ms.locfileid: "56601271"
---
# <a name="safecontrol-element"></a>SafeControl öğesi
  ASPX denetim ya da herhangi bir SharePoint sitesinde ASPX sayfasında erişmek herhangi bir kullanıcı için güvenli olarak tasarlanmış bir Web Bölümü temsil eder.

## <a name="syntax"></a>Sözdizimi

```xml
<SafeControl Assembly = "Name of assembly that contains the safe control"
    IsSafe = "true/false"
    IsSafeAgainstScript = "true/false"
    Name = "Name of this safe control entry"
    Namespace = "Namespace of the safe control"
    TypeName = "Type of the safe control" />
```

## <a name="attributes-and-elements"></a>Öznitelikler ve öğeler
 Öznitelikler, alt ve üst öğeler aşağıdaki bölümlerde açıklanmaktadır.

### <a name="attributes"></a>Öznitelikler

|Öznitelik|Açıklama|
|---------------|-----------------|
|**Assembly**|İsteğe bağlı **xs: String** özniteliği.<br /><br /> ASPX denetimi veya Web Bölümü tanımlandığı derlemenin adı. Bu öznitelik varsayılan olarak kullandığı **$SharePoint.Project.AssemblyFullName$** parametredir derleme adı. Daha fazla bilgi için [değiştirilebilir parametreler](../sharepoint/replaceable-parameters.md).|
|**IsSafe**|İsteğe bağlı **xs:boolean** özniteliği.<br /><br /> ASPX denetimi veya Web Bölümü güvenilmeyen kullanıcıların erişim için güvenli olup olmadığını belirtir.|
|**IsSafeAgainstScript**|İsteğe bağlı **xs:boolean** özniteliği.<br /><br /> Güvenilmeyen kullanıcıların görüntüleyebilir veya Web Bölümü ve ASPX denetim özelliklerini düzenleme olup olmadığını belirtir.|
|**Ad**|İsteğe bağlı **xs: String** özniteliği.<br /><br /> Bu koleksiyondaki güvenli denetim giriş adı.|
|**Namespace**|İsteğe bağlı **xs: String** özniteliği.<br /><br /> ASPX denetim ya da Web Bölümü ad alanı.|
|**typeName**|İsteğe bağlı **xs: String** özniteliği.<br /><br /> Web Bölümü ve ASPX denetim türü adı.|

### <a name="child-elements"></a>Alt öğeleri
 Yok.

### <a name="parent-elements"></a>Üst öğeler

|Öğe|Açıklama|
|-------------|-----------------|
|[SafeControls](../sharepoint/safecontrols-element.md)|ASPX denetimleri ve Web bölümleri, herhangi bir SharePoint sitesinde ASPX sayfasında erişmek herhangi bir kullanıcı için güvenli olarak belirlenmiş bir koleksiyonunu temsil eder.|

## <a name="remarks"></a>Açıklamalar
 Güvenli denetimler hakkında daha fazla bilgi için bkz: [proje öğelerinde paketleme ve dağıtım bilgileri sağlayan](../sharepoint/providing-packaging-and-deployment-information-in-project-items.md).

## <a name="element-information"></a>Öğe bilgileri

|||
|-|-|
|**Namespace**|HTTP<nolink>: //schemas.microsoft.com/VisualStudio/<br>2010/SharePointTools/SharePointProjectItemModel|
|**Şema adı**|SharePoint proje öğesi şema|
|**Doğrulama dosyası**|ProjectItemModelSchema.xsd|
|**Boş olabilir**|Hayır|

## <a name="see-also"></a>Ayrıca bkz.
- [SharePoint proje öğesi şema başvurusu](../sharepoint/sharepoint-project-item-schema-reference.md)
- [Proje öğelerinde paketleme ve dağıtım bilgileri sağlayın](../sharepoint/providing-packaging-and-deployment-information-in-project-items.md)

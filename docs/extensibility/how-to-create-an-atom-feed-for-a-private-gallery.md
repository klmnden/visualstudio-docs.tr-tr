---
title: 'Nasıl Yapılır: Atom oluşturmak için özel bir galeriyi akış | Microsoft Docs'
ms.date: 11/04/2016
ms.topic: conceptual
helpviewer_keywords:
- Atom feed, VSIX private galleries
- VSIX private galleries, Atom feed
ms.assetid: 5897f538-9c41-486f-97d9-a1976d20d9fd
author: gregvanl
ms.author: gregvanl
manager: douge
ms.workload:
- vssdk
ms.openlocfilehash: 6fc3aef8605f5c3343bcc6aca86513d631cace35
ms.sourcegitcommit: 37fb7075b0a65d2add3b137a5230767aa3266c74
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/02/2019
ms.locfileid: "53941696"
---
# <a name="how-to-create-an-atom-feed-for-a-private-gallery"></a>Nasıl Yapılır: Atom akışı için özel bir galeri oluşturun
Bir Atom (uzantıları içeren ve akışa ekleme bir intranet konumu için RSS akışı) oluşturabileceğiniz **Uzantılar ve güncelleştirmeler** özel bir galeri olarak. Daha fazla bilgi için [özel galeriler](../extensibility/private-galleries.md).  
  
## <a name="create-an-atom-feed"></a>Bir Atom akışı oluşturma  
 Atom akışı özel bir galeri oluşturmak için öncelikle uzantılarınızı toplayın (*.vsix* dosyaları) bir klasöre kopyalar. İsterseniz, alt klasörler halinde düzenleyebilirsiniz. Ayrıca, aşağıdaki kaynakları gerekir:  
  
- Bir *atom.xml* uzantıları özel bir galeride kullanıma sunduğu dosya. Bağlanma hakkında daha fazla bilgi için *atom.xml* dosyasını **Uzantılar ve güncelleştirmeler**, bkz: [özel galeriler](../extensibility/private-galleries.md).  
  
- (Örneğin, ekran görüntüleri) extensions ayıklanan herhangi bir görüntü dosyalarını içeren bir klasör. *Atom.xml* dosya içeren görüntü yollarında göreli bağlantıları yer alır, böylece **Uzantılar ve güncelleştirmeler**.  
  
  Örneğin, bir klasöre toplanan aşağıdaki iki uzantıları varsayın:  
  
- *Template_Wizard_239.vsix*, bu değer boş bir VSIX proje şablonu.  
  
- *SelectionHighlight.vsix*, seçili sözcüğün tüm örneklerinin vurgulamak için aracı.  
  
  İçeriğini *atom.xml* dosya, aşağıdaki örnekte benzer:  
  
```xml  
<?xml version="1.0" encoding="utf-8" ?>   
<feed xmlns="http://www.w3.org/2005/Atom">  
<title type="text" />   
<id>uuid:bcecded5-97c8-4d24-96f1-7d9e16652433;id=1</id>   
<updated>2011-04-14T21:25:48Z</updated>   
<entry>  
<id>SelectionHighlight..a14874d2-8199-4a60-af8a-11d6447813aa</id>   
<title type="text">Highlight all occurrences of selected word</title>   
<summary type="text">This extends the editor to highlight ....</summary>   
<published>2011-04-14T14:24:51-07:00</published>   
<updated>2011-04-14T14:24:22-07:00</updated>   
<author>  
<name>Microsoft</name>   
</author>  
<link rel="icon" href="VSIXImages/SelectionHighlight..a14874d2-8199-4a60-af8a-11d6447813aa_Icon_SelectionHighlightIcon.jpg" />   
<link rel="previewimage" href="VSIXImages/SelectionHighlight..a14874d2-8199-4a60-af8a-11d6447813aa_PreviewImage_SelectionHighlight.jpg" />   
<content type="application/octet-stream" src="SelectionHighlight.vsix" />   
<Vsix xmlns:xsd="http://www.w3.org/2001/XMLSchema" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="http://schemas.microsoft.com/developer/vsx-syndication-schema/2010">  
<Id>SelectionHighlight..a14874d2-8199-4a60-af8a-11d6447813aa</Id>   
<Version>1.31</Version>   
<References />   
<Rating xsi:nil="true" />   
<RatingCount xsi:nil="true" />   
<DownloadCount xsi:nil="true" />   
</Vsix>  
</entry>  
<entry>  
<id>Template_Wizard_239.Microsoft.3b38a7e3-5cbc-4389-a92a-d82tyc2ed592</id>   
...  
</entry>  
</feed>
```  
  
 Görüntüleri oluşturulan bir klasörde ekran görüntüleri için dikkat edin iki bağlantı etiketlerini bakın.  
  
## <a name="see-also"></a>Ayrıca bkz.  
 [Özel galeriler](../extensibility/private-galleries.md)

---
title: İş Akışı Tasarımcısı - Existsıncollection&lt;T&gt; etkinlik Tasarımcısı
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- System.Activities.Statements.ExistsInCollection`1.UI
ms.assetid: 0acf9a13-caf5-4bb4-ba22-ec37d2b7267a
author: gewarren
ms.author: gewarren
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 06892bcfdca33e5e77e8c01f06f594849e5293e5
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62949727"
---
# <a name="existsincollectiont-activity-designer"></a>Existsıncollection\<T > etkinlik Tasarımcısı

**Existsıncollection\<T >** etkinlik Tasarımcısı oluşturmak ve yapılandırmak için kullanılan bir <xref:System.Activities.Statements.ExistsInCollection%601> etkinlik.

## <a name="the-existsincollectiont-activity"></a>Existsıncollection\<T > etkinliği

<xref:System.Activities.Statements.ExistsInCollection%601> Etkinlik belirtilen bir öğenin belirli bir koleksiyonda mevcut olup olmadığını belirler.

### <a name="using-the-existsincollectiont-activity-designer"></a>Existsıncollection kullanarak\<T > etkinlik Tasarımcısı

**Existsıncollection\<T >** etkinlik Tasarımcısı bulunabilir **koleksiyon** kategorisi **araç kutusu**, hangi erişilen tıklayarak **Araç kutusu** iş akışı Tasarımcısı için sekmesinde. Alternatif olarak, seçin **araç kutusu** gelen **görünümü** tuşuna basın veya menü **Ctrl**+**Alt** + **X**.

**Existsıncollection\<T >** etkinlik Tasarımcısı, gelen sürüklenebilir **araç kutusu** ve etkinlikleri genellikle yerleştirilen her yerde, gibi olarak içinde iş akışı Tasarımcısı yüzeyine açın bir <xref:System.Activities.Statements.Sequence>. Bu, oluşturur bir <xref:System.Activities.Statements.ExistsInCollection%601> etkinliği ile bir varsayılan <xref:System.Activities.Activity.DisplayName%2A> Existsıncollection, < Int32\>. (Varsayılan olarak, *TypeArgument* olduğu **Int32**. Bu özellik kılavuzunda değiştirilebilir.)  <xref:System.Activities.Activity.DisplayName%2A> Değeri üst bilgisinde düzenlenebilir **Existsıncollection < T\>**  etkinlik Tasarımcısı veya **DisplayName** özellik kılavuzunda kutusu. Özellik Kılavuzu'nun diğer özellikleri düzenlenmesi gerekir.

### <a name="the-existsincollectiont-properties"></a>Existsıncollection\<T > Özellikleri

Aşağıdaki tabloda <xref:System.Activities.Statements.ExistsInCollection%601> özellikleri ve Tasarımcısı'nda nasıl kullanıldığını açıklar:

|Özellik Adı|Gerekli|Kullanım|
|-|--------------|-|
|<xref:System.Activities.Activity.DisplayName%2A>|False|Kolay adı <xref:System.Activities.Statements.ExistsInCollection%601> etkinlik. Existsıncollection varsayılandır < Int32\>. Ancak <xref:System.Activities.Activity.DisplayName%2A> değeri kesinlikle gerekli değil, kullanmak için en iyi bir uygulamadır.|
|<xref:System.Activities.Statements.ExistsInCollection%601.Item%2A>|Doğru|Öğe koleksiyonda aranacak\<T >. Bu öğe türünde *T*, türünde *TypeArgument*. Öğesini belirtmek için bir Visual Basic ifadesinin özellik kılavuzunda yazın.|
|<xref:System.Activities.Statements.ExistsInCollection%601.Collection%2A>|Doğru|Koleksiyon, öğe mevcut olup olmadığını denetleyin. Bu koleksiyonu türünde **ICollection < TypeArgument\>.** Koleksiyon belirtmek için bir Visual Basic ifadesinin özellik kılavuzunda yazın.|
|*TypeArgument*|Doğru|İçindeki öğe türü T <xref:System.Collections.Generic.ICollection%601>. Varsayılan olarak, bu *TypeArgument* türü ayarlandığında **Int32**. Türü değiştirmek için değerini değiştirmek *TypeArgument* birleşik giriş kutusundaki özellik kılavuzunda.|
|<xref:System.Activities.Activity%601.Result%2A>|False|Belirtilen öğe koleksiyonunda var olup olmadığını belirten bir değer. Sonucu bağlamak için bir değişken olarak belirtmek için bir Visual Basic değişken özellik kılavuzunda yazın.|

## <a name="see-also"></a>Ayrıca bkz.

- [Koleksiyon](../workflow-designer/collection-activity-designers.md)
- [AddToCollection\<T>](../workflow-designer/addtocollection-t-activity-designer.md)
- [ClearCollection\<T>](../workflow-designer/clearcollection-t-activity-designer.md)
- [RemoveFromCollection\<T>](../workflow-designer/removefromcollection-t-activity-designer.md)
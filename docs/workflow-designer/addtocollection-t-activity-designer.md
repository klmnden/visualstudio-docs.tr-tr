---
title: İş Akışı Tasarımcısı - AddToCollection<T> etkinlik Tasarımcısı
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- System.Activities.Statements.AddToCollection`1.UI
ms.assetid: f7fc0702-164e-4370-8946-bb2f9f9384b7
author: gewarren
ms.author: gewarren
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 7e339e2639d85f89d4110c36710ab9c19e0fe333
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62842091"
---
# <a name="addtocollectiont-activity-designer"></a>AddToCollection\<T > etkinlik Tasarımcısı

**AddToCollection\<T >** etkinlik Tasarımcısı oluşturmak ve yapılandırmak için kullanılan bir <xref:System.Activities.Statements.AddToCollection%601> etkinlik.

## <a name="the-addtocollectiont-activity"></a>AddToCollection\<T > etkinliği

<xref:System.Activities.Statements.AddToCollection%601> Etkinlik bir koleksiyon için bir öğe ekler.

### <a name="using-the-addtocollectiont-activity-designer"></a>AddToCollection kullanarak\<T > etkinlik Tasarımcısı

**AddToCollection\<T >** etkinlik Tasarımcısı bulunabilir **koleksiyon** kategorisi **araç kutusu**, hangi erişilen tıklayarak **Araç kutusu** iş akışı Tasarımcısı için sekmesinde. Alternatif olarak, seçin **araç kutusu** gelen **görünümü** tuşuna basın veya menü **Ctrl**+**Alt** + **X**.

**AddToCollection\<T >** etkinlik Tasarımcısı, gelen sürüklenebilir **araç kutusu** ve etkinlikleri yerleştirilir her yerde, böyle bir gibiiçindeişakışıTasarımcısıyüzeyineaçın<xref:System.Activities.Statements.Sequence>. Bırakarak **AddToCollection\<T >** etkinlik Tasarımcısı oluşturur bir <xref:System.Activities.Statements.AddToCollection%601> etkinliği ile bir varsayılan <xref:System.Activities.Activity.DisplayName%2A> AddToCollection, < Int32\>. (Varsayılan olarak, *TypeArgument* olduğu **Int32**. TypeArgument özellik kılavuzunda değiştirilebilir.) <xref:System.Activities.Activity.DisplayName%2A> Değeri üst bilgisinde düzenlenebilir **AddToCollection < T\>**  etkinlik Tasarımcısı veya **DisplayName** özellik kılavuzunda kutusu. Özellik Kılavuzu'nun diğer özellikleri düzenlenmesi gerekir.

### <a name="the-addtocollectiont-properties"></a>AddToCollection\<T > Özellikleri

Aşağıdaki tabloda <xref:System.Activities.Statements.AddToCollection%601> özellikleri Tasarımcısı'nda nasıl kullanıldığı açıklanmaktadır.

|Özellik Adı|Gerekli|Kullanım|
|-|--------------|-|
|<xref:System.Activities.Activity.DisplayName%2A>|False|Kolay adı <xref:System.Activities.Statements.AddToCollection%601> etkinlik. AddToCollection varsayılandır < Int32\>. Ancak <xref:System.Activities.Activity.DisplayName%2A> değeri kesinlikle gerekli değil, kullanmak için en iyi bir uygulamadır.|
|<xref:System.Activities.Statements.AddToCollection%601.Item%2A>|Doğru|Koleksiyona eklenecek öğe\<T >. Bu öğe türünde *T*, türünde *TypeArgument*. Öğesini belirtmek için bir Visual Basic ifadesinin özellik kılavuzunda yazın.|
|<xref:System.Activities.Statements.AddToCollection%601.Collection%2A>|Doğru|Öğesi eklenmesi gereken koleksiyon. Bu koleksiyonu türünde **ICollection < TypeArgument\>**. Koleksiyon belirtmek için bir Visual Basic ifadesinin özellik kılavuzunda yazın.|
|*TypeArgument*|Doğru|İçindeki öğe türü T <xref:System.Collections.Generic.ICollection%601>. Varsayılan olarak, bu *TypeArgument* türü ayarlandığında **Int32**. Türü değiştirmek için değerini değiştirmek *TypeArgument* birleşik giriş kutusundaki özellik kılavuzunda.|

## <a name="see-also"></a>Ayrıca bkz.

- [Koleksiyon](../workflow-designer/collection-activity-designers.md)
- [AddToCollection\<T > etkinlik Tasarımcısı](../workflow-designer/addtocollection-t-activity-designer.md)
- [ClearCollection\<T>](../workflow-designer/clearcollection-t-activity-designer.md)
- [ExistsInCollection\<T>](../workflow-designer/existsincollection-t-activity-designer.md)
- [RemoveFromCollection\<T>](../workflow-designer/removefromcollection-t-activity-designer.md)
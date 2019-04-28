---
title: İş Akışı Tasarımcısı - ClearCollection<T> etkinlik Tasarımcısı
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- System.Activities.Statements.ClearCollection`1.UI
ms.assetid: db0e5da2-7b5a-4f1a-864c-f3aeeeeb51a7
author: gewarren
ms.author: gewarren
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: cab7ea023524da7e28e2baa2d4e5018cd091c60d
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62950000"
---
# <a name="clearcollectiont-activity-designer"></a>ClearCollection\<T > etkinlik Tasarımcısı

**ClearCollection\<T >** etkinlik Tasarımcısı oluşturmak ve yapılandırmak için kullanılan bir <xref:System.Activities.Statements.ClearCollection%601> etkinlik.

## <a name="the-clearcollectiont-activity"></a>ClearCollection\<T > etkinliği

<xref:System.Activities.Statements.ClearCollection%601> Etkinlik belirtilen tüm öğeleri koleksiyonu temizler.

### <a name="using-the-clearcollectiont-activity-designer"></a>ClearCollection kullanarak\<T > etkinlik Tasarımcısı

**ClearCollection\<T >** etkinlik Tasarımcısı bulunabilir **koleksiyon** kategorisi **araç kutusu**, hangi erişilen tıklayarak **Araç kutusu** iş akışı Tasarımcısı için sekmesinde. Alternatif olarak, seçin **araç kutusu** gelen **görünümü** tuşuna basın veya menü **Ctrl**+**Alt** + **X**.

**ClearCollection\<T >** etkinlik Tasarımcısı, gelen sürüklenebilir **araç kutusu** ve etkinlikleri yerleştirilir her yerde, böyle bir gibiiçindeişakışıTasarımcısıyüzeyineaçın<xref:System.Activities.Statements.Sequence>. Etkinlik Tasarımcısı bırakarak oluşturur bir <xref:System.Activities.Statements.ClearCollection%601> etkinliği ile bir varsayılan <xref:System.Activities.Activity.DisplayName%2A> ClearCollection, < Int32\>. (Varsayılan olarak, *TypeArgument* olduğu **Int32**. TypeArgument özellik kılavuzunda değiştirilebilir.) <xref:System.Activities.Activity.DisplayName%2A> Değeri üst bilgisinde düzenlenebilir **ClearCollection < T\>**  etkinlik Tasarımcısı veya **DisplayName** özellik kılavuzunda kutusu. Özellik Kılavuzu'nun diğer özellikleri düzenlenmesi gerekir.

### <a name="the-clearcollectiont-properties"></a>ClearCollection\<T > Özellikleri

Aşağıdaki tabloda <xref:System.Activities.Statements.ClearCollection%601> özellikleri Tasarımcısı'nda nasıl kullanıldığı açıklanmaktadır.

|Özellik Adı|Gerekli|Kullanım|
|-|--------------|-|
|<xref:System.Activities.Activity.DisplayName%2A>|False|İsteğe bağlı kolay adı belirtir <xref:System.Activities.Statements.ClearCollection%601> etkinlik. ClearCollection varsayılandır < Int32\>. Ancak <xref:System.Activities.Activity.DisplayName%2A> değeri kesinlikle gerekli değil, kullanmak için en iyi bir uygulamadır.|
|<xref:System.Activities.Statements.ClearCollection%601.Collection%2A>|Doğru|Öğelerin temizlenecek koleksiyonu belirtir. Bu koleksiyonu türünde **ICollection\<TypeArgument >.** Koleksiyon belirtmek için bir Visual Basic ifadesinin özellik kılavuzunda yazın.|
|*TypeArgument*|Doğru|İçindeki öğe türü T belirtir <xref:System.Collections.Generic.ICollection%601>. Varsayılan olarak, bu *TypeArgument* türü ayarlandığında **Int32**. Türü değiştirmek için değerini değiştirmek *TypeArgument* birleşik giriş kutusundaki özellik kılavuzunda.|

## <a name="see-also"></a>Ayrıca bkz.

- [Koleksiyon](../workflow-designer/collection-activity-designers.md)
- [AddToCollection\<T>](../workflow-designer/addtocollection-t-activity-designer.md)
- [ExistsInCollection\<T>](../workflow-designer/existsincollection-t-activity-designer.md)
- [RemoveFromCollection\<T>](../workflow-designer/removefromcollection-t-activity-designer.md)
---
title: İş Akışı Tasarımcısı - ClearCollection<T> etkinlik Tasarımcısı
ms.date: 11/04/2016
ms.topic: reference
ms.prod: visual-studio-dev15
f1_keywords:
- System.Activities.Statements.ClearCollection`1.UI
ms.assetid: db0e5da2-7b5a-4f1a-864c-f3aeeeeb51a7
author: gewarren
ms.author: gewarren
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: f086acbbdbbdf442b1684cc5c32d1fa13eb785f4
ms.sourcegitcommit: 2193323efc608118e0ce6f6b2ff532f158245d56
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/25/2019
ms.locfileid: "55034070"
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
- [Existsıncollection\<T >](../workflow-designer/existsincollection-t-activity-designer.md)
- [RemoveFromCollection\<T >](../workflow-designer/removefromcollection-t-activity-designer.md)
---
title: İş Akışı Tasarımcısı - RemoveFromCollection&lt;T&gt; etkinlik Tasarımcısı
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- System.Activities.Statements.RemoveFromCollection`1.UI
ms.assetid: 6617ba26-c8bc-4aed-b746-112bf490d288
author: gewarren
ms.author: gewarren
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 4b3a43c05f8be4806cf10098a4df673903494756
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62933745"
---
# <a name="removefromcollectiont-activity-designer"></a>RemoveFromCollection\<T > etkinlik Tasarımcısı

**RemoveFromCollection\<T >** etkinlik Tasarımcısı oluşturmak ve yapılandırmak için kullanılan bir <xref:System.Activities.Statements.RemoveFromCollection%601> etkinlik.

## <a name="the-removefromcollectiontactivity"></a>RemoveFromCollection\<T > etkinliği

<xref:System.Activities.Statements.RemoveFromCollection%601> Etkinlik belirtilen bir öğenin belirli bir koleksiyondan kaldırır.

### <a name="using-the-removefromcollectiont-activity-designer"></a>RemoveFromCollection kullanarak\<T > etkinlik Tasarımcısı

Erişim **RemoveFromCollection\<T >** etkinlik Tasarımcısı'nda **koleksiyon** kategorisi **araç kutusu**.
**RemoveFromCollection\<T >** etkinlik Tasarımcısı, gelen sürüklenebilir **araç kutusu** ve etkinlikleri genellikle, gibi yerleştirilir her yerde iş akışı Tasarımcısı yüzeyine açın içinde bir <xref:System.Activities.Statements.Sequence>. Bu, oluşturur bir <xref:System.Activities.Statements.RemoveFromCollection%601> etkinliği ile bir varsayılan <xref:System.Activities.Activity.DisplayName%2A> RemoveFromCollection, < Int32\>. <xref:System.Activities.Activity.DisplayName%2A> Değeri üst bilgisinde düzenlenebilir **RemoveFromCollection < T\>**  etkinlik Tasarımcısı veya **DisplayName** özellik kılavuzunda kutusu. Özellik Kılavuzu'nun diğer özellikleri düzenlenmesi gerekir.

### <a name="the-removefromcollectiont-properties"></a>RemoveFromCollection < T\> özellikleri

Aşağıdaki tabloda <xref:System.Activities.Statements.RemoveFromCollection%601> özellikleri ve Tasarımcısı'nda nasıl kullanıldığını açıklar:

|Özellik Adı|Gerekli|Kullanım|
|-|--------------|-|
|<xref:System.Activities.Activity.DisplayName%2A>|False|İsteğe bağlı kolay adı <xref:System.Activities.Statements.RemoveFromCollection%601> etkinlik. RemoveFromCollection varsayılandır < Int32\>.<br /><br /> Ancak <xref:System.Activities.Activity.DisplayName%2A> kati şekilde gerekli değil kullanmak için en iyi bir uygulamadır.|
|<xref:System.Activities.Statements.RemoveFromCollection%601.Item%2A>|Doğru|Kaldırmak için öğeyi **koleksiyon\<T >**. Bu öğe türünde *T*, türünde *TypeArgument*. Öğesini belirtmek için bir Visual Basic ifadesinin özellik kılavuzunda yazın.|
|<xref:System.Activities.Statements.RemoveFromCollection%601.Collection%2A>|Doğru|Öğenin kaldırılması gerektiğini koleksiyonu. Bu koleksiyonu türünde **ICollection < TypeArgument\>.** Koleksiyon belirtmek için bir Visual Basic ifadesinin özellik kılavuzunda yazın.|
|*TypeArgument*|Doğru|İçindeki öğe türü T <xref:System.Collections.Generic.ICollection%601>. Varsayılan olarak, bu *TypeArgument* türü ayarlandığında **Int32**. Türü değiştirmek için değerini değiştirmek *TypeArgument* birleşik giriş kutusundaki özellik kılavuzunda.|
|<xref:System.Activities.Activity%601.Result%2A>|False|Belirtilen öğeyi koleksiyondan kaldırılıp kaldırılmadığını belirten bir değer. Sonucu bağlamak için bir değişken olarak belirtmek için bir değişken özellik kılavuzunda yazın|

## <a name="see-also"></a>Ayrıca bkz.

- [Koleksiyon](../workflow-designer/collection-activity-designers.md)
- [AddToCollection\<T>](../workflow-designer/addtocollection-t-activity-designer.md)
- [ClearCollection\<T>](../workflow-designer/clearcollection-t-activity-designer.md)
- [ExistsInCollection\<T>](../workflow-designer/existsincollection-t-activity-designer.md)
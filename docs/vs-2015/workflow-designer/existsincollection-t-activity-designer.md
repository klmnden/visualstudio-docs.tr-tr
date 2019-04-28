---
title: Existsıncollection&lt;T&gt; etkinlik Tasarımcısı | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-workflow-designer
ms.topic: reference
f1_keywords:
- System.Activities.Statements.ExistsInCollection`1.UI
ms.assetid: 0acf9a13-caf5-4bb4-ba22-ec37d2b7267a
caps.latest.revision: 6
author: gewarren
ms.author: gewarren
manager: jillfra
ms.openlocfilehash: 263bbf16c72bab5a42dc0ba1465d4c7062333071
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62952833"
---
# <a name="existsincollectionlttgt-activity-designer"></a>Existsıncollection&lt;T&gt; etkinlik Tasarımcısı
**Existsıncollection\<T >** etkinlik Tasarımcısı oluşturmak ve yapılandırmak için kullanılan bir <xref:System.Activities.Statements.ExistsInCollection%601> etkinlik.  
  
## <a name="the-existsincollectiont-activity"></a>Existsıncollection\<T > etkinliği  
 <xref:System.Activities.Statements.ExistsInCollection%601> Etkinlik belirtilen bir öğenin belirli bir koleksiyonda mevcut olup olmadığını belirler.  
  
### <a name="using-the-existsincollectiont-activity-designer"></a>Existsıncollection kullanarak\<T > etkinlik Tasarımcısı  
 **Existsıncollection\<T >** etkinlik Tasarımcısı bulunabilir **koleksiyon** kategorisi **araç kutusu**, hangi erişilen tıklayarak **Araç kutusu** sekmesinde [!INCLUDE[wfd2](../includes/wfd2-md.md)] (Alternatif olarak, seçin **araç** gelen **görünümü** menüsünden veya CTRL + ALT + X.)  
  
 **Existsıncollection\<T >** etkinlik Tasarımcısı, gelen sürüklenebilir **araç kutusu** ve oturum bırakılan [!INCLUDE[wfd2](../includes/wfd2-md.md)] yüzey yerde etkinlikleri genellikle yerleştirilir, gibi içinde bir <xref:System.Activities.Statements.Sequence>. Bu, oluşturur bir <xref:System.Activities.Statements.ExistsInCollection%601> etkinliği ile bir varsayılan <xref:System.Activities.Activity.DisplayName%2A> Existsıncollection,\<Int32 >. (Varsayılan olarak, *TypeArgument* olduğu **Int32**. Bu özellik kılavuzunda değiştirilebilir.)  <xref:System.Activities.Activity.DisplayName%2A> Değeri üst bilgisinde düzenlenebilir **Existsıncollection\<T >** etkinlik Tasarımcısı veya **DisplayName** özellik kılavuzunda kutusu. Özellik Kılavuzu'nun diğer özellikleri düzenlenmesi gerekir.  
  
### <a name="the-existsincollectiont-properties"></a>Existsıncollection\<T > Özellikleri  
 Aşağıdaki tabloda <xref:System.Activities.Statements.ExistsInCollection%601> özellikleri Tasarımcısı'nda nasıl kullanıldığı açıklanmaktadır.  
  
|Özellik Adı|Gerekli|Kullanım|  
|-------------------|--------------|-----------|  
|<xref:System.Activities.Activity.DisplayName%2A>|False|Kolay adı <xref:System.Activities.Statements.ExistsInCollection%601> etkinlik. Existsıncollection varsayılandır\<Int32 >. Ancak <xref:System.Activities.Activity.DisplayName%2A> değeri kesinlikle gerekli değil, kullanmak için en iyi bir uygulamadır.|  
|<xref:System.Activities.Statements.ExistsInCollection%601.Item%2A>|Doğru|Koleksiyona eklenecek öğe\<T >. Bu öğe türünde *T* türünde *TypeArgument*. Öğesini belirtmek için bir Visual Basic ifadesinin özellik kılavuzunda yazın.|  
|<xref:System.Activities.Statements.ExistsInCollection%601.Collection%2A>|Doğru|Öğesi eklenmesi gereken koleksiyon. Bu koleksiyonu türünde **ICollection\<TypeArgument >.** Koleksiyon belirtmek için bir Visual Basic ifadesinin özellik kılavuzunda yazın.|  
|*TypeArgument*|Doğru|İçindeki öğe türü T <xref:System.Collections.Generic.ICollection%601>. Varsayılan olarak, bu *TypeArgument* türü ayarlandığında **Int32**. Türü değiştirmek için değerini değiştirmek *TypeArgument* birleşik giriş kutusundaki özellik kılavuzunda.|  
|<xref:System.Activities.Activity%601.Result%2A>|False|Belirtilen öğe koleksiyonunda var olup olmadığını belirten bir değer. Sonucu bağlamak için bir değişken olarak belirtmek için bir Visual Basic değişken özellik kılavuzunda yazın.|  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Koleksiyon](../workflow-designer/collection-activity-designers.md)   
 [AddToCollection\<T >](../workflow-designer/addtocollection-t-activity-designer.md)   
 [ClearCollection\<T >](../workflow-designer/clearcollection-t-activity-designer.md)   
 [RemoveFromCollection\<T>](../workflow-designer/removefromcollection-t-activity-designer.md)
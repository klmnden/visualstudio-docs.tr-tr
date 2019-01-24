---
title: ClearCollection&lt;T&gt; etkinlik Tasarımcısı | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-workflow-designer
ms.topic: reference
f1_keywords:
- System.Activities.Statements.ClearCollection`1.UI
ms.assetid: db0e5da2-7b5a-4f1a-864c-f3aeeeeb51a7
caps.latest.revision: 7
author: gewarren
ms.author: gewarren
manager: jillfra
ms.openlocfilehash: 240e634115e7602c66d69f0dba9cfa52504dc89a
ms.sourcegitcommit: 8b538eea125241e9d6d8b7297b72a66faa9a4a47
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54763610"
---
# <a name="clearcollectionlttgt-activity-designer"></a>ClearCollection&lt;T&gt; etkinlik Tasarımcısı
**ClearCollection\<T >** etkinlik Tasarımcısı oluşturmak ve yapılandırmak için kullanılan bir <xref:System.Activities.Statements.ClearCollection%601> etkinlik.  
  
## <a name="the-clearcollectiont-activity"></a>ClearCollection\<T > etkinliği  
 <xref:System.Activities.Statements.ClearCollection%601> Etkinlik belirtilen tüm öğeleri koleksiyonu temizler.  
  
### <a name="using-the-clearcollectiont-activity-designer"></a>ClearCollection kullanarak\<T > etkinlik Tasarımcısı  
 **ClearCollection\<T >** etkinlik Tasarımcısı bulunabilir **koleksiyon** kategorisi **araç kutusu**, hangi erişilen tıklayarak **Araç kutusu** sekmesinde [!INCLUDE[wfd2](../includes/wfd2-md.md)] (Alternatif olarak, seçin **araç** gelen **görünümü** menüsünden veya CTRL + ALT + X.)  
  
 **ClearCollection\<T >** etkinlik Tasarımcısı, gelen sürüklenebilir **araç kutusu** ve oturum bırakılan [!INCLUDE[wfd2](../includes/wfd2-md.md)] yüzey yerde etkinlikleri genellikle yerleştirilir, örneğin olarak içinde bir <xref:System.Activities.Statements.Sequence>. Bu, oluşturur bir <xref:System.Activities.Statements.ClearCollection%601> etkinliği ile bir varsayılan <xref:System.Activities.Activity.DisplayName%2A> ClearCollection,\<Int32 >. (Varsayılan olarak, *TypeArgument* olduğu **Int32**. Bu özellik kılavuzunda değiştirilebilir.) <xref:System.Activities.Activity.DisplayName%2A> Değeri üst bilgisinde düzenlenebilir **ClearCollection\<T >** etkinlik Tasarımcısı veya **DisplayName** özellik kılavuzunda kutusu. Özellik Kılavuzu'nun diğer özellikleri düzenlenmesi gerekir.  
  
### <a name="the-clearcollectiont-properties"></a>ClearCollection\<T > Özellikleri  
 Aşağıdaki tabloda <xref:System.Activities.Statements.ClearCollection%601> özellikleri Tasarımcısı'nda nasıl kullanıldığı açıklanmaktadır.  
  
|Özellik Adı|Gerekli|Kullanım|  
|-------------------|--------------|-----------|  
|<xref:System.Activities.Activity.DisplayName%2A>|False|İsteğe bağlı kolay adı belirtir <xref:System.Activities.Statements.ClearCollection%601> etkinlik. ClearCollection varsayılandır\<Int32 >. Ancak <xref:System.Activities.Activity.DisplayName%2A> değeri kesinlikle gerekli değil, kullanmak için en iyi bir uygulamadır.|  
|<xref:System.Activities.Statements.ClearCollection%601.Collection%2A>|Doğru|Öğelerin temizlenecek koleksiyonu belirtir. Bu koleksiyonu türünde **ICollection\<TypeArgument >.** Koleksiyon belirtmek için bir Visual Basic ifadesinin özellik kılavuzunda yazın.|  
|*TypeArgument*|Doğru|İçindeki öğe türü T belirtir <xref:System.Collections.Generic.ICollection%601>. Varsayılan olarak, bu *TypeArgument* türü ayarlandığında **Int32**. Türü değiştirmek için değerini değiştirmek *TypeArgument* birleşik giriş kutusundaki özellik kılavuzunda.|  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Koleksiyon](../workflow-designer/collection-activity-designers.md)   
 [AddToCollection\<T >](../workflow-designer/addtocollection-t-activity-designer.md)   
 [Existsıncollection\<T >](../workflow-designer/existsincollection-t-activity-designer.md)   
 [RemoveFromCollection\<T >](../workflow-designer/removefromcollection-t-activity-designer.md)
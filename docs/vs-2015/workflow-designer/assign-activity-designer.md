---
title: Assign etkinlik Tasarımcısı | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-workflow-designer
ms.topic: reference
f1_keywords:
- System.Activities.Statements.Assign.UI
ms.assetid: ba3feb3c-f144-47ea-926d-cf752b804153
caps.latest.revision: 6
author: gewarren
ms.author: gewarren
manager: jillfra
ms.openlocfilehash: 111f53ec5b427207a6bde5d590cf8f1c908ff130
ms.sourcegitcommit: 8b538eea125241e9d6d8b7297b72a66faa9a4a47
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54766130"
---
# <a name="assign-activity-designer"></a>Assign Etkinlik Tasarımcısı
**Atama** etkinlik Tasarımcısı oluşturmak ve yapılandırmak için kullanılan bir <xref:System.Activities.Statements.Assign> etkinlik.  
  
## <a name="the-assign-activity"></a>Ata etkinliği  
 <xref:System.Activities.Statements.Assign> Etkinliği, bir değişken veya bağımsız değişken bir değer atar.  
  
### <a name="using-the-assign-activity-designer"></a>Ata etkinlik Tasarımcısını kullanma  
 **Atama** etkinlik Tasarımcısı bulunabilir **Temelleri** kategorisi **araç kutusu**, hangi erişilen tıklayarak **araç kutusu**sekme (Alternatif olarak, seçin **araç kutusu** gelen **görünümü** menüsünden veya CTRL + ALT + X.)  
  
 **Atama** etkinlik Tasarımcısı, gelen sürüklenebilir **araç kutusu** ve oturum bırakılan [!INCLUDE[wfd2](../includes/wfd2-md.md)] yüzey nerede hiç etkinlikleri genellikle yerleştirilir, gibi olarak içinde bir <xref:System.Activities.Statements.Sequence>. Bu, oluşturur bir <xref:System.Activities.Statements.Assign> etkinliği ile bir varsayılan **DisplayName** Ata'nın. <xref:System.Activities.Activity.DisplayName%2A> Üst bilgisinde düzenlenebilir **atama** etkinlik Tasarımcısı veya **DisplayName** özellik kılavuzunda kutusu.  
  
### <a name="the-assign-properties"></a>Ata özellikleri  
 Aşağıdaki tabloda <xref:System.Activities.Statements.Assign> özellikleri Tasarımcısı'nda nasıl kullanıldığı açıklanmaktadır. Bu özellikler, özellik kılavuzunda düzenlenebilir ve bunlardan bazıları üzerinde düzenlenebilir [!INCLUDE[wfd2](../includes/wfd2-md.md)] yüzeyi.  
  
|Özellik Adı|Gerekli|Kullanım|  
|-------------------|--------------|-----------|  
|<xref:System.Activities.Activity.DisplayName%2A>|False|Kolay adı <xref:System.Activities.Statements.Assign> etkinlik. Ata varsayılandır. Ancak <xref:System.Activities.Activity.DisplayName%2A> değeri kesinlikle gerekli değil, kullanmak için en iyi bir uygulamadır.|  
|<xref:System.Activities.Statements.Assign.To%2A>|Doğru|Değişken veya bağımsız değişken olarak <xref:System.Activities.Statements.Assign.Value%2A> atanır. Bu, geçerli bir Visual Basic tanımlayıcısı olması gerekir. Özellik ayarlamak için bir Visual Basic ifadesinin türü **için** kutusuna **atama** etkinlik Tasarımcısı veya özellik kılavuzunda.|  
|<xref:System.Activities.Statements.Assign.Value%2A>|Doğru|Değişkene atanan değer. Ayarlanacak <xref:System.Activities.Statements.Assign.Value%2A>, Visual Basic ifadesindeki türü **değer** kutusuna **atama** etkinlik Tasarımcısı veya özellik kılavuzunda.|  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Temel öğeler](../workflow-designer/primitives-activity-designers.md)   
 [gecikme](../workflow-designer/delay-activity-designer.md)   
 [InvokeMethod](../workflow-designer/invokemethod-activity-designer.md)   
 [WriteLine](../workflow-designer/writeline-activity-designer.md)
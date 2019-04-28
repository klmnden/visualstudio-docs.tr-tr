---
title: Gecikme etkinlik Tasarımcısı | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-workflow-designer
ms.topic: reference
f1_keywords:
- System.Activities.Statements.Delay.UI
ms.assetid: f51742a8-2c9a-47d1-8a23-18459d03ae19
caps.latest.revision: 8
author: gewarren
ms.author: gewarren
manager: jillfra
ms.openlocfilehash: 528317a97a9b2582442dacfcf9ba8a35943736e8
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62976710"
---
# <a name="delay-activity-designer"></a>Delay Etkinlik Tasarımcısı
**Gecikme** etkinlik Tasarımcısı oluşturmak ve yapılandırmak için kullanılan bir <xref:System.Activities.Statements.Delay> etkinlik.  
  
## <a name="the-delay-activity"></a>Delay etkinlik  
 <xref:System.Activities.Statements.Delay> Etkinlik belirtilen bir süre için bir iş akışı yürütülmesini geciktirir.  
  
### <a name="using-the-delay-activity-designer"></a>Delay etkinlik Tasarımcısı kullanma  
 **Gecikme** etkinlik Tasarımcısı bulunabilir **Temelleri** kategorisi **araç kutusu**, hangi erişilen tıklayarak **araç kutusu**sekmesinde [!INCLUDE[wfd2](../includes/wfd2-md.md)] (Alternatif olarak, seçin **araç** gelen **görünümü** menüsünü veya CTRL + ALT + X.)  
  
 **Gecikme** etkinlik Tasarımcısı, gelen sürüklenebilir **araç kutusu** ve oturum bırakılan [!INCLUDE[wfd2](../includes/wfd2-md.md)] yüzey yerde etkinlikleri genellikle yerleştirilir, örneğin olarak içinde bir <xref:System.Activities.Statements.Sequence>. Bu, oluşturur bir <xref:System.Activities.Statements.Delay> etkinliği ile bir varsayılan <xref:System.Activities.Activity.DisplayName%2A> gecikme. <xref:System.Activities.Activity.DisplayName%2A> Üst bilgisinde düzenlenebilir **gecikme** etkinlik Tasarımcısı veya **DisplayName** özellik kılavuzunda kutusu.  
  
### <a name="the-delay-properties"></a>Gecikmeli Özellikler  
 Aşağıdaki tabloda <xref:System.Activities.Statements.Delay> özellikleri Tasarımcısı'nda nasıl kullanıldığı açıklanmaktadır. Bu özellikler, özellik kılavuzunda düzenlenebilir ve bunlardan bazıları üzerinde düzenlenebilir [!INCLUDE[wfd2](../includes/wfd2-md.md)]Tasarımcı yüzeyine bırakın.  
  
|Özellik Adı|Gerekli|Kullanım|  
|-------------------|--------------|-----------|  
|<xref:System.Activities.Activity.DisplayName%2A>|False|Kolay adı <xref:System.Activities.Statements.Delay> etkinlik. Gecikme varsayılandır. Ancak <xref:System.Activities.Activity.DisplayName%2A> değeri kesinlikle gerekli değil, kullanmak için en iyi bir uygulamadır.|  
|<xref:System.Activities.Statements.Delay.Duration%2A>|Doğru|İş akışı gecikme süre miktarı. Bu özellik, özellik kılavuzunda ayarlanır. Bir sabit değer yazın ya da <xref:System.TimeSpan> 00:00:00 biçimi veya süreyi belirtmek için bir Visual Basic ifade.|  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Temel öğeler](../workflow-designer/primitives-activity-designers.md)   
 [Ata](../workflow-designer/assign-activity-designer.md)   
 [Delay etkinlik Tasarımcısı](../workflow-designer/delay-activity-designer.md)   
 [InvokeMethod](../workflow-designer/invokemethod-activity-designer.md)   
 [WriteLine](../workflow-designer/writeline-activity-designer.md)
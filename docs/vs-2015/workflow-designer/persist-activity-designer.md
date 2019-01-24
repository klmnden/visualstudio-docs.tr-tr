---
title: Persist etkinlik Tasarımcısı | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-workflow-designer
ms.topic: reference
f1_keywords:
- System.Activities.Statements.Persist.UI
ms.assetid: be8648dd-3eb9-4a50-8ec1-57a8be804692
caps.latest.revision: 6
author: gewarren
ms.author: gewarren
manager: jillfra
ms.openlocfilehash: f87997178f98e9e632b756b5a4440c19544b5c86
ms.sourcegitcommit: 8b538eea125241e9d6d8b7297b72a66faa9a4a47
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54779384"
---
# <a name="persist-activity-designer"></a>Persist Etkinlik Tasarımcısı
**Kalan** etkinlik Tasarımcısı oluşturmak ve yapılandırmak için kullanılan bir <xref:System.Activities.Statements.Persist> etkinlik.  
  
## <a name="the-persist-activity"></a>Persist etkinlik  
 <xref:System.Activities.Statements.Persist> Etkinliğini bir iş akışı mümkünse diske kaydeder. <xref:System.Activities.Statements.Persist> Etkinlik yürütülemiyor alanında bir Kalıcılık olmayan, örneğin, içinde bir <xref:System.Activities.Statements.TransactionScope> etkinlik. Kullanıyorsanız bir <xref:System.Activities.Statements.Persist> etkinlik kalıcı olmayan bir kapsam içinde bir özel durumu çalışma zamanında oluşturulur.  
  
### <a name="using-the-persist-activity-designer"></a>Kullanarak Persist etkinlik Tasarımcısı  
 **Kalan** etkinlik Tasarımcısı bulunabilir **çalışma zamanı** kategorisi **araç kutusu**, hangi erişilen tıklayarak **araç kutusu** sekme (Alternatif olarak, seçin **araç kutusu** gelen **görünümü** menüsünden veya CTRL + ALT + X.)  
  
 **Kalan** etkinlik Tasarımcısı, gelen sürüklenebilir **araç kutusu** ve oturum bırakılan [!INCLUDE[wfd2](../includes/wfd2-md.md)] yüzey yerde etkinlikleri genellikle yerleştirilir, örneğin olarak içinde bir <xref:System.Activities.Statements.Sequence>. Bu, oluşturur bir <xref:System.Activities.Statements.Persist> etkinliği ile bir varsayılan **DisplayName** kalan. <xref:System.Activities.Activity.DisplayName%2A> Üst bilgisinde düzenlenebilir **kalan** etkinlik Tasarımcısı veya **DisplayName** özellik kılavuzunda kutusu.  
  
### <a name="the-persist-properties"></a>Kalıcı özellikleri  
 Aşağıdaki tabloda <xref:System.Activities.Statements.Persist> özellikleri Tasarımcısı'nda nasıl kullanıldığı açıklanmaktadır. Bu özellikler, özellik kılavuzunda düzenlenebilir ve bunlardan bazıları üzerinde düzenlenebilir [!INCLUDE[wfd2](../includes/wfd2-md.md)] yüzeyi.  
  
|Özellik Adı|Gerekli|Kullanım|  
|-------------------|--------------|-----------|  
|<xref:System.Activities.Activity.DisplayName%2A>|False|Kolay adı <xref:System.Activities.Statements.Persist> etkinlik. Kalan varsayılandır. Görünen ad kesinlikle gerekli olmamakla birlikte, bir görünen ad kullanmak için en iyi bir uygulamadır.|  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Çalışma zamanı](../workflow-designer/runtime-activity-designers.md)   
 [TerminateWorkflow](../workflow-designer/terminateworkflow-activity-designer.md)
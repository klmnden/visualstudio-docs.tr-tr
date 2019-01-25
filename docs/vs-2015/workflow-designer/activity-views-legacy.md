---
title: Etkinlik görünümleri (eski) | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-workflow-designer
ms.topic: reference
helpviewer_keywords:
- activities, activity views
- views, activity
- activity views
ms.assetid: 83dc68cd-2cb2-45c2-9a6e-10d82053171a
caps.latest.revision: 5
author: gewarren
ms.author: gewarren
manager: jillfra
ms.openlocfilehash: 62b3c9185226512ff28c8d028cd0ba7d33b0f12f
ms.sourcegitcommit: 8b538eea125241e9d6d8b7297b72a66faa9a4a47
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54777658"
---
# <a name="activity-views-legacy"></a>Etkinlik Görünümleri (Eski)
Tarafından sağlanan etkinliklerinin birçok [!INCLUDE[wf](../includes/wf-md.md)], hangi iş akışları öğesinden oluşur, çeşitli tasarım görünümlerini eski içinde kullanılabilir olan [!INCLUDE[wfd1](../includes/wfd1-md.md)]. Bir etkinlik Tasarımcısı'ndan sürüklediğinizde **araç kutusu** tasarım yüzeyine ve bundan sonra etkinliği seçtiğinizde kullanın ya da farklı tasarım görünümler arasında geçiş yapabilirsiniz **iş akışı**menü veya sağ tıklayarak seçili etkinlik. Seçili etkinlik adı üzerinde işaretçiyi getirdiğinizde, ayrıca, farklı görünümler arasında geçiş yapmak için kullanabileceğiniz bir sekme açılır kümesi görünür.  
  
 Her etkinlik, en az bir görünüme sahiptir; Bu bir etkinlik Tasarımcısı'ndan sürüklediğinizde gösterilen varsayılan görünümü şu şekildedir **araç kutusu** tasarım yüzeyine. Bu etkinlik varsayılan görünüm olarak kullanılabilir **[etkinlik türü] görüntülemek** seçeneği menüleri ve sekmelerinde, örneğin, **görünümü paralel**. Ek görünümler etkinliklerin çoğunu sahip ve farklı görünümleri farklı olabilir. Örneğin, [TransactionScopeActivity](http://go.microsoft.com/fwlink?LinkID=65093) etkinliğinde maaş görünümü ve [EventHandlingScopeActivity](http://go.microsoft.com/fwlink?LinkID=65030) etkinliğinde bir olay görünümü. Çoğu Windows Workflow Foundation ile gelen etkinliklerinin **görünümü iptal işleyicisi** ve **görünümü hataları** Tasarım görünümüne görünümleri [CancellationHandlerActivity](http://go.microsoft.com/fwlink?LinkID=65050) ve [FaultHandlersActivity](http://go.microsoft.com/fwlink?LinkID=65055) ilişkili.  
  
 Aşağıdaki tabloda, ad ve açıklama her görünümün listeler.  
  
|Menü/sekmesi seçeneği|Açıklama|  
|----------------------|-----------------|  
|**Görünüm [etkinlik türü]**|Seçili etkinlik varsayılan grafik gösterimi görüntülemek için bu menü veya sekme seçeneği belirleyin.|  
|**Görünüm iptal işleyicisi**|Bu menü veya sekmesinde görünüm için görünüm seçeneği [CancellationHandlerActivity](http://go.microsoft.com/fwlink?LinkID=65050) seçilen etkinlikle ilişkilendirilmiş.|  
|**Hata işleyicisini görüntüle**|Bu menü veya sekmesinde görünüm için görünüm seçeneği [FaultHandlersActivity](http://go.microsoft.com/fwlink?LinkID=65055) seçilen etkinlikle ilişkilendirilmiş.|  
|**Dengeleme İşleyicisini Görüntüle**|Bu menü veya sekmesinde görünüm için görünüm seçeneği [CompensationHandlerActivity](http://go.microsoft.com/fwlink?LinkID=65053) seçili ile ilişkili [TransactionScopeActivity](http://go.microsoft.com/fwlink?LinkID=65093).|  
|**Olay işleyicisini görüntüle**|Bu menü veya sekmesinde görünüm için görünüm seçeneği [EventHandlersActivity](http://go.microsoft.com/fwlink?LinkID=65018) seçili ile ilişkili [EventHandlingScopeActivity](http://go.microsoft.com/fwlink?LinkID=65030).|  
  
 Benzer görünümleri hakkında daha fazla bilgi için bkz: [sıralı iş akışı görünümleri (eski)](../workflow-designer/sequential-workflow-views-legacy.md).  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Eski iş akışı etkinlikleri](../workflow-designer/legacy-workflow-activities.md)   
 [Sıralı İş Akışı Görünümleri (Eski)](../workflow-designer/sequential-workflow-views-legacy.md)
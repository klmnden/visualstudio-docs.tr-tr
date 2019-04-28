---
title: CancellationScope etkinlik Tasarımcısı | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-workflow-designer
ms.topic: reference
f1_keywords:
- System.Activities.Statements.CancellationScope.UI
ms.assetid: 2c85d663-b219-4142-9866-7693ffd46379
caps.latest.revision: 8
author: gewarren
ms.author: gewarren
manager: jillfra
ms.openlocfilehash: 6207d1fcd2e920de979a13624e5cf1b442c2703c
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62977210"
---
# <a name="cancellationscope-activity-designer"></a>CancellationScope Etkinlik Tasarımcısı
**CancellationScope** etkinlik Tasarımcısı oluşturmak ve yapılandırmak için kullanılan bir <xref:System.Activities.Statements.CancellationScope> etkinlik.  
  
## <a name="the-cancellationscope-activity"></a>CancellationScope etkinlik  
 <xref:System.Activities.Statements.CancellationScope> Etkinlik, Etkinlik yürütme ve iptal etme mantığı Bu etkinliğin belirtmenize olanak sağlar.  
  
### <a name="using-the-cancellationscope-activity-designer"></a>CancellationScope etkinlik Tasarımcısı kullanma  
 **CancellationScope** etkinlik Tasarımcısı bulunabilir **işlem** kategorisi **araç kutusu**, hangi erişilen tıklayarak **araç kutusu**  sekmesinde [!INCLUDE[wfd2](../includes/wfd2-md.md)] (Alternatif olarak, seçin **araç** gelen **görünümü** menüsünü veya CTRL + ALT + X.)  
  
 **CancellationScope** etkinlik Tasarımcısı, gelen sürüklenebilir **araç kutusu** ve oturum bırakılan [!INCLUDE[wfd2](../includes/wfd2-md.md)] yüzey yerde etkinlikleri genellikle yerleştirilir, örneğin olarak içinde bir <xref:System.Activities.Statements.Sequence>. Bu, oluşturur bir <xref:System.Activities.Statements.CancellationScope> etkinliği ile bir varsayılan <xref:System.Activities.Activity.DisplayName%2A> CancellationScope biri. <xref:System.Activities.Activity.DisplayName%2A> Değeri üst bilgisinde düzenlenebilir **CancellationScope** etkinlik Tasarımcısı veya **DisplayName** özellik kılavuzunda kutusu.  
  
### <a name="the-cancellationscope-properties"></a>CancellationScope özellikleri  
 Aşağıdaki tabloda <xref:System.Activities.Statements.CancellationScope> özellikleri Tasarımcısı'nda nasıl kullanıldığı açıklanmaktadır. <xref:System.Activities.Activity.DisplayName%2A> Özelliği özellik kılavuzunda düzenlenebilir ancak diğer özellikleri üzerinde düzenlenmelidir [!INCLUDE[wfd2](../includes/wfd2-md.md)] yüzeyi.  
  
|Özellik Adı|Gerekli|Kullanım|  
|-------------------|--------------|-----------|  
|<xref:System.Activities.Activity.DisplayName%2A>|False|İsteğe bağlı kolay adı <xref:System.Activities.Statements.CancellationScope> etkinlik. CancellationScope varsayılandır. Ancak <xref:System.Activities.Activity.DisplayName%2A> değeri kesinlikle gerekli değil, kullanmak için en iyi bir uygulamadır.|  
|<xref:System.Activities.Statements.CancellationScope.Body%2A>|Doğru|Hangi iptal için sağlanan mantıksal etkinlik belirtir. Eklemek için <xref:System.Activities.Statements.CancellationScope.Body%2A> etkinlik, açılan bir etkinlikten **araç kutusu** içine **gövdesi** kutusuna **CancellationScope** ipucu metnini "bırakma ile etkinlik Tasarımcısı Etkinlik burada".|  
|<xref:System.Activities.Statements.CancellationScope.CancellationHandler%2A>|Doğru|İptal durumunda çalıştırılan etkinlik belirtir. Eklemek için <xref:System.Activities.Statements.CancellationScope.CancellationHandler%2A> etkinlik, açılan bir etkinlikten **araç kutusu** içine **CancellationHandler** kutusuna **CancellationScope** ipucuyla birlikte etkinlik Tasarımcısı "Etkinliği buraya bırakın" metin.|  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [İşlem](../workflow-designer/transaction-activity-designers.md)   
 [CompensableActivity](../workflow-designer/compensableactivity-activity-designer.md)   
 [Telafi](../workflow-designer/compensate-activity-designer.md)   
 [Onayla](../workflow-designer/confirm-activity-designer.md)   
 [TransactionScope](../workflow-designer/transactionscope-activity-designer.md)
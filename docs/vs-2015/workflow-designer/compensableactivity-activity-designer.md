---
title: CompensableActivity etkinlik Tasarımcısı | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-workflow-designer
ms.topic: reference
f1_keywords:
- System.Activities.Statements.CompensableActivity.UI
ms.assetid: e0340d89-d39e-4a52-8557-13e27040d7b5
caps.latest.revision: 6
author: gewarren
ms.author: gewarren
manager: jillfra
ms.openlocfilehash: f11743e0027866fd45687f716f1989e98020c68e
ms.sourcegitcommit: 8b538eea125241e9d6d8b7297b72a66faa9a4a47
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54788707"
---
# <a name="compensableactivity-activity-designer"></a>CompensableActivity Etkinlik Tasarımcısı
**CompensableActivity** etkinlik Tasarımcısı oluşturmak ve yapılandırmak için kullanılan bir <xref:System.Activities.Statements.CompensableActivity> etkinlik.  
  
## <a name="the-compensableactivity-activity"></a>CompensableActivity etkinlik  
 <xref:System.Activities.Statements.CompensableActivity> Onaylanabilir veya işlemin başarıyla tamamlanmasından sonra dengelenebilecek iş birimi tanımlar.  
  
### <a name="using-the-compensableactivity-activity-designer"></a>CompensableActivity etkinlik Tasarımcısı kullanma  
 **CompensableActivity** etkinlik Tasarımcısı bulunabilir **işlem** kategorisi **araç kutusu**, hangi erişilen tıklayarak **araç kutusu**  sol tarafındaki sekmesinde [!INCLUDE[wfd2](../includes/wfd2-md.md)] (Alternatif olarak, seçin **araç** gelen **görünümü** menüsünü veya CTRL + ALT + X.)  
  
 **CompensableActivity** etkinlik Tasarımcısı, gelen sürüklenebilir **araç kutusu** ve oturum bırakılan [!INCLUDE[wfd2](../includes/wfd2-md.md)] yüzey yerde etkinlikleri genellikle yerleştirilir, örneğin olarak içinde bir <xref:System.Activities.Statements.Sequence>. Bu, oluşturur bir <xref:System.Activities.Statements.CompensableActivity> etkinliği ile bir varsayılan <xref:System.Activities.Activity.DisplayName%2A> CompensableActivity biri. <xref:System.Activities.Activity.DisplayName%2A> Değeri üst bilgisinde düzenlenebilir **CompensableActivity** etkinlik Tasarımcısı veya **DisplayName** özellik kılavuzunda kutusu.  
  
### <a name="the-compensableactivity-properties"></a>CompensableActivity özellikleri  
 Aşağıdaki tabloda <xref:System.Activities.Statements.CompensableActivity> özellikleri Tasarımcısı'nda nasıl kullanıldığı açıklanmaktadır. <xref:System.Activities.Activity.DisplayName%2A> Ve <xref:System.Activities.Activity%601.Result%2A> özelliği özellik kılavuzunda düzenlenebilir ancak diğer özellikleri üzerinde düzenlenmelidir [!INCLUDE[wfd2](../includes/wfd2-md.md)] yüzeyi.  
  
|Özellik Adı|Gerekli|Kullanım|  
|-------------------|--------------|-----------|  
|<xref:System.Activities.Activity.DisplayName%2A>|False|İsteğe bağlı kolay adı <xref:System.Activities.Statements.CompensableActivity> etkinlik. CompensableActivity varsayılandır.|  
|<xref:System.Activities.Activity%601.Result%2A>|False|Dönüş değerini belirtir <xref:System.Activities.Statements.CompensableActivity>. Bu özellik, özellik kılavuzunda düzenlenmelidir.|  
|<xref:System.Activities.Statements.CompensableActivity.Body%2A>|Doğru|Sağlanan maaş, iptal ve Doğrulama mantığı için etkinlik belirtir. Eklemek için <xref:System.Activities.Statements.CompensableActivity.Body%2A> etkinlik, açılan bir etkinlikten **araç kutusu** içine **gövdesi** kutusuna **CompensableActivity** ipucu metnini "bırakma ile etkinlik Tasarımcısı Etkinlik burada".|  
|<xref:System.Activities.Statements.CompensableActivity.CancellationHandler%2A>|False|İptal durumunda çalıştırılan etkinlik belirtir. Etkinlik eklemek için kendi Tasarımcısından bırak **araç kutusu** içine **CancellationHandler** kutusuna **CompensableActivity** ipucu metnini "bırakma ile etkinlik Tasarımcısı Etkinlik burada".|  
|<xref:System.Activities.Statements.CompensableActivity.CompensationHandler%2A>|False|Etkinlik için telafi bırakıldığında yürütülecek belirtir <xref:System.Activities.Statements.CompensableActivity.Body%2A> etkinlik. Bu işleyici açıkça çağrılabilir <xref:System.Activities.Statements.Compensate> etkinlik.<br /><br /> Etkinlik eklemek için etkinlik Tasarımcısı'ndan doğrudan **araç kutusu** içine **CompensationHandler** kutusuna **CompensableActivity** etkinlik Tasarımcısı ile ipucu metnini " Etkinliği buraya bırakın".|  
|<xref:System.Activities.Statements.CompensableActivity.ConfirmationHandler%2A>|False|Onaylama yürütülecek etkinliği <xref:System.Activities.Statements.CompensableActivity.Body%2A> etkinlik. Bu işleyici açıkça çağrılabilir <xref:System.Activities.Statements.Confirm> etkinlik.<br /><br /> Etkinlik eklemek için etkinlik Tasarımcısı'ndan doğrudan **araç kutusu** içine **ConfirmationHandler** kutusuna **CompensableActivity** etkinlik Tasarımcısı ile ipucu metnini " Etkinliği buraya bırakın".|  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [İşlem](../workflow-designer/transaction-activity-designers.md)   
 [CancellationScope](../workflow-designer/cancellationscope-activity-designer.md)   
 [Telafi](../workflow-designer/compensate-activity-designer.md)   
 [Onayla](../workflow-designer/confirm-activity-designer.md)   
 [TransactionScope](../workflow-designer/transactionscope-activity-designer.md)
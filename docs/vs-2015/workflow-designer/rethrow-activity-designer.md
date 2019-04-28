---
title: Rethrow etkinlik Tasarımcısı | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-workflow-designer
ms.topic: reference
f1_keywords:
- System.Activities.Statements.Rethrow.UI
ms.assetid: 9cfa2eda-395f-4cf3-9154-83fadd4f7452
caps.latest.revision: 5
author: gewarren
ms.author: gewarren
manager: jillfra
ms.openlocfilehash: 8b023a42da1c862927606c4bec0215120a5e5a11
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62937996"
---
# <a name="rethrow-activity-designer"></a>Rethrow Etkinlik Tasarımcısı
**Rethrow** etkinlik Tasarımcısı oluşturmak ve yapılandırmak için kullanılan bir <xref:System.Activities.Statements.Rethrow> etkinlik.  
  
## <a name="the-rethrow-activity"></a>Rethrow etkinlik  
 <xref:System.Activities.Statements.Rethrow> Etkinlik, daha önce oluşturulan bir özel durum oluşturur. Bu etkinlik yalnızca kullanılabilir bir <xref:System.Activities.Statements.Catch> işleyicisinde <xref:System.Activities.Statements.TryCatch> etkinlik.  
  
### <a name="using-the-rethrow-activity-designer"></a>ReThrow etkinlik Tasarımcısı kullanma  
 **Rethrow** etkinlik Tasarımcısı bulunabilir **hata işleme** kategorisi **araç kutusu**, hangi erişilen tıklayarak **araç kutusu**sol tarafındaki sekmesinde [!INCLUDE[wfd2](../includes/wfd2-md.md)] (Alternatif olarak, seçin **araç** gelen **görünümü** menüsünden veya CTRL + ALT + X.)  
  
 **Rethrow** etkinlik Tasarımcısı, gelen sürüklenebilir **araç kutusu** ve oturum bırakılan [!INCLUDE[wfd2](../includes/wfd2-md.md)] yüzey yerde etkinlikleri genellikle yerleştirilir, örneğin olarak içinde bir <xref:System.Activities.Statements.Sequence>. Bu, oluşturur bir <xref:System.Activities.Statements.Rethrow> etkinliği ile bir varsayılan **DisplayName** Throw biri. <xref:System.Activities.Activity.DisplayName%2A> Değeri üst bilgisinde düzenlenebilir **Rethrow** etkinlik Tasarımcısı veya **DisplayName** özellik kılavuzunda kutusu.  
  
### <a name="the-rethrow-properties"></a>Rethrow özellikleri  
 Aşağıdaki tabloda <xref:System.Activities.Statements.Rethrow> özellikleri Tasarımcısı'nda nasıl kullanıldığı açıklanmaktadır.  
  
|Özellik Adı|Gerekli|Kullanım|  
|-------------------|--------------|-----------|  
|<xref:System.Activities.Activity.DisplayName%2A>|False|İsteğe bağlı kolay adı belirtir <xref:System.Activities.Statements.Rethrow> etkinlik. Rethrow varsayılandır.|  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Koleksiyon](../workflow-designer/collection-activity-designers.md)   
 [throw](../workflow-designer/throw-activity-designer.md)   
 [TryCatch](../workflow-designer/trycatch-activity-designer.md)
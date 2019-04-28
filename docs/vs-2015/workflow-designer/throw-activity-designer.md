---
title: Throw etkinlik Tasarımcısı | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-workflow-designer
ms.topic: reference
f1_keywords:
- System.Activities.Statements.Throw.UI
ms.assetid: 5e97c947-be39-4a1f-af04-000e2e09528a
caps.latest.revision: 4
author: gewarren
ms.author: gewarren
manager: jillfra
ms.openlocfilehash: db909618971eeab2d92506d1c29b06290aa9263b
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62976626"
---
# <a name="throw-activity-designer"></a>Throw Etkinlik Tasarımcısı
**Throw** etkinlik Tasarımcısı oluşturmak ve yapılandırmak için kullanılan bir <xref:System.Activities.Statements.Throw> etkinlik.  
  
## <a name="the-throw-activity"></a>Throw etkinlik  
 <xref:System.Activities.Statements.Throw> Etkinlik bir özel durum oluşturur.  
  
### <a name="using-the-throw-activity-designer"></a>Throw etkinlik Tasarımcısı kullanma  
 **Throw** etkinlik Tasarımcısı bulunabilir **hata işleme** kategorisi **araç kutusu**, hangi erişilen tıklayarak **araç kutusu**sol tarafındaki sekmesinde [!INCLUDE[wfd2](../includes/wfd2-md.md)] (Alternatif olarak, seçin **araç** gelen **görünümü** menüsünü veya CTRL + ALT + X.)  
  
 **Throw** etkinlik Tasarımcısı, gelen sürüklenebilir **araç kutusu** ve oturum bırakılan [!INCLUDE[wfd2](../includes/wfd2-md.md)] yüzey yerde etkinlikleri genellikle yerleştirilir, örneğin olarak içinde bir <xref:System.Activities.Statements.Sequence>. Bu, oluşturur bir <xref:System.Activities.Statements.Throw> etkinliği ile bir varsayılan **DisplayName** Throw biri. <xref:System.Activities.Activity.DisplayName%2A> Değeri üst bilgisinde düzenlenebilir **Throw** etkinlik Tasarımcısı veya **DisplayName** özellik kılavuzunda kutusu. <xref:System.Activities.Statements.Throw.Exception%2A> Özellik Kılavuzu'nun özellik düzenlenemez.  
  
### <a name="the-throw-properties"></a>Throw özellikleri  
 Aşağıdaki tabloda <xref:System.Activities.Statements.Throw> özellikleri Tasarımcısı'nda nasıl kullanıldığı açıklanmaktadır.  
  
|Özellik Adı|Gerekli|Kullanım|  
|-------------------|--------------|-----------|  
|<xref:System.Activities.Activity.DisplayName%2A>|False|İsteğe bağlı kolay adı belirtir <xref:System.Activities.Statements.Throw> etkinlik. Throw varsayılandır.|  
|<xref:System.Activities.Statements.Throw.Exception%2A>|Doğru|Oluşturulacak özel durum. Bu özel durumun öğesinden türetilmelidir <xref:System.Exception>. Özel durumu belirtmek için bir Visual Basic ifadesinin özellik kılavuzunda yazın.|  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Koleksiyon](../workflow-designer/collection-activity-designers.md)   
 [yeniden oluşturma](../workflow-designer/rethrow-activity-designer.md)   
 [Throw etkinlik Tasarımcısı](../workflow-designer/throw-activity-designer.md)   
 [TryCatch](../workflow-designer/trycatch-activity-designer.md)
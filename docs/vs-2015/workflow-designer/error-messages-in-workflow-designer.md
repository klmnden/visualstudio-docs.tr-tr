---
title: İş akışı tasarımcısında hata iletileri | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-workflow-designer
ms.topic: reference
f1_keywords:
- WFDErrorMessages.UI
- System.Activities.Presentation.ErrorActivity.UI
- System.Activities.Presentation.View.ErrorView.UI
ms.assetid: 4d8bbc2e-34fc-477f-9140-4adfd70c34a0
caps.latest.revision: 5
author: gewarren
ms.author: gewarren
manager: jillfra
ms.openlocfilehash: 005a1db9d99b5eb91fb49d1694610cdc4ace9826
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62823318"
---
# <a name="error-messages-in-workflow-designer"></a>İş Akışı Tasarımcısında Hata İletileri
Bu konu ile çalışırken karşılaşılan hata iletileri türlerini açıklar [!INCLUDE[wfd1](../includes/wfd1-md.md)].  
  
## <a name="situations-in-which-errors-in-the-workflow-designer-occur"></a>İş akışı tasarımcısında hatalar oluşabilen durumları  
 Hataları [!INCLUDE[wfd2](../includes/wfd2-md.md)] aşağıdaki durumlarda oluşur:  
  
1. Bir ifadede bir hata var.  
  
2. Bir etkinliğin doğrulama kısıtlamaları karşılanmadı.  
  
3. Bir etkinlik yüklenemedi neden XAML dosyasındaki hataları vardır.  
  
4. Neden yüklenmesi başarısız iş akışı XAML dosyasındaki hataları vardır.  
  
   Geçersiz ifade ve hizmetlerinizden doğrulama kısıtlamalarını iş akışı oluşturmak başarısız olmasına neden olmaz. İş akışınızı oluşturma başarılı, ancak bir <xref:System.Activities.InvalidWorkflowException> çalışma zamanında oluşturulur. XAML dosyasında hatalar varsa derleme başarısız oluyor.  
  
   İçinde [!INCLUDE[vsprvs](../includes/vsprvs-md.md)], bir iş akışı yüklendiğinde, hatalar görüntülenir **hata listesi**. Hata kaynağı olan etkinliğin gitmek için hataya çift **hata listesi**.  
  
### <a name="expression-errors"></a>İfade hataları  
 Geçersiz bir ifade, kırmızı bir daire ifade yanındaki beyaz bir ünlem işaretiyle gösterilir. Bu simgenin üzerine geldiğinizde, hatanın kaynağını tanımlayan bir araç ipucu görüntülenir. İçinde [!INCLUDE[vsprvs](../includes/vsprvs-md.md)], ifade hatanın kaynağını çizip çizmeyeceğini satırı görüntülemek için tıklayın. Hatanın kaynağını tanımlayan bir araç ipucu çizgili metin görüntüler geldiğinizde.  
  
### <a name="activity-validation-errors"></a>Etkinlik doğrulama hataları  
 Bir etkinliğin doğrulama kısıtlamaları karşılanmadı etkinliğin sağ üst köşesindeki kırmızı bir daire beyaz bir ünlem işaretiyle görünür. Bu simgenin üzerine geldiğinizde, hatanın kaynağını tanımlayan bir araç ipucu görüntülenir.  
  
### <a name="xaml-load-errors"></a>XAML yükleme hataları  
 Bir etkinlik yük devrettiğinde metniyle "etkinlik XAML içindeki hatalar nedeniyle yüklenemedi" kırmızı kutu görünür. Bu genellikle, etkinliğin türü çözümlenemiyor oluşur. Geçersiz Etkinlik Tasarımcısı'nda kırmızı kutu seçip silerek silinebilir.  
  
### <a name="workflow-load-errors"></a>İş akışı yükleme hataları  
 Yüklenecek bir iş akışı başarısız olduğunda, "Belgenizi sorunlarla karşılaştı iş akışı Tasarımcısı" metin Tasarımcı yüzeyinde yüklemek iş akışının başarısızlığa neden özel durum bilgilerinin yanında görünür. Bu genellikle, XAML dosyası ayrıştırılamıyor oluşur.
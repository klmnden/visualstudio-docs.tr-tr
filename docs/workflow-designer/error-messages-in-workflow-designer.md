---
title: İş Akışı Tasarımcısında Hata İletileri
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- WFDErrorMessages.UI
- System.Activities.Presentation.ErrorActivity.UI
- System.Activities.Presentation.View.ErrorView.UI
ms.assetid: 4d8bbc2e-34fc-477f-9140-4adfd70c34a0
author: gewarren
ms.author: gewarren
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: ab2cb4562f816b254b658cfdc152dc38033fbe03
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62949713"
---
# <a name="error-messages-in-workflow-designer"></a>İş Akışı Tasarımcısında Hata İletileri

Bu konuda, iş akışı Tasarımcısı ile çalışırken karşılaşılan hata iletileri türleri açıklanmaktadır.

## <a name="situations-in-which-errors-in-the-workflow-designer-occur"></a>İş akışı tasarımcısında hatalar oluşabilen durumları

İş Akışı Tasarımcısı'nda hataları, aşağıdaki durumlarda oluşur:

1. Bir ifadede bir hata var.

2. Bir etkinliğin doğrulama kısıtlamaları karşılanmadı.

3. Bir etkinlik yüklenemedi neden XAML dosyasındaki hataları vardır.

4. Neden yüklenmesi başarısız iş akışı XAML dosyasındaki hataları vardır.

Geçersiz ifade ve hizmetlerinizden doğrulama kısıtlamalarını iş akışı oluşturmak başarısız olmasına neden olmaz. İş akışınızı oluşturma başarılı, ancak bir <xref:System.Activities.InvalidWorkflowException> çalışma zamanında oluşturulur. XAML dosyasında hatalar varsa derleme başarısız oluyor.

Bir iş akışı yüklendiğinde, Visual Studio içinde hatalar görüntülenir **hata listesi**. Hata kaynağı olan etkinliğin gitmek için hataya çift **hata listesi**.

### <a name="expression-errors"></a>İfade hataları
 Geçersiz bir ifade, kırmızı bir daire ifade yanındaki beyaz bir ünlem işaretiyle gösterilir. Bu simgenin üzerine geldiğinizde, hatanın kaynağını tanımlayan bir araç ipucu görüntülenir. Visual Studio içinde ifade hatanın kaynağını çizip çizmeyeceğini satırı görüntülemek için tıklayın. Hatanın kaynağını tanımlayan bir araç ipucu çizgili metin görüntüler geldiğinizde.

### <a name="activity-validation-errors"></a>Etkinlik doğrulama hataları
 Bir etkinliğin doğrulama kısıtlamaları karşılanmadı etkinliğin sağ üst köşesindeki kırmızı bir daire beyaz bir ünlem işaretiyle görünür. Bu simgenin üzerine geldiğinizde, hatanın kaynağını tanımlayan bir araç ipucu görüntülenir.

### <a name="xaml-load-errors"></a>XAML yükleme hataları
 Bir etkinlik yük devrettiğinde metniyle "etkinlik XAML içindeki hatalar nedeniyle yüklenemedi" kırmızı kutu görünür. Bu genellikle, etkinliğin türü çözümlenemiyor oluşur. Geçersiz Etkinlik Tasarımcısı'nda kırmızı kutu seçip silerek silinebilir.

### <a name="workflow-load-errors"></a>İş akışı yükleme hataları
 Yüklenecek bir iş akışı başarısız olduğunda, "Belgenizi sorunlarla karşılaştı iş akışı Tasarımcısı" metin Tasarımcı yüzeyinde yüklemek iş akışının başarısızlığa neden özel durum bilgilerinin yanında görünür. Bu genellikle, XAML dosyası ayrıştırılamıyor oluşur.
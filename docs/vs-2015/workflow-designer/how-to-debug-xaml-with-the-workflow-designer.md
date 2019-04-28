---
title: 'Nasıl yapılır: İş Akışı Tasarımcısı ile XAML hatalarını ayıklama | Microsoft Docs'
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-workflow-designer
ms.topic: reference
ms.assetid: d9305dbc-af62-4bdd-b03f-c54e3fe9ecc7
caps.latest.revision: 8
author: gewarren
ms.author: gewarren
manager: jillfra
ms.openlocfilehash: 0b8ed6bbb41b2fa3f54d825a13c16b064d010012
ms.sourcegitcommit: 47eeeeadd84c879636e9d48747b615de69384356
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "63444188"
---
# <a name="how-to-debug-xaml-with-the-workflow-designer"></a>Nasıl yapılır: İş Akışı Tasarımcısı ile XAML Hatalarını Ayıklama
İş akışı XAML açısından tanımlanır. İş akışı UI gösterimini iş akışını tanımlayan XAML ağaç üzerinde oluşturulmuştur. İş akışlarında hata ayıklama için hata ayıklama deneyimini benzer [!INCLUDE[wfd1](../includes/wfd1-md.md)]. Bunlar yaptığınız gibi örneği için XAML hata ayıklarken yerel öğeler, izleme ve iş parçacıkları windows aynı şekilde çalışır [!INCLUDE[wfd2](../includes/wfd2-md.md)] hata ayıklama. Ayrıca, XAML hata ayıklama sırasında çağrı yığınını görüntüle satırı tabanlı hiyerarşik bir görünümü yürütme akış iş akışı için ' dir.  
  
> [!NOTE]
> XAML iş akışı için etkinlikler aynı bütünleştirilmiş kod bulunuyorsa, sınıf adları derleme kısmı dahil değildir. Sınıf (etkinlik) adları bu kısmı XAML çalışma zamanında yüklenemez. Ana proje ile aynı ad alanında etkinlikleri tanımlamak için önerilmez; Aksi takdirde, XAML Tasarımcısı'nda düzenlenebilir sonra elle düzenlenerek olması gerekir.  
  
### <a name="to-debug-workflow-xaml"></a>İş akışı XAML hatalarını ayıklamak için  
  
1. İş akışı veya etkinlik proje açıp [!INCLUDE[vsprvs](../includes/vsprvs-md.md)].  
  
2. Bölümünde anlatıldığı gibi ayıklamak istediğiniz etkinlikleri ve etkinlik üzerinde bir kesme noktası ayarlamak [nasıl yapılır: İş akışlarında kesme noktası ayarlama](../workflow-designer/how-to-set-breakpoints-in-workflows.md).  
  
3. Seçin ve iş akışı tanımını içeren .xaml dosyasını sağ tıklatın **kodu görüntüle**. Tasarım görünümünde kesme noktasına kümesi etkinliğin XAML öğe bildirimi ile aynı satırda görüntülenen bir kesme noktası görürsünüz.  
  
4. Hata ayıklayıcısı içinde açıklanan şekilde çağırır [nasıl yapılır: İş akışı hata ayıklayıcısını çağırma](../workflow-designer/how-to-invoke-the-workflow-debugger.md).  
  
5. Kod yürütmeyi kesme noktalarınız ulaştığında, o kesme noktası ile ilişkili XAML öğe vurgulanır. Sonraki kesme noktasına gidin, **F10** veya **F11** anahtarı.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Nasıl yapılır: İş akışlarında kesme noktaları ayarlama](../workflow-designer/how-to-set-breakpoints-in-workflows.md)   
 [Nasıl yapılır: İş Akışı Hata Ayıklayıcısını Çağırma](../workflow-designer/how-to-invoke-the-workflow-debugger.md)
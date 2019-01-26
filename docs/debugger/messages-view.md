---
title: İletiler görünümünü | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
f1_keywords:
- vs.externaltools.spyplus.messagesview
helpviewer_keywords:
- Messages view
ms.assetid: 14c2a786-c23a-4b2d-acad-8c32a856c70d
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: db1b4ec3c2ae5fa0b24c3981e2b0296b54aec3cb
ms.sourcegitcommit: 2193323efc608118e0ce6f6b2ff532f158245d56
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/25/2019
ms.locfileid: "55016375"
---
# <a name="messages-view"></a>İletiler Görünümü
Her pencere bir ilişkili ileti akışı içerir. İletiler Görünümü penceresi bu ileti akışı görüntüler. Pencere tanıtıcısı, ileti kodu ve ileti gösterilir. Bir iş parçacığı veya işlem de bir iletiler görünümü oluşturabilirsiniz. Bu, belirli bir işlem veya pencere Başlatma iletilerinin yakalamak için özellikle yararlıdır iş parçacığı tarafından sahip olunan tüm windows gönderilen iletileri görüntülemenize olanak sağlar.  
  
 Tipik bir iletiler Görünümü penceresi altında görünür. İlk sütun pencere tanıtıcısı içerir ve ikinci sütun içeren bir ileti kodu Not (açıklandığı [iletisi kodlarını](../debugger/message-codes.md)). Kodu çözülen ileti parametreleri ve dönüş değerleri sağdadır.  
  
 ![Spy&#43; &#43; iletiler görünümünü](../debugger/media/spy--_messagesview.png "Spy ++ _MessagesView")  
Spy ++ iletiler görünümü  
  
## <a name="procedures"></a>Yordamlar  
  
#### <a name="to-open-a-messages-view-for-a-window-process-or-thread"></a>Bir pencere, işlem veya iş parçacığı için bir iletiler görünümünü açmak için  
  
1.  Odağı Taşı bir [Windows görünümü](../debugger/windows-view.md), [işlemler görünümü](../debugger/processes-view.md), veya [iş parçacıkları görünümü](../debugger/threads-view.md) penceresi.  
  
2.  Öğe için iletileri incelemek istediğiniz düğümü bulun ve seçin.  
  
3.  Gelen **Spy** menüsünde seçin **günlük iletilerini**.  
  
     [İleti seçenekleri iletişim kutusu](../debugger/message-options-dialog-box.md) açılır.  
  
4.  Görüntülemek istediğiniz iletisi için seçenekleri seçin.  
  
5.  Tuşuna **Tamam** günlük iletilerini başlatmak için.  
  
     Bir ileti Görünümü penceresini açar ve bir **iletileri** Spy ++ araç çubuğuna menü eklenir. Seçilen seçeneklere bağlı olarak, iletileri etkin iletileri görünüm penceresine akış başlayın.  
  
6.  Yeterli sayıda ileti olduğunda seçin **Günlüğü Durdur** gelen **iletileri** menüsü.  
  
## <a name="in-this-section"></a>Bu Bölümde  
 [İletiler görünümünü denetleme](../debugger/how-to-control-messages-view.md)  
 İletiler görünümü yönetmek açıklar.  
  
 [Bul penceresinden iletiler görünümünü açma](../debugger/how-to-open-messages-view-from-find-window.md)  
 Pencere Bul iletişim kutusundaki iletiler görünümünü açma açıklanmaktadır.  
  
 [İletiler görünümünde ileti arama](../debugger/how-to-search-for-a-message-in-messages-view.md)  
 Belirli bir ileti'ta iletiler görünümü bulmak açıklanmaktadır.  
  
 [Başlatma ve durdurma ileti günlüğü görüntüsü](../debugger/how-to-start-and-stop-the-message-log-display.md)  
 İleti günlüğe kaydetmeyi durdurmak ve başlatmak açıklanmaktadır.  
  
 [İleti Kodları](../debugger/message-codes.md)  
 İletiler Görünümü'nde listelenen iletilerin kodlarını tanımlar.  
  
 [İleti özelliklerini görüntüleme](../debugger/how-to-display-message-properties.md)  
 Bir ileti hakkında daha fazla bilgi görüntülemek nasıl.  
  
## <a name="related-sections"></a>İlgili Bölümler  
 [Spy++ Görünümleri](../debugger/spy-increment-views.md)  
 Spy ++ ağaç görünümlerini windows, iletileri, süreçleri ve iş parçacıkları açıklar.  
  
 [Spy++ kullanma](../debugger/using-spy-increment.md)  
 Spy ++ araç tanıtır ve nasıl kullanılacağını açıklar.  
  
 [İleti Seçenekleri İletişim Kutusu](../debugger/message-options-dialog-box.md)  
 İletileri etkin iletilerin Görünümü'nde listelenen seçmek için kullanılır.  
  
 [İleti Arama İletişim Kutusu](../debugger/message-search-dialog-box.md)  
 Düğüm iletiler görünümünde belirli bir ileti bulmak için kullanılır.  
  
 [İleti Özellikleri İletişim Kutusu](../debugger/message-properties-dialog-box.md)  
 İleti görünümünde seçilen bir ileti özelliklerini görüntülemek için kullanılır.  
  
 [Spy++ Başvurusu](../debugger/spy-increment-reference.md)  
 Her Spy ++ menü ve iletişim kutusunu tanımlayan bölümler içerir.
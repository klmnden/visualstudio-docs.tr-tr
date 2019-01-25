---
title: XAML Tasarımcısı'nda nesnelere animasyon ekleme | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-designers
ms.topic: conceptual
ms.assetid: fb88fa26-e835-47f5-9771-2f279441c83c
caps.latest.revision: 11
author: gewarren
ms.author: gewarren
manager: jillfra
ms.openlocfilehash: 7846ade8dba2ce849acf62311e508c157b07dd3e
ms.sourcegitcommit: 8b538eea125241e9d6d8b7297b72a66faa9a4a47
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54805515"
---
# <a name="animate-objects-in-xaml-designer"></a>XAML Tasarımcısı’nda nesnelere animasyon ekleme
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Nesneleri taşıma kısa animasyonlar oluşturma veya içeri ve dışarı Soldurma.  
  
 Başlamak için oluşturun bir *film şeridi*. Bir veya daha fazla görsel taslak içeren *zaman çizelgeleri*. Ayarlama *ana kareleri* özellik değişiklikleri işaretlemek için bir zaman çizelgesi üzerinde. Ardından, animasyon çalıştırdığınızda, Blend özellik değişikliklerini belirtilen süre içindeki ilişkilendirir. Sorunsuz bir geçiş sonucudur. Bir nesneye ait herhangi bir özelliğine animasyon, görsel olmayan özelliklere bile yapabilirsiniz.  
  
 Adlı bir görsel taslak aşağıdaki çizimde **MoveUp**. Bir dikdörtgen X ve Y konumunu işaretleyen ana kareleri Zaman Çizelgesi içerir. Bu animasyonu çalıştırdığında, dikdörtgen bir konumdan diğerine sorunsuz bir şekilde taşır.  
  
 ![](../designers/media/982f031a-74a3-414a-abc2-a0f41a741075.png "982f031a-74a3-414a-abc2-a0f41a741075")  
  
 Bu videoları izleyerek animasyonları oluşturmayı öğrenin.  
  
|Kısa bir video izleyin:|Şunları nasıl yapacağınızı öğrenin:|  
|--------------------------|-------------------|  
|![Yüklü Özellikleri Yapılandır](../designers/media/bldadminconsoleinitialconfigicon.PNG "BldAdminConsoleInitialConfigIcon") [zaman çizelgesini oluşturun](http://www.popscreen.com/v/6A4eF/Microsoft-Expression-Blend-Creating-Timelines)|Bir zaman çizelgesi oluşturun ve zaman çizelgesi nesneleri ile çalışır.|  
|![Yüklü Özellikleri Yapılandır](../designers/media/bldadminconsoleinitialconfigicon.PNG "BldAdminConsoleInitialConfigIcon") [ana kareleri ekleyin ve animasyonu yineleme](http://www.popscreen.com/v/6A4fi/Microsoft-Expression-Blend-Adding-Keyframes-and-Repeating-an-Animation)|Ana kareleri ekleyin ve her bir kareden özelliklerini ayarlayın. Ardından, animasyon ve izleme nesneleri sorunsuz geçiş aralarında çalıştırın.|  
|![Yüklü Özellikleri Yapılandır](../designers/media/bldadminconsoleinitialconfigicon.PNG "BldAdminConsoleInitialConfigIcon") [etkileşim için olay tetikleyicileri ekleme](http://www.popscreen.com/v/6A4e4/Microsoft-Expression-Blend-Adding-Event-Triggers-for-Interactivity)|Bir olay oluştuğunda animasyon başlatın. Örneğin, penceresi yüklendiğinde birini başlatın.|  
|![Yüklü Özellikleri Yapılandır](../designers/media/bldadminconsoleinitialconfigicon.PNG "BldAdminConsoleInitialConfigIcon") [renkleri animasyon ekleme](http://www.popscreen.com/v/6A4gv/Microsoft-Expression-Blend-Animating-Colors)|Bir nesnenin rengini değiştirmek için animasyon kullanın.|  
|![Yüklü Özellikleri Yapılandır](../designers/media/bldadminconsoleinitialconfigicon.PNG "BldAdminConsoleInitialConfigIcon") [oluşturma ve değiştirme hareket yolları](http://www.popscreen.com/v/6A4fX/Microsoft-Expression-Blend-Creating-and-Modifying-Motion-Paths)|Yol nesnelere animasyon ekleme.|  
|![Yüklü Özellikleri Yapılandır](../designers/media/bldadminconsoleinitialconfigicon.PNG "BldAdminConsoleInitialConfigIcon") [kolaylaştırmak ana kareler](http://www.popscreen.com/v/6A4dM/Microsoft-Expression-Blend-Easing-Keyframes)|Hız performansındaki veya bir animasyon başlangıcı yakınında yavaşlatmaz (*içinde kolaylaştırıcı*) veya sonlarında (*hızlandırma giden*) animasyonun.|  
|![Yüklü Özellikleri Yapılandır](../designers/media/bldadminconsoleinitialconfigicon.PNG "BldAdminConsoleInitialConfigIcon") [düğmeye animasyon ekleme](http://www.popscreen.com/v/6A4fK/Microsoft-Expression-Blend-Animating-a-Button)|Kullanıcının üzerine getirdiğinde üzerindeki bir düğme görünen ilginç efektleri oluşturun.|  
|![Yüklü Özellikleri Yapılandır](../designers/media/bldadminconsoleinitialconfigicon.PNG "BldAdminConsoleInitialConfigIcon") [animasyon oluşturmak ve iş ile hızlandırma](https://www.youtube.com/watch?v=mAJXYrwxGYo)|Bir kullanıcı bir düğme basılıyken görüntüsüne bir hesap makinesi bastığında görüntülenen Canlandır etkiler.|  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Visual Studio için Blend’i kullanarak kullanıcı arabirimi oluşturma](../designers/creating-a-ui-by-using-blend-for-visual-studio.md)

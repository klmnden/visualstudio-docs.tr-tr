---
title: "Nasıl yapılır: Bir ARM cihazla grafik Tanılama'yı kullanma | Microsoft Docs"
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-debug
ms.topic: conceptual
ms.assetid: 346fd3c0-9e92-4ab8-bb3b-1aa9000a2483
caps.latest.revision: 12
author: MikeJo5000
ms.author: mikejo
manager: jillfra
ms.openlocfilehash: 5bbe12449849b656af2658c5bab667b0e611515e
ms.sourcegitcommit: 08fc78516f1107b83f46e2401888df4868bb1e40
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/15/2019
ms.locfileid: "65685869"
---
# <a name="how-to-use-graphics-diagnostics-with-an-arm-device"></a>Nasıl yapılır: Bir ARM cihazla grafik Tanılama'yı kullanma
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Grafik tanılama Direct3D uygulamaların ARM tabanlı ve Windows RT 8.1 veya Windows Phone 8.1 çalıştıran cihazlarda uzaktan hata ayıklamayı destekler. Bir cihazda çalıştığı sırada Direct3D uygulamanızdan grafik bilgilerini yakalama veya cihaz için daha önce yakalanan grafik bilgilerini kayıttan yürütme makinesi olarak kullanın.  
  
## <a name="using-graphics-diagnostics-with-an-arm-based-device"></a>ARM tabanlı bir cihazla grafik tanılamayı kullanma  
 Visual Studio, ARM tabanlı cihazlarda çalışmadığı için bunlar üzerinde çalışan bir uygulama analiz etmek için uzaktan hata ayıklayıcı kullanmak zorunda. İşleme hataları tanılamanıza ve bu cihazlarda grafik performansı kolayca bunları uygulamanızda hata ayıklama gibi değerlendir uzaktan hata ayıklayıcı grafik yakalama ve kayıttan yürütme destekler.  
  
 Grafik tanılama özelliklerini kullanmak için önce Cihazınızda uzaktan hata ayıklamayı etkinleştirin.  
  
#### <a name="to-enable-remote-debugging-on-your-arm-based-device"></a>ARM tabanlı cihazda uzaktan hata ayıklamayı etkinleştirmek için  
  
1. Yükleme [ARM Kits ilkesini](https://msdn.microsoft.com/windows/desktop/dn469188) ARM tabanlı Cihazınızda.  
  
2. Yükleme [uzaktan hata ayıklama araçları](https://my.visualstudio.com/Downloads?q=remote%20tools%20visual%20studio%202015) ARM tabanlı Cihazınızda.  
  
> [!IMPORTANT]
> Windows Phone 8.1 cihazları için geliştirme için telefonunuzu kaydedin gerekebilir. Bunu yapmak için kayıtlı bir geliştirici olması gerekir. Daha fazla bilgi için [dağıtma ve Windows Phone 8 için uygulama çalıştırma](https://msdn.microsoft.com/library/windowsphone/develop/ff402565.aspx).  
  
 Uzaktan hata ayıklama Cihazınızda etkinleştirdikten sonra hata ayıklama hedefi kolaylaştırır ve grafik Tanılama'yı başlatın.  
  
#### <a name="to-configure-and-start-graphics-diagnostics-on-your-device"></a>Yapılandırma ve Cihazınızda grafik tanılama başlatmak için  
  
1. Üzerinde **çözüm platformları** aşağı açılan listesinden **ARM** ARM tabanlı cihaz uzaktan hata ayıklama hedefi olarak kullanılabilir olmayacaktır.  
  
2. Üzerinde **hata ayıklama hedefi** aşağı açılan listesinde, ARM Cihazınızı seçin.  
  
3. Menüsünde **hata ayıklama**, **grafik**, **tanılamayı Başlat**. (Klavye: Alt + F5)  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Uzak makinede Windows Store uygulamaları çalıştırma](../debugger/run-windows-store-apps-on-a-remote-machine.md)   
 [Nasıl yapılır: Grafik Tanılama Kayıttan Yürütme Makinesini Değiştirme](../debugger/how-to-change-the-graphics-diagnostics-playback-machine.md)

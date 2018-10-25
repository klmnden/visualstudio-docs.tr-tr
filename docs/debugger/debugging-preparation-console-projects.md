---
title: 'Hata ayıklama hazırlığı: Konsol projeleri | Microsoft Docs'
ms.custom: ''
ms.date: 11/04/2016
ms.technology: vs-ide-debug
ms.topic: reference
dev_langs:
- CSharp
- VB
- FSharp
- C++
helpviewer_keywords:
- debugging [Visual Studio], console applications
- debugging console applications
- console applications, debugging
ms.assetid: 9641f1d9-2d5a-48b1-8731-6525e8f67892
author: mikejo5000
ms.author: mikejo
manager: douge
ms.workload:
- multiple
ms.openlocfilehash: 516b2a6191cc76c3380875fda4679048e255f394
ms.sourcegitcommit: 240c8b34e80952d00e90c52dcb1a077b9aff47f6
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/23/2018
ms.locfileid: "49902087"
---
# <a name="debugging-preparation-console-projects"></a>Hata Ayıklama Hazırlığı: Konsol Projeleri
Bir konsol projesinde hata ayıklamaya hazırlanıyor, bazı ek hususlar ile bir Windows projede hata ayıklamak hazırlamaya benzerdir. Daha fazla bilgi için [Windows Forms uygulamaları](../debugger/debugging-preparation-windows-forms-applications.md), ve [hata ayıklama hazırlığı: Windows Forms uygulamaları (.NET)](https://docs.microsoft.com/previous-versions/visualstudio/visual-studio-2010/sez9z95a(v=vs.100)). Tüm konsol uygulamaları benzerlik nedeniyle, bu konu, aşağıdaki proje türlerini içerir:  
  
- C# konsol uygulaması  
  
- Visual Basic konsol uygulaması  
  
- C++ konsol uygulaması (.NET)  
  
- C++ konsol uygulaması (Win32)  
  
  Konsol uygulamanız için komut satırı bağımsız değişkenleri belirtmeniz gerekebilir. Daha fazla bilgi için [C++ hata ayıklama yapılandırması proje ayarları](../debugger/project-settings-for-a-cpp-debug-configuration.md), [Visual Basic hata ayıklama yapılandırması proje ayarları](../debugger/project-settings-for-a-visual-basic-debug-configuration.md), veya [C# hata ayıklama yapılandırmaları için proje ayarları ](../debugger/project-settings-for-csharp-debug-configurations.md).  
  
  Bu bağımsız değişkenler tüm proje özellikleri gibi Visual Studio oturumları arasında hata ayıklama oturumları arasında kalıcı hale getirin. Daha önce hataları ayıklanmakta bir konsol uygulaması ise, bu nedenle, girdiğiniz önceki oturumlarını bağımsız değişkenleri olabilir unutmayın  **\<Proje > özellik sayfaları** iletişim kutusu.  
  
  Bir konsol uygulaması kullanan **konsol** giriş kabul etmek ve çıkış iletileri görüntülemek için bir pencere. Yazılacak **konsol** penceresinde, uygulamanızın kullanmalıdır **konsol** hata ayıklama nesnesi yerine nesne. Yazılacak **Visual Studio çıkış** penceresi, hata ayıklama nesnesi zamanki kullanın. Burada, uygulama yazma veya yanlış yere iletiler için arıyor olabilirsiniz bildiğinizden emin olun. Daha fazla bilgi için [konsol sınıfı](/dotnet/api/system.console), [hata ayıklama sınıfı](/dotnet/api/system.diagnostics.debug), ve [çıkış penceresine](../ide/reference/output-window.md).  
  
## <a name="starting-the-application"></a>Uygulama başlatılıyor  
 Bazı konsol uygulamaları başlattığınızda tamamlanmak üzere çalıştırılmasını ve çıkın. Bu davranış yürütme sonu ve hata ayıklama için yeterli zaman sağlamayabilir. Bir uygulamada hata ayıklamak için uygulamayı başlatmak için aşağıdaki prosedürlerden birini kullanın:  
  
- Uygulamanızı çalıştırmaya başlar ve kesme noktasına erişene kadar çalışır.  
  
- Uygulamanız başlar ve kaynak kodu ilk satırında hemen keser.  
  
- Bir kaynak kodu penceresindeki bir satıra sağ tıklayın ve seçin **imlece kadar Çalıştır**.  
  
   Uygulamanız başlar ve önce satır kesme noktasına erişildiğinde seçili satır için ya da bir kesme noktası için çalışır.  
  
  Bir konsol uygulaması hata ayıklaması yaparken, komut isteminden yerine Visual Studio uygulamayı başlatmak isteyebilirsiniz. Bu durumda, uygulamayı komut isteminden başlatmak ve Visual Studio hata ayıklayıcısını ekleyebilir. Daha fazla bilgi için [çalışan işlemlere ekleme](../debugger/attach-to-running-processes-with-the-visual-studio-debugger.md).  
  
  Visual Studio'dan bir konsol uygulaması'nı başlattığınızda **konsol** penceresi bazen Visual Studio penceresinde görüntülenir. Konsol uygulamanızı Visual Studio ve hiçbir şey başlatmaya çalışırsanız görünüyor gerçekleşir, Visual Studio penceresine gitme deneyin.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Yerel kodda hata ayıklama](../debugger/debugging-native-code.md)   
 [Yönetilen kodda hata ayıklama](../debugger/debugging-managed-code.md)   
 [Visual C++ proje türleri](../debugger/debugging-preparation-visual-cpp-project-types.md)   
 [C#, F # ve Visual Basic proje türleri](../debugger/debugging-preparation-csharp-f-hash-and-visual-basic-project-types.md)   
 [C++ hata ayıklama yapılandırması proje ayarları](../debugger/project-settings-for-a-cpp-debug-configuration.md)   
 [Hata Ayıklayıcısı Güvenliği](../debugger/debugger-security.md)
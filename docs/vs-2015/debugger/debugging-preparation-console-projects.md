---
title: 'Hata ayıklama hazırlığı: Konsol projeleri | Microsoft Docs'
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-debug
ms.topic: conceptual
dev_langs:
- FSharp
- VB
- CSharp
- C++
helpviewer_keywords:
- debugging [Visual Studio], console applications
- debugging console applications
- console applications, debugging
ms.assetid: 9641f1d9-2d5a-48b1-8731-6525e8f67892
caps.latest.revision: 29
author: MikeJo5000
ms.author: mikejo
manager: jillfra
ms.openlocfilehash: 438e619be3e7650961709ef8fce8d69304d5c6ac
ms.sourcegitcommit: 8b538eea125241e9d6d8b7297b72a66faa9a4a47
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54793418"
---
# <a name="debugging-preparation-console-projects"></a>Hata ayıklama hazırlığı: Konsol Projeleri
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Bir konsol projesinde hata ayıklamaya hazırlanıyor, bazı ek hususlar ile bir Windows projede hata ayıklamak hazırlamaya benzerdir. Daha fazla bilgi için [Windows Forms uygulamaları](../debugger/debugging-preparation-windows-forms-applications.md), ve [hata ayıklama hazırlığı: Windows Forms uygulamalarında (.NET)](http://msdn.microsoft.com/a8bc54de-41a3-464d-9a12-db9bdcbc1ad5). Tüm konsol uygulamaları benzerlik nedeniyle, bu konu, aşağıdaki proje türlerini içerir:  
  
- C# konsol uygulaması  
  
- Visual Basic konsol uygulaması  
  
- C++ konsol uygulaması (.NET)  
  
- C++ konsol uygulaması (Win32)  
  
  Konsol uygulamanız için komut satırı bağımsız değişkenleri belirtmeniz gerekebilir. Daha fazla bilgi için [C++ hata ayıklama yapılandırması proje ayarları](../debugger/project-settings-for-a-cpp-debug-configuration.md), [Visual Basic hata ayıklama yapılandırması proje ayarları](../debugger/project-settings-for-a-visual-basic-debug-configuration.md), veya [C# hata ayıklama yapılandırmaları için proje ayarları ](../debugger/project-settings-for-csharp-debug-configurations.md).  
  
  Bu bağımsız değişkenler tüm proje özellikleri gibi Visual Studio oturumları arasında hata ayıklama oturumları arasında kalıcı hale getirin. Daha önce hataları ayıklanmakta bir konsol uygulaması ise, bu nedenle, girdiğiniz önceki oturumlarını bağımsız değişkenleri olabilir unutmayın  **\<Proje > özellik sayfaları** iletişim kutusu.  
  
  Bir konsol uygulaması kullanan **konsol** giriş kabul etmek ve çıkış iletileri görüntülemek için bir pencere. Yazılacak **konsol** penceresinde, uygulamanızın kullanmalıdır **konsol** hata ayıklama nesnesi yerine nesne. Yazılacak **Visual Studio çıkış** penceresi, hata ayıklama nesnesi zamanki kullanın. Burada, uygulama yazma veya yanlış yere iletiler için arıyor olabilirsiniz bildiğinizden emin olun. Daha fazla bilgi için [konsol sınıfı](https://msdn.microsoft.com/library/system.console.aspx), [hata ayıklama sınıfı](https://msdn.microsoft.com/library/system.diagnostics.debug.aspx), ve [çıkış penceresine](../ide/reference/output-window.md).  
  
## <a name="starting-the-application"></a>Uygulama başlatılıyor  
 Bazı konsol uygulamaları başlattığınızda tamamlanmak üzere çalıştırılmasını ve çıkın. Bu davranış yürütme sonu ve hata ayıklama için yeterli zaman sağlamayabilir. Bir uygulamada hata ayıklamak için uygulamayı başlatmak için aşağıdaki prosedürlerden birini kullanın:  
  
- Uygulamanız kesme noktasına ulaşır yürütme ve çalışan untils başlatır.  
  
- Uygulamanız başlar ve kaynak kodu ilk satırında hemen keser.  
  
- Bir kaynak kodu penceresindeki bir satıra sağ tıklayın ve seçin **imlece kadar Çalıştır**.  
  
   Uygulamanız başlar ve önce satır kesme noktasına erişildiğinde seçili satır için ya da bir kesme noktası için çalışır.  
  
  Bir konsol uygulaması hata ayıklaması yaparken, komut isteminden yerine Visual Studio uygulamayı başlatmak isteyebilirsiniz. Bu durumda, uygulamayı komut isteminden başlatmak ve Visual Studio hata ayıklayıcısını ekleyebilir. Daha fazla bilgi için [çalışan işlemlere ekleme](../debugger/attach-to-running-processes-with-the-visual-studio-debugger.md).  
  
  Visual Studio'dan bir konsol uygulaması'nı başlattığınızda **konsol** penceresi bazen Visual Studio penceresinde görüntülenir. Konsol uygulamanızı Visual Studio ve hiçbir şey başlatmaya çalışırsanız görünüyor gerçekleşir, Visual Studio penceresine gitme deneyin.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Yerel kodda hata ayıklama](../debugger/debugging-native-code.md)   
 [Yönetilen kodda hata ayıklama](../debugger/debugging-managed-code.md)   
 [Visual C++ proje türleri](../debugger/debugging-preparation-visual-cpp-project-types.md)   
 [C#, F#ve Visual Basic proje türleri](../debugger/debugging-preparation-csharp-f-hash-and-visual-basic-project-types.md)   
 [C++ hata ayıklama yapılandırması proje ayarları](../debugger/project-settings-for-a-cpp-debug-configuration.md)   
 [Hata Ayıklayıcısı Güvenliği](../debugger/debugger-security.md)

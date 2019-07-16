---
title: Hata ayıklama ve barındırma işlemi | Microsoft Docs
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
- debugging [Visual Studio], hosting process
- hosting process
ms.assetid: d0f0b9a6-2a6e-463d-b6ea-9518ee727933
caps.latest.revision: 13
author: MikeJo5000
ms.author: mikejo
manager: jillfra
ms.openlocfilehash: 10f3968367b188203671fa6bfff48bc482efe4f7
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "68157892"
---
# <a name="debugging-and-the-hosting-process"></a>Hata Ayıklama ve Barındırma İşlemi
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Visual Studio barındırma işlemini, hata ayıklayıcı performansı artırır ve kısmi güven hata ayıklama ve tasarım zamanı ifade değerlendirmesi gibi yeni hata ayıklayıcı özelliklerini etkinleştirir. Gerekirse, barındırma işlemini devre dışı bırakabilirsiniz. Daha fazla bilgi için [nasıl yapılır: Barındırma işlemini devre dışı](../ide/how-to-disable-the-hosting-process.md). Aşağıdaki bölümlerde, barındırma işlemi olmadan ve hata ayıklama arasındaki bazı farklar açıklanmaktadır.  
  
## <a name="partial-trust-debugging-and-click-once-security"></a>Kısmi güven hata ayıklama ve tıklayın-bir kez güvenlik  
 Kısmi güven hata ayıklama barındırma işlemini gerektiriyor. Barındırma işlemini devre dışı bırakırsanız, kısmi güven güvenliği etkinleştirilmiş olsa dahi kısmi güven hata ayıklama çalışmaz **güvenlik** sayfasının **proje özellikleri**. Daha fazla bilgi için [nasıl yapılır: Barındırma işlemini devre dışı](../ide/how-to-disable-the-hosting-process.md) ve [nasıl yapılır: Kısmen güvenilen uygulamada hata ayıklama](../debugger/how-to-debug-a-partial-trust-application.md).  
  
## <a name="design-time-expression-evaluation"></a>Tasarım zamanı ifade değerlendirmesi  
 Tasarım zamanı ifade her zaman, barındırma işlemi kullanır. Barındırma devre dışı bırakma işlemi **proje özellikleri** sınıf kitaplığı projeleri için tasarım zamanı ifade değerlendirmesi devre dışı bırakır. Diğer proje türleri için tasarım zamanı ifade değerlendirmesi devre dışı değil. Bunun yerine, Visual Studio gerçek yürütülebilir başlar ve barındırma işlemi olmadan tasarım zamanı değerlendirmesi için kullanır. Bu fark, farklı sonuçlar üretebilir.  
  
## <a name="appdomaincurrentdomainfriendlyname-differences"></a>AppDomain.CurrentDomain.FriendlyName farkları  
 `AppDomain.CurrentDomain.FriendlyName` barındırma işlemi etkin olup olmadığını bağlı olarak farklı sonuçlar döndürür. Eğer `AppDomain.CurrentDomain.FriendlyName` barındırma işlemi etkin döndürür *app_name*`.vhost.exe`. Bunu devre dışı barındırma işlemini çağırdığınızda, döndürür *app_name*`.exe`.  
  
## <a name="assemblygetcallingassemblyfullname-differences"></a>Assembly.GetCallingAssembly(). FullName farkları  
 `Assembly.GetCallingAssembly().FullName` barındırma işlemi etkin olup olmadığını bağlı olarak farklı sonuçlar döndürür. Eğer `Assembly.GetCallingAssembly().FullName` barındırma işlemi etkin döndürür `mscorlib`. Eğer `Assembly.GetCallingAssembly().FullName` barındırma işlemini devre dışı uygulama adını döndürür.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Barındırma süreci (vshost.exe)](../ide/hosting-process-vshost-exe.md)   
 [Nasıl yapılır: Kısmen güvenilen uygulamada hata ayıklama](../debugger/how-to-debug-a-partial-trust-application.md)   
 [Nasıl yapılır: Barındırma İşlemini Devre Dışı Bırakma](../ide/how-to-disable-the-hosting-process.md)

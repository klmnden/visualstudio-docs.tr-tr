---
title: 'Nasıl yapılır: Barındırma işlemini devre dışı bırakma | Microsoft Docs'
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-general
ms.topic: conceptual
helpviewer_keywords:
- hosting process, disabling
- vshost.exe, disabling the hosting process
ms.assetid: 9157488d-737f-454b-8d8d-36f99de38bb0
caps.latest.revision: 12
author: gewarren
ms.author: gewarren
manager: jillfra
ms.openlocfilehash: 813094285557171e9c7f021f597d0d643356b5d4
ms.sourcegitcommit: 08fc78516f1107b83f46e2401888df4868bb1e40
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/15/2019
ms.locfileid: "65694407"
---
# <a name="how-to-disable-the-hosting-process"></a>Nasıl yapılır: Barındırma İşlemini Devre Dışı Bırakma
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Barındırma işlemi etkinleştirildiğinde bazı API'lere giden çağrıların etkilenebilir. Bu gibi durumlarda doğru sonuçları döndürmek için barındırma işlemini devre dışı bırakmak gereklidir.  
  
### <a name="to-disable-the-hosting-process"></a>Barındırma işlemini devre dışı bırakmak için  
  
1. Yürütülebilir bir proje açın [!INCLUDE[vsprvs](../includes/vsprvs-md.md)]. Yürütülebilir dosyalar (örneğin, sınıf kitaplığı veya hizmeti projeleri) üretmez projeleri, bu seçeneği yoktur.  
  
2. Üzerinde **proje** menüsünü tıklatın **özellikleri**.  
  
3. Tıklayın **hata ayıklama** sekmesi.  
  
4. NET **Visual Studio barındırma işlemini etkinleştir** onay kutusu.  
  
   Barındırma işlemini devre dışı bırakıldığında, birçok hata ayıklama özellikleri kullanılamaz veya düşük performansla karşılaşabilirsiniz. Daha fazla bilgi için [hata ayıklama ve barındırma işlemi](../debugger/debugging-and-the-hosting-process.md).  
  
   Genel olarak, ne zaman barındırma işlemini devre dışı bırakılır:  
  
- Hata ayıklamayı başlatmak için gereken süre [!INCLUDE[dnprdnshort](../includes/dnprdnshort-md.md)] uygulamaları artar.  
  
- Tasarım zamanı ifade değerlendirmesi kullanılamıyor.  
  
- Kısmi güvende hata ayıklama kullanılamıyor.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Hata ayıklama ve barındırma işlemi](../debugger/debugging-and-the-hosting-process.md)   
 [Barındırma süreci (vshost.exe)](../ide/hosting-process-vshost-exe.md)   
 [Uygulama geliştirme sırasında oluşturur](https://msdn.microsoft.com/c9497d62-3b7b-4449-88e8-cf27acc9efe6)

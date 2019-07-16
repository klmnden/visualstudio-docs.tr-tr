---
title: 'Nasıl yapılır: Web uygulamalarında hata ayıklama | Microsoft Docs'
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
- Web services, debugging
- ASP.NET Web Forms, debugging
- ASP.NET, debugging Web applications
- debugging ASP.NET Web applications, during development
ms.assetid: 6440d12e-6b29-42c5-a958-99aeaaff480f
caps.latest.revision: 40
author: MikeJo5000
ms.author: mikejo
manager: jillfra
ms.openlocfilehash: cd3cbbcd740c0f124b8ab4379204a9d425cd541c
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "68205396"
---
# <a name="how-to-debug-web-applications"></a>Nasıl yapılır: Web Uygulamalarında Hata Ayıklama
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

[!INCLUDE[vstecasp](../includes/vstecasp-md.md)] Web uygulamaları geliştirmek için birincil teknolojidir [!INCLUDE[vsprvs](../includes/vsprvs-md.md)]. [!INCLUDE[vsprvs](../includes/vsprvs-md.md)] Hata ayıklayıcı, hata ayıklama için güçlü araçlar sağlar [!INCLUDE[vstecasp](../includes/vstecasp-md.md)] yerel veya uzak bir sunucuya Web uygulamaları. Bu konu, hata ayıklamak açıklar bir [!INCLUDE[vstecasp](../includes/vstecasp-md.md)] geliştirme sırasında proje. Hata ayıklama hakkında bilgi için bir [!INCLUDE[vstecasp](../includes/vstecasp-md.md)] Web bir üretim sunucusu üzerinde zaten dağıtılmış uygulaması, bakın [dağıtılan Web uygulamaları hata ayıklama](../debugger/debugging-deployed-web-applications.md).  
  
 Hata ayıklamak için bir [!INCLUDE[vstecasp](../includes/vstecasp-md.md)] uygulama:  
  
- Gerekli izinleriniz gerekir. Daha fazla bilgi için, bkz. [System Requirements](../debugger/aspnet-debugging-system-requirements.md).  
  
- [!INCLUDE[vstecasp](../includes/vstecasp-md.md)] içinde hata ayıklaması etkinleştirilmelidir **proje özellikleri**.  
  
- Uygulamanızın yapılandırma dosyası (Web.config) hata ayıklama moduna ayarlanmalıdır. Hata ayıklama modu nedenleri [!INCLUDE[vstecasp](../includes/vstecasp-md.md)] iliştirmek hata ayıklayıcı sağlar ve dinamik olarak oluşturulan dosyaları simgeleri üretmesine [!INCLUDE[vstecasp](../includes/vstecasp-md.md)] uygulama. [!INCLUDE[vsprvs](../includes/vsprvs-md.md)] Web proje şablonunu projenizi oluşturduysanız, hata ayıklamak başlattığınızda bu otomatik olarak ayarlar.  
  
- Daha fazla bilgi için [nasıl yapılır: ASP.NET uygulamaları için hata ayıklamayı](../debugger/how-to-enable-debugging-for-aspnet-applications.md).  
  
### <a name="to-debug-a-web-application-during-development"></a>Bir Web uygulaması geliştirme sırasında hata ayıklamak için  
  
1. Üzerinde **hata ayıklama** menüsünde tıklatın **Başlat** Web uygulamasına hata ayıklamayı başlatmak için.  
  
     [!INCLUDE[vsprvs](../includes/vsprvs-md.md)] Web uygulaması projesi oluşturur, gerekirse başlarsa ASP.NET geliştirme sunucusu yerel olarak hata ayıklaması yapıyorsanız, uygulama dağıtır ve ekler [!INCLUDE[vstecasp](../includes/vstecasp-md.md)] çalışan işlemi.  
  
2. Hata ayıklayıcısını kümesi ve açık kesme noktaları, adım ve herhangi bir uygulamada olduğu gibi diğer hata ayıklama işlemlerini gerçekleştirin.  
  
     Daha fazla bilgi için [hata ayıklayıcı temel bilgileri](../debugger/debugger-basics.md).  
  
3. Üzerinde **hata ayıklama** menüsünde tıklayın **hata ayıklamayı Durdur** son hata ayıklama oturumu veya üzerinde **dosya** Internet Explorer'da menüsünü **Kapat**.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Web uygulamalarında ve betikte hata ayıklama](../debugger/debugging-web-applications-and-script.md)   
 [ASP.NET ve AJAX uygulamalarında hata ayıklama](../debugger/debugging-aspnet-and-ajax-applications.md)   
 [Nasıl yapılır: ASP.NET Uygulamaları için Hata Ayıklamayı Etkinleştirme](../debugger/how-to-enable-debugging-for-aspnet-applications.md)

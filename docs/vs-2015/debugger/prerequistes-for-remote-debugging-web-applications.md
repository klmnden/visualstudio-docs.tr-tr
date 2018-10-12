---
title: Uzaktan hata ayıklama Web uygulamaları önkoşulları | Microsoft Docs
ms.custom: ''
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.reviewer: ''
ms.suite: ''
ms.technology:
- vs-ide-debug
ms.tgt_pltfrm: ''
ms.topic: article
dev_langs:
- FSharp
- VB
- CSharp
- C++
helpviewer_keywords:
- debugging ASP.NET Web applications, remote servers
- remote debugging, prerequisites
- remote servers, debugging Web applications
ms.assetid: 1cd777b5-6d20-4ca6-a0df-51653b118469
caps.latest.revision: 30
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: 448e6e7705e4df7330abce0e919adc705721102c
ms.sourcegitcommit: 9ceaf69568d61023868ced59108ae4dd46f720ab
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/12/2018
ms.locfileid: "49227311"
---
# <a name="prerequistes-for-remote-debugging-web-applications"></a>Uzak Hata Ayıklama Web Uygulamaları Önkoşulları
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

İle [!INCLUDE[vsprvs](../includes/vsprvs-md.md)] hata ayıklayıcı, bir Web uygulamasını yerel bilgisayarda veya uzak bir sunucu üzerinde şeffaf bir şekilde hata ayıklaması yapabilirsiniz. Bu, hata ayıklayıcı işlevleri aynı şekilde anlamına gelir ve herhangi bir bilgisayarın aynı özellikleri kullanmanıza olanak tanır. Uzaktan düzgün çalışması için hata ayıklama için ancak bazı önkoşulları vardır.  
  
-   [!INCLUDE[vsprvs](../includes/vsprvs-md.md)] Uzaktan hata ayıklama bileşenleri hata ayıklaması yapmak istediğiniz sunucuda yüklenmesi gerekir. Daha fazla bilgi için [ayarı yukarı uzaktan hata ayıklama](http://msdn.microsoft.com/library/90f45630-0d26-4698-8c1f-63f85a12db9c).  
  
-   Varsayılan olarak, [!INCLUDE[vstecasp](../includes/vstecasp-md.md)] çalışan işlemi, bir ASP.NET kullanıcı işlem olarak çalışır. Sonuç olarak, bilgisayarda yönetici ayrıcalıkları olmalıdır. burada [!INCLUDE[vstecasp](../includes/vstecasp-md.md)] hata ayıklamak için çalışır. Adını [!INCLUDE[vstecasp](../includes/vstecasp-md.md)] çalışan işlemi IIS sürümü ve hata ayıklama senaryosunu göre değişir. Daha fazla bilgi için [nasıl yapılır: ASP.NET işleminin adını bulma](../debugger/how-to-find-the-name-of-the-aspnet-process.md).  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [ASP.NET ve AJAX uygulamalarında hata ayıklama](../debugger/debugging-aspnet-and-ajax-applications.md)   
 [Sistem Gereksinimleri](../debugger/aspnet-debugging-system-requirements.md)




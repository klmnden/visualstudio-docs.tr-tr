---
title: 'Hata: Web hizmetlerinde hata ayıklama sırasında zaman aşımı | Microsoft Docs'
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-debug
ms.topic: reference
dev_langs:
- FSharp
- VB
- CSharp
- C++
helpviewer_keywords:
- debugger, Web application errors
- XML Web services, timeout while debugging
ms.assetid: 4b7df112-788a-4429-9a0c-4c6dac4fb609
caps.latest.revision: 11
author: MikeJo5000
ms.author: mikejo
manager: jillfra
ms.openlocfilehash: 5745a23e70f9245d6f1cb34a6d4ccc042f64bdd3
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62538339"
---
# <a name="error-timeout-while-debugging-web-services"></a>Hata: Web hizmetlerinde hata ayıklama sırasında zaman aşımı
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Çağrıldığı koddan bir XML Web hizmeti adımladığınızda, hata ayıklama devam edemiyor emin olmasına çağrı bazen sonuç zaman aşımı olabilir. Bunun gibi bir hata iletisi görebilirsiniz.  
  
```  
An unhandled exception of type 'System.Net.WebException' occurred in   
system.Web.services.dll  
Additional information: The operation has timed-out.  
```  
  
## <a name="solution"></a>Çözüm  
 Bu sorunu önlemek için XML Web hizmeti çağrısı için zaman aşımı değeri sonsuz olarak, bu örnekte gösterilen şekilde ayarlayın:  
  
```  
Service1 obj = new Service1();  
obj.TimeOut = -1; // infinite time out.  
```  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Web Uygulamalarında Hata Ayıklama: Hatalar ve Sorun Giderme](../debugger/debugging-web-applications-errors-and-troubleshooting.md)

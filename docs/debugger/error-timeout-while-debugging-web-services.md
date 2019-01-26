---
title: 'Hata: Web hizmetlerinde hata ayıklama sırasında zaman aşımı | Microsoft Docs'
ms.date: 11/04/2016
ms.topic: troubleshooting
dev_langs:
- CSharp
- VB
- FSharp
- C++
helpviewer_keywords:
- debugger, Web application errors
- XML Web services, timeout while debugging
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 0963d1675c3456601aba70bb5291b7cc19d454fb
ms.sourcegitcommit: 2193323efc608118e0ce6f6b2ff532f158245d56
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/25/2019
ms.locfileid: "54930764"
---
# <a name="error-timeout-while-debugging-web-services"></a>Hata: Web hizmetlerinde hata ayıklama sırasında zaman aşımı
Çağrıldığı koddan bir XML Web hizmeti adımladığınızda, hata ayıklama devam edemiyor emin olmasına çağrı bazen sonuç zaman aşımı olabilir. Bunun gibi bir hata iletisi görebilirsiniz.  
  
```cmd
An unhandled exception of type 'System.Net.WebException' occurred in   
system.Web.services.dll  
Additional information: The operation has timed-out.  
```  
  
## <a name="solution"></a>Çözüm  
 Bu sorunu önlemek için XML Web hizmeti çağrısı için zaman aşımı değeri sonsuz olarak, bu örnekte gösterilen şekilde ayarlayın:  
  
```csharp
Service1 obj = new Service1();  
obj.TimeOut = -1; // infinite time out.  
```  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Web Uygulamalarında Hata Ayıklama: Hatalar ve Sorun Giderme](../debugger/debugging-web-applications-errors-and-troubleshooting.md)

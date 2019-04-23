---
title: 'Hata: Otomatik olarak adımlanamıyor aktarılacaksa | Microsoft Docs'
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-debug
ms.topic: reference
f1_keywords:
- vs.debug.error.causality_no_server_response
dev_langs:
- FSharp
- VB
- CSharp
- C++
- JScript
- VB
- CSharp
- C++
helpviewer_keywords:
- remote debugging, notification error
ms.assetid: 9a370ccc-d358-429c-b285-9b6c0649bc68
caps.latest.revision: 16
author: MikeJo5000
ms.author: mikejo
manager: jillfra
ms.openlocfilehash: 2d979b53f4bd5962a01fa5eb1b77cc7c81c68a4a
ms.sourcegitcommit: 1fc6ee928733e61a1f42782f832ead9f7946d00c
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/22/2019
ms.locfileid: "60102425"
---
# <a name="error-unable-to-automatically-step-into-the-server"></a>Hata: Otomatik olarak adımlanamıyor aktarılacaksa
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Hata görünür:  
  
 Otomatik olarak adımlanamıyor aktarılacaksa. Hata ayıklayıcı uzak yordam yürütülmesi önce bildirilmedi  
  
 Bir web hizmeti adımlamak çalışırken, bu hata oluşabilir (bkz [Adımlama içine bir XML Web hizmeti](http://msdn.microsoft.com/8e67de38-bf5f-41cc-a457-1b88ce63d764)). Herhangi bir zamanda gerçekleşebilir [!INCLUDE[vstecasp](../includes/vstecasp-md.md)] düzgün ayarlanmadı.  
  
 Olası nedenler şunlardır:  
  
- Web.config dosyasında, [!INCLUDE[vstecasp](../includes/vstecasp-md.md)] uygulama ayarlı değil "true" debug (bkz [ASP.NET uygulamalarında hata ayıklama modu](../debugger/how-to-enable-debugging-for-aspnet-applications.md)).  
  
- Bir sürümünü [!INCLUDE[vstecasp](../includes/vstecasp-md.md)] Visual Studio yüklendikten sonra yüklendi. [!INCLUDE[vstecasp](../includes/vstecasp-md.md)] Visual Studio'da daha önce yüklü olması gerekir. Bu sorunu gidermek için Windows kullanın **Denetim Masası**, **programlar ve Özellikler** Visual Studio yüklemenizi onarmak için.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Uzaktan hata ayıklama ve sorun giderme](../debugger/remote-debugging-errors-and-troubleshooting.md)   
 [Uzaktan Hata Ayıklama](../debugger/remote-debugging.md)

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
ms.openlocfilehash: c8dcb8fa757f1cccf2f3aef6c2520e0c61da0b9f
ms.sourcegitcommit: 08fc78516f1107b83f46e2401888df4868bb1e40
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/15/2019
ms.locfileid: "65682674"
---
# <a name="error-unable-to-automatically-step-into-the-server"></a>Hata: Otomatik olarak adımlanamıyor aktarılacaksa
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Hata görünür:  
  
 Otomatik olarak adımlanamıyor aktarılacaksa. Hata ayıklayıcı uzak yordam yürütülmesi önce bildirilmedi  
  
 Bir web hizmeti adımlamak çalışırken, bu hata oluşabilir (bkz [Adımlama içine bir XML Web hizmeti](https://msdn.microsoft.com/8e67de38-bf5f-41cc-a457-1b88ce63d764)). Herhangi bir zamanda gerçekleşebilir [!INCLUDE[vstecasp](../includes/vstecasp-md.md)] düzgün ayarlanmadı.  
  
 Olası nedenler şunlardır:  
  
- Web.config dosyasında, [!INCLUDE[vstecasp](../includes/vstecasp-md.md)] uygulama ayarlı değil "true" debug (bkz [ASP.NET uygulamalarında hata ayıklama modu](../debugger/how-to-enable-debugging-for-aspnet-applications.md)).  
  
- Bir sürümünü [!INCLUDE[vstecasp](../includes/vstecasp-md.md)] Visual Studio yüklendikten sonra yüklendi. [!INCLUDE[vstecasp](../includes/vstecasp-md.md)] Visual Studio'da daha önce yüklü olması gerekir. Bu sorunu gidermek için Windows kullanın **Denetim Masası**, **programlar ve Özellikler** Visual Studio yüklemenizi onarmak için.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Uzaktan hata ayıklama ve sorun giderme](../debugger/remote-debugging-errors-and-troubleshooting.md)   
 [Uzaktan Hata Ayıklama](../debugger/remote-debugging.md)

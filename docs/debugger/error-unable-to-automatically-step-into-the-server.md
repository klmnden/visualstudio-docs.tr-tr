---
title: 'Hata: Otomatik olarak adımlanamıyor aktarılacaksa | Microsoft Docs'
ms.date: 11/04/2016
ms.topic: troubleshooting
f1_keywords:
- vs.debug.error.causality_no_server_response
dev_langs:
- CSharp
- VB
- FSharp
- C++
- JScript
helpviewer_keywords:
- remote debugging, notification error
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: e9d84f4c7f7f58ae980a266b436207c843926ae1
ms.sourcegitcommit: b0d8e61745f67bd1f7ecf7fe080a0fe73ac6a181
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/22/2019
ms.locfileid: "56711741"
---
# <a name="error-unable-to-automatically-step-into-the-server"></a>Hata: Otomatik olarak adımlanamıyor aktarılacaksa
Hata görünür:

 Otomatik olarak adımlanamıyor aktarılacaksa. Hata ayıklayıcı uzak yordam yürütülmesi önce bildirilmedi

 Bir web hizmeti adımlamak çalışırken, bu hata oluşabilir (bkz [Adımlama içine bir XML Web hizmeti](https://msdn.microsoft.com/library/8e67de38-bf5f-41cc-a457-1b88ce63d764)). Herhangi bir zamanda gerçekleşebilir [!INCLUDE[vstecasp](../code-quality/includes/vstecasp_md.md)] düzgün ayarlanmadı.

 Olası nedenler şunlardır:

- Web.config dosyasında, [!INCLUDE[vstecasp](../code-quality/includes/vstecasp_md.md)] uygulama ayarlı değil "true" debug (bkz [ASP.NET uygulamalarında hata ayıklama modu](../debugger/how-to-enable-debugging-for-aspnet-applications.md)).

- Bir sürümünü [!INCLUDE[vstecasp](../code-quality/includes/vstecasp_md.md)] Visual Studio yüklendikten sonra yüklendi. [!INCLUDE[vstecasp](../code-quality/includes/vstecasp_md.md)] Visual Studio'da daha önce yüklü olması gerekir. Bu sorunu gidermek için Windows kullanın **Denetim Masası > Programlar ve Özellikler** Visual Studio yüklemenizi onarmak için.

## <a name="see-also"></a>Ayrıca Bkz.
- [Uzaktan Hata Ayıklama Hataları ve Sorun Giderme](../debugger/remote-debugging-errors-and-troubleshooting.md)
- [Uzaktan Hata Ayıklama](../debugger/remote-debugging.md)
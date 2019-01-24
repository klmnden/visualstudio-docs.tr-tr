---
title: Uzak bilgisayara erişilmeye çalışılırken DCOM hatası oluştu. Erişim reddedildi. | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-debug
ms.topic: conceptual
f1_keywords:
- vs.debug.remote.dcom_access_denied
dev_langs:
- FSharp
- VB
- CSharp
- C++
- JScript
helpviewer_keywords:
- remote debugging, DCOM error
- remote DCOM access denied error
- DCOM, access errors
ms.assetid: 9d7dfc1b-9fe0-4f54-9c50-9c0e0f8358c5
caps.latest.revision: 30
author: MikeJo5000
ms.author: mikejo
manager: jillfra
ms.openlocfilehash: 0157b1ade2c38a2c10920b9674d7c9a58ac036b2
ms.sourcegitcommit: 8b538eea125241e9d6d8b7297b72a66faa9a4a47
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54796068"
---
# <a name="a-dcom-error-occurred-trying-to-contact-the-remote-computer-access-is-denied"></a>Uzak bilgisayara erişilmeye çalışılırken DCOM hatası oluştu. Erişim reddedildi.
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Uzaktan hata ayıklama, aşağıdaki durumlarda yerel ve uzak bilgisayarlar arasında iletişim kurmak için DCOM kullanır:  
  
- Hata ayıklayıcı kümesine **yerel uyumluluk modu** veya **yönetilen uyumluluk modu** iade **Araçlar / Seçenekler / hata ayıklama** sayfası  
  
- Yönetilen C++ hata ayıklama (C + +/ CLI) kodu.  
  
- Visual Studio 2013'te zaman **yerel Düzenle ve Devam Et'i etkinleştir** iade **Araçlar / Seçenekler / hata ayıklama** sayfası  
  
- Bazı üçüncü taraf hata ayıklama senaryoları  
  
  Visual Studio işlemini kendi kimlik doğrulaması yapamaz (veya sağlanan kimlik bilgilerinin yeterli kabul zaman) Bu hata oluşur. DCOM üzerinden uzaktan hata ayıklayıcı işleme. Bir veya daha fazla aşağıdaki geçici çözümlerden sorunu çözebilir:  
  
- Devre dışı **yerel uyumluluk modu** ve **yönetilen uyumluluk modu**.  
  
- Visual Studio 2013'te kapatmak **yerel Düzenle ve Devam Et'i etkinleştir**.  
  
- Her iki bilgisayar yeniden başlatın.  
  
- Uzaktan hata ayıklama kimlik bilgilerinin girilmesi gerekir, kimlik bilgilerini kaydetme seçeneğini denetleyin.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Uzaktan hata ayıklama ve sorun giderme](../debugger/remote-debugging-errors-and-troubleshooting.md)   
 [Uzaktan Hata Ayıklama](../debugger/remote-debugging.md)

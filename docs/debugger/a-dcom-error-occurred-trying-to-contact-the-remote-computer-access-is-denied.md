---
title: Uzak bilgisayara erişilmeye çalışılırken DCOM hatası oluştu. Erişim reddedildi. | Microsoft Docs
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- vs.debug.remote.dcom_access_denied
dev_langs:
- CSharp
- VB
- FSharp
- C++
- JScript
helpviewer_keywords:
- remote debugging, DCOM error
- remote DCOM access denied error
- DCOM, access errors
ms.assetid: 9d7dfc1b-9fe0-4f54-9c50-9c0e0f8358c5
author: mikejo5000
ms.author: mikejo
manager: douge
ms.workload:
- multiple
ms.openlocfilehash: c329704ee7f2ea19f56d3bd9201783a04d967de7
ms.sourcegitcommit: 37fb7075b0a65d2add3b137a5230767aa3266c74
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/02/2019
ms.locfileid: "53938669"
---
# <a name="a-dcom-error-occurred-trying-to-contact-the-remote-computer-access-is-denied"></a>Uzak bilgisayara erişilmeye çalışılırken DCOM hatası oluştu. Erişim reddedildi.
Uzaktan hata ayıklama, aşağıdaki durumlarda yerel ve uzak bilgisayarlar arasında iletişim kurmak için DCOM kullanır:  
  
- Hata ayıklayıcısını ayarlamak **yerel uyumluluk modu** veya **yönetilen uyumluluk modu** iade **Araçlar > Seçenekler > hata ayıklama** sayfası  
  
- Yönetilen C++ hata ayıklama (C + +/ CLI) kodu.  
  
- Visual Studio 2013'te zaman **yerel Düzenle ve Devam Et'i etkinleştir** iade **Araçlar > Seçenekler > hata ayıklama** sayfası  
  
- Bazı üçüncü taraf hata ayıklama senaryoları  
  
  Visual Studio işlemini kendi kimlik doğrulaması yapamaz (veya sağlanan kimlik bilgilerinin yeterli kabul zaman) Bu hata oluşur. DCOM üzerinden uzaktan hata ayıklayıcı işleme. Bir veya daha fazla aşağıdaki geçici çözümlerden sorunu çözebilir:  
  
- Devre dışı **yerel uyumluluk modu** ve **yönetilen uyumluluk modu**.  
  
- Visual Studio 2013'te kapatmak **yerel Düzenle ve Devam Et'i etkinleştir**.  
  
- Her iki bilgisayar yeniden başlatın.  
  
- Uzaktan hata ayıklama kimlik bilgilerinin girilmesi gerekir, kimlik bilgilerini kaydetme seçeneğini denetleyin.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Uzaktan hata ayıklama ve sorun giderme](../debugger/remote-debugging-errors-and-troubleshooting.md)   
 [Uzaktan Hata Ayıklama](../debugger/remote-debugging.md)
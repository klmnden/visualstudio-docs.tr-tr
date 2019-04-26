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
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 75d1c9f9c23df04ca19f68dada718fba12dc51f3
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62564697"
---
# <a name="a-dcom-error-occurred-trying-to-contact-the-remote-computer-access-is-denied"></a>Uzak bilgisayara erişilmeye çalışılırken DCOM hatası oluştu. Erişim reddedildi.
Uzaktan hata ayıklama, aşağıdaki durumlarda yerel ve uzak bilgisayarlar arasında iletişim kurmak için DCOM kullanır:

- Hata ayıklayıcısını ayarlamak **yerel uyumluluk modu** veya **yönetilen uyumluluk modu** iade **Araçlar > Seçenekler > hata ayıklama** sayfası

- Hata ayıklama yönetilen C++ (C++/CLI) kodu.

- Visual Studio 2013'te zaman **yerel Düzenle ve Devam Et'i etkinleştir** iade **Araçlar > Seçenekler > hata ayıklama** sayfası

- Bazı üçüncü taraf hata ayıklama senaryoları

  Visual Studio işlemini kendi kimlik doğrulaması yapamaz (veya sağlanan kimlik bilgilerinin yeterli kabul zaman) Bu hata oluşur. DCOM üzerinden uzaktan hata ayıklayıcı işleme. Bir veya daha fazla aşağıdaki geçici çözümlerden sorunu çözebilir:

- Devre dışı **yerel uyumluluk modu** ve **yönetilen uyumluluk modu**.

- Visual Studio 2013'te kapatmak **yerel Düzenle ve Devam Et'i etkinleştir**.

- Her iki bilgisayar yeniden başlatın.

- Uzaktan hata ayıklama kimlik bilgilerinin girilmesi gerekir, kimlik bilgilerini kaydetme seçeneğini denetleyin.

## <a name="see-also"></a>Ayrıca Bkz.

- [Uzaktan Hata Ayıklama Hataları ve Sorun Giderme](../debugger/remote-debugging-errors-and-troubleshooting.md)
- [Uzaktan Hata Ayıklama](../debugger/remote-debugging.md)